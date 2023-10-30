Runs nbdev-ci and deploys to private

Usage:
```
name: CI

permissions:
  contents: write
  pages: write
  
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
