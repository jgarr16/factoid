# newsletters

Web copy of the newsletter tidbits log — the things worth acting on from the newsletters
that land in the inbox, each one deep-linking to the exact item in the archived issue.

**Live site:** https://jgarr16.github.io/newsletters/ (enable GitHub Pages → Deploy from
branch → `main` / root, then it's up).

## What's here

| Path | What it is |
|---|---|
| `index.html` | the tidbits log — 66 entries, newest first, filterable by theme and text |
| `issues/` | one page per archived newsletter issue cited by the log (`issues/index.html` browses them) |
| `tidbits.md` | the raw log markdown, for local/Typora reading |
| `assets/style.css` | mobile-first, light/dark, system fonts only (no CDN) |
| `TRAINING.md` | standing interest profile that drives what gets kept |
| `.nojekyll` | serve files verbatim (the site is pre-built HTML) |
| `robots.txt` | `Disallow: /` — the archive holds full newsletter text, so it stays unindexed |

Reading order: source "chips" on each entry link straight to the item inside the issue page.
Tick a `📌` checkbox in the **local** copy of the log to have an Apple Reminder created for
that entry — that affordance is local-only and does nothing on the web.

## Rebuilding

```bash
~/.hermes/hermes-agent/venv/bin/python ~/.hermes/scripts/newsletters_site.py
```

Reads `~/newsletters/2026-09-18_interesting_tidbits.md` + the issues it cites, writes the
pages here. The builder warns if any chip's `#anchor` is missing from its issue page — the
fix is `tidbit_insert.py --refresh` (re-injects anchors), then rebuild. Re-converting an
issue from email drops its anchors, so run the refresh after any conversion.

## History

Earlier iteration of this repo stored a hand-curated `index.md` + `log/` entries; the
pipeline now generates the whole site from the tidbits log, so those are legacy.
