# Theo Avila’s website

This site uses the standard **Minimal Mistakes** Jekyll theme with the **Air**
skin. Its original layouts, includes, Sass styles, JavaScript, and footer are
retained. Pages use the built-in `single` layout and author sidebar.

## Edit the site

- `index.md`: home page introduction and research overview.
- `_pages/publications.md`: publications, written in ordinary Markdown.
- `_pages/research.md`: the older research address, retained for existing links.
- `_data/navigation.yml`: Home and Publications navigation links.
- `_config.yml`: site title, author biography, email, Scholar link, and theme skin.

The `author.avatar` setting is blank, so no photo or placeholder appears.
To add a photo, place it in `assets/` and set that setting to its path.
The GitHub profile link is omitted from the author sidebar. This does not change
the repository’s visibility.

## Preview and build

With Ruby 3.3 and Bundler installed:

```sh
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000`. Restart the server after changing `_config.yml`.

To build without serving:

```sh
JEKYLL_ENV=production bundle exec jekyll build --strict_front_matter
```

The build workflow checks pushes and pull requests. Preserve the existing
GitHub Pages publishing settings; pushing to the configured publishing branch
updates the public website.

Theme documentation is included in `docs/` and available at
[Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/).
The original theme license is retained in `LICENSE`.
