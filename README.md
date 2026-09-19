# factoid

Memorable ideas, excerpts and takeaways — from newsletters, books, seminars and other sources.

**Live site:** https://factoid.garrigai.com/

Built by `~/.hermes/scripts/factoid_site.py` from the tidbits log at
`~/newsletters/2026-09-18_interesting_tidbits.md`. The source archive keeps the older
"newsletters" name (that folder really is the newsletters); this repo is the published output.

## Contents

| Path | What it is |
|---|---|
| `index.html` | the log — every entry as a card, each source chip deep-linking to the exact item |
| `issues/` | one page per cited newsletter issue, original anchors preserved |
| `assets/style.css` | mobile-first (≤640px single column), light/dark, system fonts, no CDN |
| `tidbits.md` | the raw log, for local / Typora use |
| `TRAINING.md` | the interest profile that drives filtering |
| `.nojekyll` | **required** — serves files verbatim. Without it GitHub Pages runs Jekyll and renders `index.md` instead of `index.html` |

## Deploy

Push to `main`. Pages builds from the branch root, custom domain `factoid.garrigai.com`,
HTTPS enforced. The site is deliberately unindexed (`robots.txt` Disallow + `noindex`) because
`issues/` contains full newsletter text.
