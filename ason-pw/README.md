# Ason.pw

Separate personal-brand site (SEO target: searches for the first name "Ason"), deployed as its own Worker (`ason-pw`), distinct from `asonpeikoff-com`. Adapted from the main site's `public/` with its own title/meta/canonical and a short "about the name" paragraph so it doesn't read as duplicate content to search engines.

## Deploy

No Cloudflare Workers Build is wired up for this subdirectory yet (the repo's existing Build trigger only deploys the root `wrangler.toml`/`asonpeikoff-com`). Until a second Build trigger is added in the Cloudflare dashboard for this path, deploy manually:

```bash
cd ason-pw
npx wrangler deploy
```
