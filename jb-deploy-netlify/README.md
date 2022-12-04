Builds, run and deploy jupyterbook on netlify even inside nbdev python repo

Usage:
```
name: deploy-book

on:
  push:
    paths:
    - 'book/**'
    branches:
    - main
    - master
  workflow_dispatch:

concurrency:
  group: jupyterbook-export
  cancel-in-progress: true  


# This job installs dependencies, builds the book, and pushes it to `netlify`
jobs:
  deploy-book:
    runs-on: ubuntu-latest
    steps:
    - uses: Rahuketu86/workflows/jb-deploy-netlify@main
      with:
        book_folder: book
        is_inside_nbdev: true
        requirements: 'requirements.txt'
        NETLIFY_AUTH_TOKEN: ${{ secrets.NETLIFY_AUTH_TOKEN }}
        NETLIFY_SITE_ID: ${{ secrets.NETLIFY_SITE_ID}}
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
