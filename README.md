# <center>Create an example workflow</center>

## 1. Under your working directory

```dash
 git init
```

## 2. Create folder '''dash .github/workflows/```

```dash
mkdir .github
mkdir .github/workflows
```

In the .github/workflows/ directory, create a new file called learn-github-actions.yml and add the following code.

```dash
name: learn-github-actions
on: [push]
jobs:
  check-bats-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: '14'
      - run: npm install -g bats
      - run: bats -v
```
