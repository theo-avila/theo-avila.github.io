# Theo Avila’s website

A small Jekyll site for GitHub Pages. Main navigation has **Home** and
**Publications**; research lives on the home page. The old `/research/` URL
still works. There is no public repository link or theme credit in the layout.
This does not change the GitHub repository’s visibility.

## Edit content

- `index.html`: introduction and home page sections.
- `_includes/research-topics.html`: research descriptions (shared with the old research URL).
- `_data/publications.yml`: papers, authors, years, DOI links, and preparation status.
  Mark a paper `featured: true` to show it on the home page.
- `_config.yml`: name, contact email, Google Scholar URL, and optional portrait.
- `_data/navigation.yml`: navigation.
- `assets/css/academic.css`: colors, typography, and responsive layout.
- `_layouts/academic.html`: shared page shell and footer.

No portrait is required. To add one, put your image in `assets/` and set
`portrait: /assets/your-photo.jpg` in `_config.yml`.

## Preview locally

With Ruby 3.3 and Bundler installed:

```sh
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000`. Restart the server after editing `_config.yml`.

## Build

```sh
JEKYLL_ENV=production bundle exec jekyll build --strict_front_matter
```

Output goes into `_site/` (ignored by Git). The GitHub Actions build checks the
site on pushes and pull requests; it does not deploy it. For the existing
GitHub Pages site, preserve its publishing settings. If using branch-based
publishing, use `master` and `/ (root)`. Changes become public when pushed to
the configured publishing branch.

## Content notes

The fire-weather paper’s published status and bibliographic details were checked
against the [University of Illinois publication record](https://experts.illinois.edu/en/publications/downscaled-cmip5-projections-of-physical-fire-risk-understate-his/).
The maize manuscript retains the previous site’s “in preparation” status.

Unused Minimal Mistakes source files are retained for reference and licensing;
the website uses the independent `academic` layout. Theme demos, tooling, and
unused assets are excluded from the generated site. The original `LICENSE` is retained.
