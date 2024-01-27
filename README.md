# template.github.platform

This repository is for experimentation and examples of how to use GitHub features.

- [template.github.platform](#templategithubplatform)
  - [README Examples](#readme-examples)
  - [Work Item Template Examples](#work-item-template-examples)
  - [Automation](#automation)

## README Examples

- [Awesome Readme](https://github.com/matiassingers/awesome-readme)

## Work Item Template Examples

- [Awesome Github Templates](https://github.com/devspace/awesome-github-templates)

## Automation

- [Hello World](.github/workflows/hello-world.yml) - This is the simplest github action workflow that allows for a base understanding of how they work.
- [Add to Project](.github/workflows/add-to-project.yml) - This workflow adds a new issue to a project board when a new issue is created. It leverages a user PAT token embedded as a github organisation secret that has issue and project write permissions only. It also references an organisation wide github variable to reference the project.
