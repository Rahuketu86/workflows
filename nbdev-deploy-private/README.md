Runs nbdev-ci and deploys to netlify

Usage:
```
name: CI
on:
  push:
    branches: [ "main", "master" ]
  workflow_dispatch:
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps: 
      - uses: Rahuketu86/workflows/nbdev-deploy-private@main
```
