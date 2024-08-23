# Actions

## Links

* [Tim Warner Actions Course and Links](https://github.com/timothywarner/actions-cert-prep)

### Triggers

#### Push

```yaml
on:
    push:
        branches:
            - main
            - develop
```

#### Schedule

```yaml
on:
    schedule:
        - cron: '0 0 * * * *'
        
```

#### Manual

```yaml
on:
    workflow_dispatch 
```

#### Webhook

```yaml
on:
    webhook:
        url: www.example.com
```

