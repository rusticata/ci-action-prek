# ci-action-prek

Github CI action to install and run [prek](https://github.com/j178/prek)

## Inputs

```yaml
inputs:
  prek-version:
    description: 'prek version to use'
    default: "0.2.0"
```

## Usage

```yaml
name: CI
on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]
  workflow_dispatch:

jobs:
  readme:
    name: Run prek (pre-commit) checks
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v5
      - id: prek
        uses: rusticata/ci-action-prek@master
```
