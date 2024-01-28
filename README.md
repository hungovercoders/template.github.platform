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

## Repo Insights

- [Insights](https://github.com/hungovercoders/template.github.platform/pulse) - Remember to use the insights tab and look through your repo to ensure you meet community standards and keep an eye on dependencies among other things.

## README Examples

- [Awesome Readme](https://github.com/matiassingers/awesome-readme)

## Work Item Template Examples

- [Hungovercoder Templates](.githhub/ISSUE_TEMPLATE) - Currently it appears only the yaml base templates allow for automatic linking projects to the issue. This is why have the [add to project](.github/workflows/add-to-project.yml) to cover non-template raised issues (such as mobile app).
- [Awesome Github Templates](https://github.com/devspace/awesome-github-templates)

## Markdown

- []()

## Automation

- [Actions](https://github.com/hungovercoders/template.github.platform/actions) - All automation from this repo can be found under its actions tab.
- [Hello World](.github/workflows/hello-world.yml) - This is the simplest github action workflow that allows for a base understanding of how they work.
- [Add to Project](.github/workflows/add-to-project.yml) - This workflow adds a new issue to a project board when a new issue is created. It leverages a user PAT token embedded as a github organisation secret that has issue and project write permissions only. It also references an organisation wide github variable to reference the project.

## Developer Environments

- [Github Dev](https://github.dev/hungovercoders/template.github.platform) - By changing any github repo URL to https://github.**dev**/{organisation}/{repo} instead of https://github.**com**/{organisation}/{repo} you get a light browser IDE to make text chamges easy. You wouldn't use this for real development as it can't run code etc but it is a quick way of updating markdown for example.
- [Gitpod](https://gitpod.io)
- [Github Codespaces](https://github.com/features/codespaces)

## Discussions

- [Discussions](https://github.com/hungovercoders/template.github.platform/wiki) - Remember the discussions tab is a great place to have conversations and gather feedback on the repo that can link to future issues etc.

## Wiki

- [Wiki](https://github.com/hungovercoders/template.github.platform/wiki) - Remember the wiki tab might be a better place for deep documentation so that you can keep the README more digestible!

## Projects

- [Projects](https://github.com/hungovercoders/template.github.platform/projects?query=is%3Aopen) - Don't forget to utilise projects for work management and link your codebase to one to make it easily accessible. This doesn't mean every issue magically appears there though currently and you'll need to setup some automation either via work item templates, automation in the project itself, or cover yourself with the [Add to Project](.github/workflows/add-to-project.yml) workflow in this repo.

- ## Inner Source

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


