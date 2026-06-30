# CLAUDE.md — john-broadway.github.io

John Broadway's personal site (public, static). **Jekyll on GitHub Pages**, no Actions — Pages builds on push to `main`. No Gemfile (uses the github-pages default toolchain), no JavaScript, no external fonts.

## Stack & structure
- `index.html` — home page: Jekyll front matter (layout/title/description) at top, body markup below.
- `_layouts/` — `default.html` (head/body, SEO via `jekyll-seo-tag`); `page.html` + `post.html` extend it.
- `assets/style.css` — all styles; color tokens in `:root`, sections commented (Header, Cards, Tags, etc.). `assets/zestgobble.png`, `favicon.svg`.
- `maude/`, `rys/`, `log/` — standalone subpages (each an `index.html` with `layout: page` front matter).
- `_posts/` — dated Markdown posts.
- `_config.yml` — site config; plugins: `jekyll-feed`, `jekyll-sitemap`, `jekyll-seo-tag`.
- `_site/`, `.jekyll-cache/` — build output, git-ignored. Don't edit.

## Preview & deploy
- Local preview (Docker, no Ruby needed):
  `docker run --rm -v "$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll:4 jekyll serve --watch`
- Deploy: push to `main` → GitHub Pages rebuilds (~30s). No CI workflow to wait on.
- Remote is the **public** GitHub repo. Run the pre-public-push checklist before pushing.

## Framing (public-facing copy)
- Present John as the **whole man** — independent AI researcher & infrastructure architect, 25 years of work, sovereign-by-default builder. Disability/veteran status is **engine, not headline**: it explains the why, it is not the label.
- Keep public-safe: no internal IPs, no host/container names, no private infra paths, no secrets.
- Don't position WICK relative to other things (global rule).
