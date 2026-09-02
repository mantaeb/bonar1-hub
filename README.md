# bonar1.com hub

A small bilingual directory for the public `bonar1.com` properties.

## Public routes

| Route | Purpose |
|---|---|
| `/` | English hub |
| `/he/` | Hebrew hub |

## Content rule

The apex explains and routes. It does not duplicate the detailed profile, private-AI proof or psychotherapy-practice copy held on the canonical subdomains.

The initial destinations are:

- `etgar.bonar1.com`
- `ai.bonar1.com`
- `adi.bonar1.com`

`ai-build.bonar1.com` is intentionally excluded. The standalone build-story source remains available, but the current live Etgar and Private AI sites already carry its core proof.

## Local preview

```bash
python3 -m http.server 8766 --directory projects/bonar1-websites/hub-site
```

Then open `http://127.0.0.1:8766/`.

## Launch requirements

1. Publish the contents of this folder at the repository root.
2. Configure the custom domain as `bonar1.com`.
3. Point the Cloudflare apex records at the GitHub Pages apex addresses.
4. Redirect `www.bonar1.com` to `https://bonar1.com/`.
5. Enable HTTPS, submit `sitemap.xml`, request indexing for both language routes and add analytics if wanted.

## Analytics

Cloudflare Web Analytics is installed on the English, Hebrew and 404 pages with site token `67241cd43e0c4f0fb9cee03bfa8d3f15`. The footer discloses it. The page has no cookies, forms or advertising trackers.
