# NFC Hub (Wildcard Subdomains) — GitHub Pages

This repo supports **hundreds of client NFC pages** with **one** GitHub Pages site.

## How it works
All subdomains point to the same Pages site. The site reads the hostname (subdomain) and loads:

- `sam.card.yourdomain.com` → `/data/clients/sam.json`

## Client data
- Client JSON: `/data/clients/{slug}.json`
- Client vCard: `/vcards/{slug}.vcf`
- Client logos (recommended): `/assets/logos/{slug}.jpg` (create this folder if you want)

## Admin (foundation)
Open `/admin/` to generate JSON + vCard (copy/paste into the repo files).

## GitHub Pages
This repo includes `.github/workflows/pages.yml` to deploy Pages from `main` via GitHub Actions.

## Custom domain
Set your Pages custom domain to:
- `card.crestedcritters.com`

Then add DNS records at your provider:
- CNAME `card` → `coxusw.github.io`
- CNAME `*.card` → `coxusw.github.io`

Messaging apps cache previews; use `?v=2` when sharing if you update images.
