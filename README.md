# factoid

Memorable ideas, excerpts and takeaways — from newsletters, books, seminars and other sources.

**Live site:** https://factoid.garrigai.com/

The log is `factoid.md` in this folder, and it **is** the published file (the site links it as "raw
markdown"). `~/.hermes/scripts/factoid_site.py` renders `index.html` + `issues/` from it. Ticking 🙈
on an entry removes it from the log at the next refresh — and so from the site.

## Contents

| Path | What it is |
|---|---|
| `index.html` | the log — every entry as a card, each source chip deep-linking to the exact item |
| `issues/` | one page per cited newsletter issue, original anchors preserved |
| `assets/style.css` | mobile-first (≤640px single column), light/dark, system fonts, no CDN |
| `factoid.md` | the log — published as-is; **this is the file to edit** |
| `newsletters/`, `.backups/` | the raw issue sources and the log's history — **gitignored, never published** |
| `TRAINING.md` | the interest profile that drives filtering |
| `.nojekyll` | **required** — serves files verbatim. Without it GitHub Pages runs Jekyll and renders `index.md` instead of `index.html` |

## Deploy

Push to `main`. Pages builds from the branch root, custom domain `factoid.garrigai.com`,
HTTPS enforced. The site is deliberately unindexed (`robots.txt` Disallow + `noindex`) because
`issues/` contains full newsletter text.
