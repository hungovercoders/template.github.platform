# template.github.platform

This repository is for experimentation and examples of how to use GitHub features.

- [template.github.platform](#templategithubplatform)
  - [README Examples](#readme-examples)
  - [.gitgnore Examples](#gitgnore-examples)
  - [Work Item Template Examples](#work-item-template-examples)
  - [Automation](#automation)
  - [Inner Source](#inner-source)

## README Examples

- [Awesome Readme](https://github.com/matiassingers/awesome-readme)

## .gitgnore Examples

- [Git Ignore Examples](https://github.com/github/gitignore)

## Work Item Template Examples

- [Hungovercoder Templates](.githhub/ISSUE_TEMPLATE) - Currently it appears only the yaml base templates allow for automatic linking projects to the issue. This is why have the [add to project](.github/workflows/add-to-project.yml) to cover non-template raised issues (such as mobile app).
- [Awesome Github Templates](https://github.com/devspace/awesome-github-templates)

## Automation

- [Hello World](.github/workflows/hello-world.yml) - This is the simplest github action workflow that allows for a base understanding of how they work.
- [Add to Project](.github/workflows/add-to-project.yml) - This workflow adds a new issue to a project board when a new issue is created. It leverages a user PAT token embedded as a github organisation secret that has issue and project write permissions only. It also references an organisation wide github variable to reference the project.

## Inner Source

- [Github Inner Source Guide](https://githubtraining.github.io/innersource-theory/#/measuring_success)
