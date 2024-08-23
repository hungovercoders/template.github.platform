# Actions

## Links

- [Tim Warner Actions Course and Links](https://github.com/timothywarner/actions-cert-prep)
- [Github Actions Marketplace](https://github.com/marketplace?type=actions)
- [Github Docs Actions](https://docs.github.com/en/actions)
- [Github Docs Actions Contexts](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/accessing-contextual-information-about-workflow-runs#github-context)

## Action Structure

- Workflow > Jobs > Steps > Action
- [Detailed Hello World](hello-world.yml)

```yaml
name: hello-world
permissions:
  contents: read
on: [push]
jobs:
    job1:
        runs-on: ubuntu-latest
        steps:
            - name: Checkout
              uses: actions/checkout@v2
            - name: Hello World
              run: echo "Hello World"
            with:
                MY_VAR: "Griff
```

## Triggers

### Push

```yaml
on:
  push:
    branches:
      - main
      - develop
```

### Pull Request

```yaml
on:
  pull_request:
    branches:
      - main
```

### Schedule

```yaml
on:
  schedule:
    - cron: "0 0 * * * *"
```

### Manual

```yaml
on: workflow_dispatch
```

### Webhook

```yaml
on:
  webhook:
    url: www.example.com
```

## Conditions

```yaml
jobs:
  job1:
    runs-on: ubuntu-latest
    if: github.ref == 'refs/heads/main'
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Hello World
        run: echo "Hello World"
    needs: [job1]
    runs-on: ubuntu-latest
    if: github.ref == 'refs/heads/main'
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Hello World
        run: echo "Hello World"
```
