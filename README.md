<p align="center">
  <a href="https://github.com/yuya-takeyama/open-backport-pull-request-action"><img alt="open-backport-pull-request-action status" src="https://github.com/yuya-takeyama/open-backport-pull-request-action/workflows/build-test/badge.svg"></a>
</p>

# Open Backport Pull Request

Open a backport Pull Request from a branch

## Usage

```yaml
on:
  push:
    branches:
      - main

jobs:
  backport:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: yuya-takeyama/open-backport-pull-request-action@v0.1.0
```

## Inputs

| Name           | Required | Default             | Description                        |
|----------------|----------|---------------------|------------------------------------|
| `github-token` | `true`   | ${{ github.token }} | GitHub API token                   |
| `head-ref`     | `true`   | ${{ github.ref }}   | HEAD ref to create a Pull Request  |
