Builds, run and deploy jupyterbook on netlify even inside nbdev python repo

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
      - uses: Rahuketu86/workflows/nbdev-deploy-netlify@main
        with:
          NETLIFY_AUTH_TOKEN: ${{ secrets.NETLIFY_AUTH_TOKEN }}
```
