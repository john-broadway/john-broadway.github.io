# john-broadway.github.io

Source for [john-broadway.github.io](https://john-broadway.github.io).

Jekyll on GitHub Pages — no Actions, builds on push. Page content with front matter in `index.html`; layout chrome in `_layouts/`; styles in `assets/style.css`; site config in `_config.yml`. No external fonts, no JavaScript.

## Content

- Header with name, role, lead description
- Personal context: veteran, no team / lab / budget, 25 years of work
- "I think in analogies" — physics-of-systems framing
- **Research** card: RYS on small language models, sub-14B results
- **Projects** card: Maude for Claude
- **Values** list: AI partnership, sovereign-by-default, right-sized systems, governance-as-code
- **Buddy**: Zestgobble (rare goose)
- **Elsewhere** links: GitHub, Hugging Face, Maude for Claude

## Editing

- **Page content:** `index.html` — body markup with Jekyll front matter at the top setting layout, title, and description.
- **Styles:** `assets/style.css`. Color tokens in `:root`. Sections commented:

```
/* ── Header ─────────── */
/* ── Section headings ── */
/* ── Cards ──────────── */
/* ── Tags ───────────── */
/* ── Stats grid ─────── */
/* ── Values list ─────── */
/* ── Elsewhere row ───── */
/* ── Buddy block ─────── */
/* ── Footer ─────────── */
```

- **Layouts:** `_layouts/default.html` wraps the page (head, body, SEO tags via `jekyll-seo-tag`). `_layouts/page.html` and `_layouts/post.html` extend it.
- **Site config:** `_config.yml`.

Local preview (Docker, no Ruby install needed):

```
docker run --rm -v "$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll:4 jekyll serve --watch
```

Or skip preview — push to main; GitHub Pages deploys on push (~30s).

## License

The site content is © 2026 John Broadway. The structural HTML/CSS scaffold is yours to lift if useful.
