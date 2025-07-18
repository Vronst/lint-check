# Reusable Workflows

This repository contains reusable GitHub Actions workflows for consistent automation across multiple projects.
This workflow check formating/linting for python code with ruff. (It does not edit code)

## 🔁 Reusable Release Workflow

### Usage

```yaml
# Exapmle job
name: test

on:
  push:
    branches:
      - main

# needed permissions
permissions:
  contents: read
  packages: read

# This is most important part
# This uses release workflow
jobs:
  release:
    uses: Vronst/Vronst/lint-check/.github/workflows/lint.yaml@1.0.0
    # (optional)
    with:
      python-version: '3.13'
```
