# ason.pw

Placeholder "coming soon" page for ason.pw, deployed as its own Worker (`ason-pw`), distinct from `asonpeikoff-com`. Static assets only, served from `public/`:

- `index.html` — the page (black background, white text; no external fonts, scripts, links, or trackers)
- `404.html` — served for unknown paths (`not_found_handling = "404-page"` in `wrangler.toml`)
- `favicon.svg`, `robots.txt`, `sitemap.xml`

## Deploy

No Cloudflare Workers Build is wired up for this subdirectory yet (the repo's existing Build trigger only deploys the root `wrangler.toml`/`asonpeikoff-com`). Until a second Build trigger is added in the Cloudflare dashboard for this path, deploy manually:

```bash
cd ason-pw
npx wrangler deploy
```
