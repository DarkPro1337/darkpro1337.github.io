# Homepage

Hugo sources for [https://darkpro1337.github.io/](https://darkpro1337.github.io/).
The site uses the [Congo](https://github.com/jpanther/congo) theme, installed as a Hugo module.

This repository is now the single source of truth. Generated HTML is **not** committed; GitHub Actions builds and deploys it.

## Local preview

1. Clone this repo.
2. Open the repo root.
3. Run `hugo server`.
4. Open the URL Hugo prints (usually `http://localhost:1313/`).

## Publish

1. Edit content (markdown, layouts, assets).
2. Preview with `hugo server`.
3. Push to `master`.
4. GitHub Actions runs `hugo --minify` and deploys to Pages.

The workflow lives in `.github/workflows/deploy-pages.yml`. After the first merge, set **Settings → Pages → Source → GitHub Actions**.

Manual `hugo` output goes to `public/` (gitignored). Do not commit that folder or paste HTML into the repo root.

## Update theme

1. Open the repo root.
2. Run `hugo mod get -u`.
3. Commit `go.mod` / `go.sum` if they changed.
