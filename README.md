# factoid

Memorable ideas, excerpts and takeaways — from newsletters, books, seminars and other sources.

**Live site:** https://factoid.garrigai.com/

The log is `~/repo/factoid/factoid.md`. `~/.hermes/scripts/factoid_site.py` renders this repo from
it: `index.html` + `issues/`, plus `factoid-web.md` — the copy the web serves (entries marked 🙈 are
left out of that copy, never out of the log).

## Contents

| Path | What it is |
|---|---|
| `index.html` | the log — every entry as a card, each source chip deep-linking to the exact item |
| `issues/` | one page per cited newsletter issue, original anchors preserved |
| `assets/style.css` | mobile-first (≤640px single column), light/dark, system fonts, no CDN |
| `factoid-web.md` | the published copy of the log, for local / Typora use from the web |
| `factoid.md`, `newsletters/`, `.backups/` | the working log, its raw issue sources and its history — **gitignored, never published** |
| `TRAINING.md` | the interest profile that drives filtering |
| `.nojekyll` | **required** — serves files verbatim. Without it GitHub Pages runs Jekyll and renders `index.md` instead of `index.html` |

## Deploy

Push to `main`. Pages builds from the branch root, custom domain `factoid.garrigai.com`,
HTTPS enforced. The site is deliberately unindexed (`robots.txt` Disallow + `noindex`) because
`issues/` contains full newsletter text.
