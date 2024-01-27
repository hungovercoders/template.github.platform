# template.github.platform

This repository is for experimentation and examples of how to use GitHub features.

- [template.github.platform](#templategithubplatform)
  - [README](#readme)
  - [Work Item Templates](#work-item-templates)
  - [Automation](#automation)

## README

- [Awesome Readme](https://github.com/matiassingers/awesome-readme)

## Work Item Templates

- [Awesome Github Templates](https://github.com/devspace/awesome-github-templates)

## Automation

- [Add to Project](.github/workflows/add-to-project.yml) - This workflow adds a new issue to a project board when a new issue is created. It leverages a user PAT token embedded as a github organisation secret that has issue and project write permissions only. It also references an organisation wide github variable to reference the project.
