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

1. [x] Publish the contents of this folder at the repository root.
2. [x] Configure the custom domain as `bonar1.com`.
3. [x] Point the Cloudflare apex records at the GitHub Pages apex addresses.
4. [x] Route `www.bonar1.com` to the Pages site and redirect it to `https://bonar1.com/`.
5. [x] Serve both hostnames through Cloudflare's active universal HTTPS certificate.
6. [ ] Submit `sitemap.xml` and request indexing for both language routes.

## Hosting state

- Public repository: `mantaeb/bonar1-hub`.
- GitHub Pages custom domain: `bonar1.com`.
- Cloudflare apex A/AAAA records and the `www` CNAME are proxied.
- Cloudflare SSL mode is Full, its universal certificate covers `bonar1.com` and `*.bonar1.com`, and Always Use HTTPS is on.
- GitHub's own custom-domain certificate had not attached after roughly 30 minutes on 2026-09-03. This does not block visitors because Cloudflare terminates valid HTTPS at the edge and uses encrypted Full-mode transport to GitHub.
- If the records are ever changed back to DNS-only, verify GitHub's certificate first and enable GitHub Pages HTTPS in the same operation.

## Analytics

Cloudflare Web Analytics is installed on the English, Hebrew and 404 pages with site token `67241cd43e0c4f0fb9cee03bfa8d3f15`. The footer discloses it. The page has no cookies, forms or advertising trackers.
