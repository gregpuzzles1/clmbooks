# CLMBooks

CLMBooks is the source repository for https://clmbooks.org, the Christian Living Ministries Books website. The site exists to share Christian devotional and inspirational books rooted in Scripture, with a strong emphasis on the person and work of Jesus Christ.

The home page introduces the collection as a free resource for personal devotion, small-group study, Sunday School use, and ministry teaching. Visitors can read books online and download them as PDFs at no cost.

This repository currently contains content for over 80 books and booklets that are available for free reading and download.

The website administrator is Greg Christian. Ron Christian, whose writing and ministry are featured throughout the site, is Greg Christian's uncle.

## Site Highlights

- Free Christian devotional books from Christian Living Ministries in Fort Collins, Colorado
- More than 80 books and booklets available for online reading and PDF download
- Content centered on biblical teaching, spiritual growth, and practical Christian living
- Multiple book collections, including devotional series, journal entries, and themed booklet groups

## Tech Stack

- Hugo static site generator
- Blowfish Hugo theme
- Markdown content files with front matter
- TOML-based Hugo configuration
- Custom Hugo layouts, partials, and shortcodes
- Custom CSS in `assets/css/custom.css`
- Static assets and hosted PDF downloads
- Google Analytics integration
- GitHub Actions for build and deployment automation

## Repository Structure

- `content/` contains the site pages and book entries
- `config/_default/` contains the Hugo site configuration
- `layouts/` contains custom templates, list layouts, partials, and shortcodes
- `assets/` contains custom CSS and supporting metadata files
- `static/` contains static files served directly by Hugo
- `themes/blowfish/` contains the vendored Blowfish theme

## Local Development

### Prerequisites

- Hugo extended edition installed locally

### Common Commands

Run the local development server:

```powershell
hugo server
```

Build the production site:

```powershell
hugo
```

## Deployment Output

Generated site output is written to `public/` when Hugo builds the site.

## Deployment

The live site is built and deployed only through GitHub Actions.

Production deployments are triggered from the `main` branch, which is the branch used for the published site.