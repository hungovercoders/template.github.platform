# Github Advanced Security 

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

### Dependabot

Github tool that helps you keep up to date with your dependencies by automatically checking for updates and security vulnerabilities. Comprised of dependabot alerts, security updates and version updates.

### Dependabot Alerts

Rely on dependency graph and advisory database to notify you about known security vulnerabilities in your dependencies. Alerts are created for vulnerable dependencies in your repository. Viewable in security tab > dependabot alerts. These can be reactive or proactive in pull requests.

Alerts not enabled by default, you have to turn them on in [security settings](https://github.com/settings/security_analysis) for your repositories. For an organisation you have to enable it in the organisation settings e.g. [hungovercoder organisation settings](https://github.com/organizations/hungovercoders/settings/security_products).Enterprise owners can enable it for all repositories in the enterprise.

Dependabot alerts for this repo can be found at [https://github.com/hungovercoders/template.github.platform/security/dependabot](https://github.com/hungovercoders/template.github.platform/security/dependabot). Its congiguration can be found at in [security analysis settings](https://github.com/hungovercoders/template.github.platform/settings/security_analysis) of the repo. In this area you can also turn on automated PRs for security updates. You can also get automated updates through a dependabot yaml file as a [github action](../.github/dependabot.yml).

You can configure notifcations for dependabot alerts in your organisation [notification settings](https://github.com/settings/notifications#vulnerability-alerts-heading).

### Dependency Review

Github tool that helps you understand dependency changes in a pull request. It highlights new or updated dependencies and any associated security vulnerabilities. Proactive approach to managing dependencies whereas dependabot is reactive.
