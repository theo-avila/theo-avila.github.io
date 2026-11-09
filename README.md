# Theo Avila’s website

This site uses the standard **Minimal Mistakes** Jekyll theme with the **Air**
skin. Its original layouts, includes, JavaScript, and footer are retained. Pages use
the built-in `single` layout, image header, and author sidebar. Small Sass
overrides improve text size and image presentation without replacing the theme.

## Edit the site

- `index.md`: home page introduction and research overview.
- `_pages/publications.md`: publications, written in ordinary Markdown.
- `_pages/research.md`: the older research address, retained for existing links.
- `_includes/research-overview.md`: research text shared by the home and research pages.
- `_data/navigation.yml`: Home and Publications navigation links.
- `_config.yml`: site title, author biography, portrait, email, Scholar link, and theme skin.
- `assets/css/main.scss`: the theme’s font-size settings (18px mobile, 20px desktop).
- `_sass/site.scss`: navigation heading size, line spacing, banner height, and portrait sizing.

The portrait is the existing `assets/bio-photo.jpg`, set through `author.avatar`
in `_config.yml`. The home and publications pages use the existing
`assets/publications.jpg` as their top banner. To replace the banner, change
`header.image` and its `header.image_description` in those pages. The original
image files are unchanged; CSS controls their displayed crop.
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

## Layout references

The portrait-and-banner structure takes general inspiration from
[Wenda Zhang](https://wendazhang33.github.io/) and
[Stephen Griffies](https://stephengriffies.github.io/), who also use Minimal Mistakes.
The short selected-publication section takes inspiration from
[Jake Steinberg](https://jakesteinberg.github.io/).
No text or images from those sites are included here.
