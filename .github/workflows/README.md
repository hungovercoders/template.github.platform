# Actions

## Links

- [Tim Warner Actions Course and Links](https://github.com/timothywarner/actions-cert-prep)
- [Github Actions Marketplace](https://github.com/marketplace?type=actions)

## Action Structure

- Workflow > Jobs > Steps > Action
- [Detailed Hello World](hello-world.yml)

```yaml
name: hello-world
permissions:
  contents: read
on: [push]
jobs:
    build:
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
