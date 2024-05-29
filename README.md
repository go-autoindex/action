# Autoindex Action

GitHub Action for the [autoindex CLI](https://github.com/go-autoindex/cli).

## Getting Started

<details>
<summary>Deploy to GitHub Pages</summary>

```yml
name: autoindex

on:
  push:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  autoindex:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Autoindex
        uses: go-autoindex/action@v1
      - name: Setup Pages
        uses: actions/configure-pages@v5
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: .
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

</details>

## Inputs

See [action.yml](action.yml) for details.
