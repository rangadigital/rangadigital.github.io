# rangadigital.github.io

Source for the [Ranga Digital](https://rangadigital.github.io/) website, a static
site published with GitHub Pages.

Ranga Digital builds editor extensions and data-driven architectural tools for
Unity 6.

## Pages

| URL | Source | Purpose |
| --- | --- | --- |
| [`/`](https://rangadigital.github.io/) | `index.html` | Landing page, product overview and support form |

## Structure

```
.
├── index.html            Landing page
├── assets/
│   └── img/              Shared images, referenced by every page
├── robots.txt            Crawler directives
├── sitemap.xml           Sitemap submitted to Google Search Console
└── google*.html          Search Console verification token
```

Each page is a self-contained HTML file with its own inline `<style>` block. There
is no build step, bundler or dependency install. What is committed is what ships.

## Local development

No tooling required. Open `index.html` directly, or serve the folder to get
correct absolute paths:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Pushing to `main` publishes automatically via GitHub Pages (branch `main`, path
`/`). No workflow file is involved.

## Conventions

- Filenames are lowercase `kebab-case`; images are named for what they show
  (`asset-sentinel-01.png`, not `AS3.png`).
- Shared images live in `assets/img/` and are referenced with relative paths
  (`assets/img/...` from the root, `../assets/img/...` from a subfolder).
- Every page sets `<title>`, `<meta name="description">` and `<link rel="canonical">`.

## Notes for future edits

Some paths are referenced externally and must not be renamed or moved:

- `google8083060ec2a3580d.html`: Google Search Console verification; must stay at the
  repository root under this exact name
- `robots.txt` and `sitemap.xml`: must stay at the root

Add new pages to `sitemap.xml` and update `lastmod` when content changes materially.

## License

© 2026 Ranga Digital. All rights reserved.

The site content, product copy and images in this repository are not licensed for
reuse.
