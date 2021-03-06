##### Example: Using a single event

```yaml
# Triggered when code is pushed to any branch in a repository
on: push
```

##### Example: Using a list of events

```yaml
# Triggers the workflow on push or pull request events
on: [push, pull_request]
```

##### Example: Using multiple events with activity types or configuration

Se você precisar especificar tipos de atividade ou configuração para um evento, você deve configurar cada evento separadamente. Você deve anexar dois pontos (`:`) a todos os eventos, incluindo eventos sem configuração.

```yaml
on:
  # Trigger the workflow on push or pull request,
  # but only for the main branch
  push:
    branches:
      - main
  pull_request:
    branches:
      - main
  # Also trigger on page_build, as well as release created events
  page_build:
  release:
    types: # This configuration does not affect the page_build event above
      - created
```
