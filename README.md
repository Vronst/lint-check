# Exapmle job
name: test

on:
  push:
    branches:
      - main

# needed permissions
permissions:
  contents: write
  packages: write

# This is most important part
# This uses release workflow
jobs:
  release:
    uses: Vronst/Vronst/lint-check/.github/workflows/lint.yaml@1.0.0
    with:
      python-version: '3.13'
    secrets:
      TOKEN: ${{ secrets.PRO_TOKEN }}
