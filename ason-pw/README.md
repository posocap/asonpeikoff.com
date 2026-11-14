# ason.pw

Placeholder "coming soon" page for ason.pw, deployed as its own Worker (`ason-pw`), distinct from `asonpeikoff-com`. Static assets in `public/`, plus a small Worker script:

- `index.html` — the page (black background, white text; no external fonts, scripts or trackers). Carries the title, description, canonical, Open Graph/Twitter tags and WebSite JSON-LD.
- `404.html` — served with a 404 status for unknown paths (`not_found_handling = "404-page"`); `noindex`.
- `_headers` — security headers (CSP, HSTS, nosniff, frame and referrer policy) for every asset.
- `favicon.svg`, `robots.txt`, `sitemap.xml`

`src/index.js` runs in front of the assets and does two things:

- 301-redirects `http://` and `www.ason.pw` requests to `https://ason.pw` in a single hop, so only one version of each URL exists.
- serves the 1200×630 share image at `/og.png` (stored as base64 in `src/og-image.js`).

## Deploy

No Cloudflare Workers Build is wired up for this subdirectory yet (the repo's existing Build trigger only deploys the root `wrangler.toml`/`asonpeikoff-com`). Until a second Build trigger is added in the Cloudflare dashboard for this path, deploy manually:

```bash
cd ason-pw
npx wrangler deploy
```
