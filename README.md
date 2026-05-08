# Personal site

Minimal monospace Jekyll site with auto light/dark mode.

## Structure

```
.
├── _config.yml           # site metadata, your name, socials, nav
├── _data/
│   ├── projects.yml      # add projects here — no HTML needed
│   └── publications.yml  # add papers here — no HTML needed
├── _includes/nav.html    # top navigation
├── _layouts/
│   ├── default.html      # base layout (head, nav, footer)
│   └── page.html         # extends default, adds page title
├── assets/css/main.css   # all styling — single file
├── index.html            # hero landing page
├── about.md              # /about/
├── projects.md           # /projects/   (renders _data/projects.yml)
└── publications.md       # /publications/ (renders _data/publications.yml)
```

## Run locally

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>.

## Customize

1. **Your info** → edit `_config.yml` (name, tagline, affiliation, socials).
2. **Hero copy** → edit the `<div class="hero-bio">` paragraph in `index.html`.
3. **About page** → edit `about.md`.
4. **Add a project** → add an entry to `_data/projects.yml`.
5. **Add a publication** → add an entry to `_data/publications.yml`.
6. **Restyle** → all CSS lives in `assets/css/main.css`. Color variables
   are at the top — light mode under `:root`, dark mode under
   `@media (prefers-color-scheme: dark)`.

## Deploy

For GitHub Pages: push to `yourusername.github.io` and enable Pages
(Settings → Pages → Source: GitHub Actions, with the default Jekyll workflow).
