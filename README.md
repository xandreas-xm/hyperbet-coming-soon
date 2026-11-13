# hyperbet.cc coming-soon page

A one-page "coming soon" site for hyperbet.cc, the domain the new Hyperbet platform (built by GeniusBet on Genius360)
will launch on. Static HTML, no build step: `index.html` plus `assets/`. Served by GitHub Pages from `main`, with the
custom domain set by the `CNAME` file.

## DNS (set by whoever runs the hyperbet.cc Cloudflare zone)

| Type | Name | Value | Proxy |
|---|---|---|---|
| A | @ | 185.199.108.153 | DNS only (grey cloud) |
| A | @ | 185.199.109.153 | DNS only |
| A | @ | 185.199.110.153 | DNS only |
| A | @ | 185.199.111.153 | DNS only |
| CNAME | www | xandreas-xm.github.io | DNS only |

Any existing A/AAAA/CNAME records on `@` and `www`, and the redirect rule that sends hyperbet.cc to playhyperbet.com,
have to go, or they win over these. DNS only matters: GitHub can only issue the HTTPS certificate when it sees its own
IPs. Once the certificate is issued, the zone may switch the records to proxied with SSL mode "Full".

## Why it looks like this

- **GitHub Pages, not the platform host.** The page has to exist before the platform does, and it is the only host we
  can deploy to ourselves; when the platform goes live, the zone's records move to GeniusBet's host and this repo can
  be archived.
- **No link to playhyperbet.com** (operator, 2026-11-13): the page stands on its own for the new platform; the only
  way out is the Telegram community.

## Changing it

Edit `index.html`, push to `main`; Pages redeploys in about a minute.
