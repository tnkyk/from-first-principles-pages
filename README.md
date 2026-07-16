# From First Principles — Pages catalog

This repository hosts **all** published [From First Principles](https://tnkyk.github.io/from-first-principles-pages/) essays as a multi-article GitHub Pages site — not a single-topic repo.

Essays are authored in the sibling plugin/vault repo [`from-first-principles`](https://github.com/tnkyk/from-first-principles) (local path: `../from-first-principles`). Compose and check HTML there, then sync into this catalog.

## What’s here

- `index.html` — catalog of every published essay
- `<slug>.html` — each essay (e.g. `llm.html`)
- `assets/` — shared CSS, sims, and per-essay media

## Local plugin → this site

```bash
# in from-first-principles (authoring)
python scripts/compose_article.py --slug <slug>
python scripts/check_html.py --slug <slug>

# sync composed site into this repo (from plugin root)
python scripts/publish_to_pages.py --pages-root ../from-first-principles-pages
```

Or copy `site/*` into this repo root, commit, and push to `main`.

## Live site

GitHub Pages deploys from branch `main` at `/` (repo root).

- Catalog: https://tnkyk.github.io/from-first-principles-pages/
- Example essay: https://tnkyk.github.io/from-first-principles-pages/llm.html
