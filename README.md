# CLMBooks

CLMBooks is the source repository for [clmbooks.org](https://clmbooks.org), a Hugo-powered site that publishes free Christian devotional books from Christian Living Ministries in Fort Collins, Colorado.

The site content includes multiple book and booklet collections, downloadable assets, and custom Hugo layouts built on top of the Blowfish theme.

## Stack

- [Hugo](https://gohugo.io/) extended edition
- Blowfish theme, vendored in `themes/blowfish`
- GitHub Pages deployment via GitHub Actions

The current deployment workflow builds the site with Hugo `0.163.3`.

## Local development

### Prerequisites

- Hugo extended edition installed locally

### Start the local server

```powershell
hugo server
```

The local server will build the site and serve it with live reload.

### Create a production build

```powershell
hugo
```

For the same style of optimized build used in CI, run:

```powershell
hugo --gc --minify
```

Generated output is written to `public/`. Hugo build artifacts are also cached in `resources/`. Both are ignored by Git.

## Repository structure

- `content/`: Markdown source for the site, organized by book series and collections
- `layouts/`: Site-specific Hugo templates and overrides
- `assets/`: Custom CSS and supporting source assets
- `static/`: Files copied directly to the generated site
- `config/_default/`: Hugo site configuration
- `themes/blowfish/`: Vendored theme source
- `.github/workflows/`: GitHub Actions workflows for deployment and community automation

## Content collections

The site currently includes collections such as:

- Effective Christian Living Booklets
- From Ron's Journal
- Growing a Godly Life Series
- More Devotional Books
- Sanctity of Human Life Series

Each collection lives under `content/` and may also have section-specific layouts under `layouts/`.

## Deployment

Deployments are handled automatically by [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) when changes are pushed to `main`.

The workflow:

1. Checks out the repository.
2. Installs Hugo extended `0.163.3`.
3. Builds the site with `hugo --gc --minify`.
4. Publishes the generated `public/` directory to GitHub Pages.

## Contributing

Typical content and site updates:

1. Edit or add Markdown files under `content/`.
2. Update layouts, assets, or static files as needed.
3. Run `hugo` locally to verify the site builds.
4. Open a pull request against `main`.

If you add new layouts or styling, keep changes scoped to the relevant section so the existing site presentation remains consistent.