# AGENTS.md

Guidance for AI coding agents working in this repository.

## What this is

The marketing/docs site for **MapMindAI**, an open-source SLAM/robotics-perception
project, hosted on GitHub Pages at `mapmindai.github.io`. It's a static
[Jekyll](https://jekyllrb.com/) site built on a customized fork of the
`beautiful-jekyll-theme`. There is no application backend, database, or JS
build pipeline — pages are markdown/HTML with Liquid templating, styled with
hand-written CSS.

## Running locally

```bash
bundle install
bundle exec jekyll serve --incremental --host 0.0.0.0   # or: HOST=0.0.0.0 ./run.sh
```

Site serves at `http://localhost:4000` by default. `run.sh` accepts an
optional `rebuild` argument to force a full (non-incremental) build — useful
when `_config.yml`, layouts, or includes change, since `--incremental` doesn't
always pick those up.

There is no test suite. To verify a change, build/serve the site and check
the affected page renders correctly (see "Verifying changes" below).

## Repo structure

- `index.md` — homepage (hero, showcase, portfolio sections); custom CSS in `assets/css/index.css`
- `aboutme.md` — About page
- `uniscanner.md` — product landing page for the UniScanner hardware; custom CSS in `assets/css/uniscanner.css`
- `products/` — reserved for additional product pages (currently empty)
- `_posts/` — blog posts (currently empty); rendered via `blog/index.html` with pagination
- `_layouts/` — `base.html` (root, loads CSS/JS + favicon), `default.html`, `page.html`, `home.html`, `post.html`, plus `page_tree_*.html` (unused doc-tree layouts inherited from the theme fork)
- `_includes/` — header/footer/nav partials, comment integrations (Disqus/Staticman/Utterances/Facebook), analytics snippets (GA/GTM/Matomo)
- `_data/portfolio.yml` — GitHub project cards shown on the homepage
- `_data/learn_info.yml` — the "what we build" bullet list on the homepage
- `_data/ui-text.yml` — localized UI strings (comments form, etc.)
- `assets/css/` — one stylesheet per concern; `main.css`/`theme.css` are theme-wide, `index.css`/`uniscanner.css` are page-specific. No preprocessor/bundler — edit CSS directly.
- `assets/js/` — vanilla JS (`main.js` nav/scroll behavior, `image_zoom.js`, `simple-jekyll-search.min.js`, `staticman.js`). No bundler.
- `assets/videos/` — product demo videos, with generated poster frames in `assets/videos/posters/` (see "Adding video assets")
- `assets/img/` — logos, favicons, static images
- `data/` — local-only scratch folder for raw source media (git-ignored, excluded from the Jekyll build via `_config.yml`); not deployed
- `_config.yml` — site config: nav links, colors, social links, excluded paths, plugins (`jekyll-paginate`, `jekyll-sitemap`)
- `.github/workflows/ci.yml` — builds the site with Jekyll on push/PR and (via GitHub Pages Actions) deploys `main`

## Conventions

- Front matter: pages use `layout: base` directly (not `page` or `default`) when they need full control over the `<body>` for custom hero/section markup — see `index.md` and `uniscanner.md`. Use `layout: page` for simple prose pages like `aboutme.md`.
- Custom page sections use scoped class prefixes to avoid clobbering theme CSS: `mm-*` for shared/homepage components, `us-*` for UniScanner-specific ones. Follow this pattern for new product pages (e.g. a new page's own prefix).
- Liquid asset URLs use `{{ '/path' | relative_url }}` (or `absolute_url`), not hardcoded paths, so the site still works if served under a subpath.
- External links (GitHub, docs) use `target="_blank" rel="noopener"`.
- `.gitattributes` forces LF line endings on text files (`.html`, `.md`, `.css`, `.js`, `.yml`, `.rb`) and marks images/video/fonts as binary — don't fight this with editor-specific line-ending settings.
- Commit messages in this repo are short and lower-case (`update`, `refine`, `update price`) — match that style unless doing something that needs more explanation.

## Adding video assets

Videos are large; keep them web-friendly and always pair them with a poster
image so the page doesn't show a blank/black box before playback:

```bash
ffmpeg -y -i input.mp4 -c:v libx264 -crf 22 -preset slow -pix_fmt yuv420p -movflags +faststart assets/videos/name.mp4
ffmpeg -y -ss 00:00:03 -i assets/videos/name.mp4 -frames:v 1 -q:v 4 assets/videos/posters/name.jpg
```

Reference both via `relative_url` in the `<video>`/`<source>`/`poster` attributes, and use `preload="none"` for videos below the fold.

## Verifying changes

Since there's no test suite, validate visually:

1. `bundle exec jekyll serve --host 0.0.0.0` and confirm the build has no Liquid/YAML errors in the console.
2. `curl` the affected route to check it returns 200.
3. For layout/CSS changes, take a headless-browser screenshot (e.g. `google-chrome --headless --disable-gpu --no-sandbox --window-size=<w>,<h> --screenshot=out.png <url>`) at both desktop and mobile widths, and check light/dark rendering if colors changed.
4. Kill the dev server when done (`pkill -f "jekyll serve"` or note the job and `kill` it) — don't leave background servers running across unrelated tasks.

## Deployment

Pushing to `main` triggers `.github/workflows/ci.yml`, which builds with
`bundle exec jekyll build --future --config _config_ci.yml,_config.yml` under
`JEKYLL_ENV=production` and publishes via GitHub Pages Actions. There's no
manual deploy step — don't hand-build and commit `_site/` (it's git-ignored).
