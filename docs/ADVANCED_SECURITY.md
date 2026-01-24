# Github Advanced Security 

- See example exercise repo here for [dependencies](https://github.com/dataGriff/skills-secure-repository-supply-chain).

## Dependencies

### Dependendy Graph

- This repositorys [dependency graph](https://github.com/hungovercoders/template.github.platform/network/dependencies) found at insights > dependency graph. Sourced from lock and manifest files in the repository. Direct and indirect dependencies are listed. Enabled by default for public repositories. Need to enable for private repositories.

[Supported files](https://docs.github.com/en/code-security/reference/supply-chain-security/dependency-graph-supported-package-ecosystems) to use to generate the dependency graph.

### Advisory Database

[Github advisory database](https://github.com/advisories) is a collection of security advisories that affect open source packages. It is used to power security features like Dependabot alerts and security updates.

it uses the [common vilnerability scoring system (CVSS)](https://www.first.org/cvss/v3.1/specification-document) to rate the severity of vulnerabilities.

The database is populated by a number of sources.

### Software Bill of Materials (SBOM)

Machine readable inventory of projecct dependencies and associated information (versions identifies and licenses). Reduce supply chain risks and improve compliance.

Exportable in [SPDX](https://spdx.github.io/spdx-spec/v2.3/) format.

### Dependency Review

Github tool that helps you understand dependency changes in a pull request. It highlights new or updated dependencies and any associated security vulnerabilities. Proactive approach to managing dependencies whereas dependabot is reactive.

### Dependabot

Github tool that helps you keep up to date with your dependencies by automatically checking for updates and security vulnerabilities. Comprised of dependabot alerts, security updates and version updates.

### Dependabot Alerts

Rely on dependency graph and advisory database to notify you about known security vulnerabilities in your dependencies. Alerts are created for vulnerable dependencies in your repository. Viewable in security tab > dependabot alerts. These can be reactive or proactive in pull requests.

Alerts not enabled by default, you have to turn them on in [security settings](https://github.com/settings/security_analysis) for your repositories. For an organisation you have to enable it in the organisation settings e.g. [hungovercoder organisation settings](https://github.com/organizations/hungovercoders/settings/security_products).Enterprise owners can enable it for all repositories in the enterprise.

Dependabot alerts for this repo can be found at [https://github.com/hungovercoders/template.github.platform/security/dependabot](https://github.com/hungovercoders/template.github.platform/security/dependabot). Its congiguration can be found at in [security analysis settings](https://github.com/hungovercoders/template.github.platform/settings/security_analysis) of the repo. In this area you can also turn on automated PRs for security updates. You can also get automated updates through a dependabot yaml file as a [github action](../.github/dependabot.yml).

You can configure notifcations for dependabot alerts in your organisation [notification settings](https://github.com/settings/notifications#vulnerability-alerts-heading).

#### Data Driven Decision and Resolution

- Review the alert > Evaludate the Risk > Decide Action Based no Data > Document the Decision > Immediate Remediation > Close the Alert > Monitor Alerts.

### Dependabot Security Updates

When a vulnerability is found in one of your dependencies, dependabot can automatically create a pull request to update the dependency to a secure version. This helps you quickly remediate vulnerabilities without having to manually track and update dependencies.  

### Dependabot Version Updates

Dependabot can also help you keep your dependencies up to date by automatically checking for new versions and creating pull requests to update them. This helps you stay current with the latest features and bug fixes in your dependencies.

### Example Dependabot Configuration File

```yaml
# Basic dependabot.yml file with
# configuration for two package managers

version: 2
updates:
  # Enable version updates for npm
  - package-ecosystem: "npm"
    # Look for `package.json` and `lock` files in the `root` directory
    directory: "/"
    # Check the npm registry for updates every day (weekdays)
    schedule:
      interval: "daily"
    groups:
      production-dependencies:
        dependency-type: "production"
      development-dependencies:
        dependency-type: "development"

  # Enable version updates for Docker
  - package-ecosystem: "docker"
    # Look for a `Dockerfile` in the `root` directory
    directory: "/"
    # Check for updates once a week
    schedule:
      interval: "weekly"
    groups:
      production-dependencies:
        dependency-type: "production"
      development-dependencies:
        dependency-type: "development"
```

### Notifications

By default, users receive notifications in the following manner:

- By email: An email is sent when Dependabot is enabled for a repository, when a new manifest file is committed to the repository, and when a new vulnerability with a critical or high severity is found (Email option).
- In the user interface: A warning is shown in your repository's file and code views if there are any vulnerable dependencies.
- On the command line: Warnings are displayed as callbacks when you push to repositories with any insecure dependencies (CLI option).
- In your inbox: As web notifications. A web notification is sent when Dependabot is enabled for a repository, when a new manifest file is committed to the repository, and when a new vulnerability with a critical or high severity is found (On GitHub option).
- On GitHub Mobile: As web notifications.

### Graph QL Queries

- Query to get dependabot alerts for a repository

```graphql
{
  repository(owner: "hungovercoders", name: "template.github.platform") {
    vulnerabilityAlerts(first: 10) {
      nodes {
        createdAt
        dismissedAt
        securityVulnerability {
          package {
            name
          }
          advisory {
            summary
            severity
            references {
              url
            }
          }
        }
      }
    }
  }
}
```

### Dependency Review

Allows you to shift left and review dependency changes in pull requests before merging them. It highlights new or updated dependencies and any associated security vulnerabilities.

You can setup one of these using a github action in your repository. Easiest way is to go to github actions and select new workflow and type "dependency review". This will create a workflow file in your .github/workflows/dependency-review.yml file. You can configure this to better suit your needs.

You can setup a number of [dependency review confiuration options](https://github.com/marketplace/actions/dependency-review#configuration-options?azure-portal=true).

You can enforce dependency review in your repository by setting up branch protection rules. This will require that all pull requests pass the dependency review check before they can be merged.

You can check dependency review results in the "Checks" tab of a pull request. Any new or updated dependencies will be listed, along with any associated security vulnerabilities.
