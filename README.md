# template.github.platform

This repository is for experimentation and examples of how to use GitHub features.

- [template.github.platform](#templategithubplatform)
  - [README Examples](#readme-examples)
  - [Work Item Template Examples](#work-item-template-examples)
  - [Automation](#automation)
  - [Inner Source](#inner-source)
  - [Security](#security)
    - [.gitgnore Examples](#gitgnore-examples)
    - [Policy](#policy)
    - [Codeowners](#codeowners)
    - [Automation](#automation-1)

## README Examples

- [Awesome Readme](https://github.com/matiassingers/awesome-readme)

## Work Item Template Examples

- [Hungovercoder Templates](.githhub/ISSUE_TEMPLATE) - Currently it appears only the yaml base templates allow for automatic linking projects to the issue. This is why have the [add to project](.github/workflows/add-to-project.yml) to cover non-template raised issues (such as mobile app).
- [Awesome Github Templates](https://github.com/devspace/awesome-github-templates)

## Automation

- [Hello World](.github/workflows/hello-world.yml) - This is the simplest github action workflow that allows for a base understanding of how they work.
- [Add to Project](.github/workflows/add-to-project.yml) - This workflow adds a new issue to a project board when a new issue is created. It leverages a user PAT token embedded as a github organisation secret that has issue and project write permissions only. It also references an organisation wide github variable to reference the project.

## Inner Source

- [Github Inner Source Guide](https://githubtraining.github.io/innersource-theory/#/measuring_success)

## Security

### .gitgnore Examples

- [Git Ignore Examples](https://github.com/github/gitignore)

### Policy

- [Security Policy](https://github.com/hungovercoders/template.github.platform/security/policy) - This is maintanied by SECURITY.md file in the root of the repository. It is a good idea to have a security policy in place to ensure that any security issues are reported to the correct people.

### Codeowners

- [Hungovercoders Codeowners](.github/CODEOWNERS) - This is a simple example of how to use codeowners to automatically assign reviewers to pull requests. It also shows how to use a wildcard to assign a team to a folder.
- [About Codeowners](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)

### Automation

- [Security Analysis](https://github.com/hungovercoders/template.github.platform/settings/security_analysis) - Consider enabling and automating dependabot alerts and security updates. This will ensure that any security issues are automatically raised as issues and pull requests.
