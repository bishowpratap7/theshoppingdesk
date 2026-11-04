# The Shopping Desk 🛍️

Deal hunters across the internet post hundreds of finds a day; this desk gathers the ones a smart shopper would actually send a friend: gifts for her, beauty and self-care steals, cozy home picks, and the under-$25 treasures that sell out first. Refreshed around the clock — when it's gone, it's gone.

- Live page: https://bishowpratap7.github.io/theshoppingdesk/
- Run by **Bishow Pandey** — follow on X: https://x.com/bishowppandey
- Sister desks: The Dev Desk (developer news), Scroll Patrol (trending posts & memes), The World Desk (world news), The Stock Desk (stock deep dives), plus The Shopping Desk, The Cozy Desk, The Foodie Desk and The Style Desk

## What's on the desk
- **🔥 Today's Best Finds**
- **💸 Treasures Under $25**
- **💄 Beauty & Self-Care Steals**
- **🏠 Home & Cozy Picks**

Today's best finds, under-$25 treasures, beauty & self-care steals, and home & cozy picks — gathered from public community deal feeds (Slickdeals).

## How it works
- `tools/scan.py` reads the public sources above (no API keys), writes `data/feed.json`, bakes an SEO summary of every item into `index.html`, and regenerates `feed.xml` and `sitemap.xml`. If a source fails, the desk keeps its last good data and flags it stale.
- A GitHub Actions loop (`.github/workflows/loop-scan.yml`) re-runs the scanner every 30 minutes around the clock and commits only when something changed; each loop job hands off to its successor, so the desk stays current on its own.
- The page is a single static file — no backend, no build step, no tracking.

## Repos
- `theshoppingdesk` (public) — the live site, served by GitHub Pages
- `the-shopping-desk` (private) — the archive twin

## Good to know
Prices and availability change fast and were accurate only when the deal was posted. The Shopping Desk does not sell products and cannot honor prices; confirm everything at the store. Deal posts belong to their communities and stores — every card links to the original.
