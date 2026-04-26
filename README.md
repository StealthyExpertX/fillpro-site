# Stealthy Apps — public site

Source for [stealthyapps.com](https://stealthyapps.com), the public site for **Stealthy Apps** — a one-person indie studio (Karl) building small, private browser extensions.

The site is intentionally static: plain HTML + CSS, one tiny mailto script, no framework, no analytics, no build step.

## Structure

```
/                  # Stealthy Apps portfolio homepage
/about.html        # About Karl
/apps/fillpro/     # FillPro product page
  index.html       # product overview, features, pricing, FAQ
  privacy.html     # FillPro privacy policy (linked from CWS listing)
  support.html     # FillPro support + contact form
  changelog.html   # FillPro release notes
/assets/           # shared logo + brand assets
/styles.css        # shared visual system
/contact.js        # tiny mailto-based contact flow
/sitemap.xml       # SEO
/robots.txt        # SEO + AI crawler allowlist
/llms.txt          # AI-crawler summary (ChatGPT, Gemini, Perplexity, Claude)
/humans.txt        # who built this
/CNAME             # custom domain (stealthyapps.com)
/404.html          # not-found page
```

Old top-level paths (`/privacy-policy.html`, `/support.html`, `/changelog.html`) redirect to `/apps/fillpro/*` to preserve any existing inbound links.

## Hosting

GitHub Pages, served from the `main` branch root. The `CNAME` file pins the custom domain `stealthyapps.com`.

### DNS setup (one-time, in your domain registrar)

For an apex domain (`stealthyapps.com`), add four A records pointing to GitHub Pages:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

For the `www` subdomain, add a CNAME pointing to `stealthyexpertx.github.io.`

After DNS propagates, GitHub Pages will auto-provision a Let's Encrypt cert.

### GitHub Pages settings

Repo → Settings → Pages:
- Source: **Deploy from a branch**
- Branch: `main` / `/` (root)
- Custom domain: `stealthyapps.com`
- Enforce HTTPS: ✅

## SEO + AI search

- Schema.org JSON-LD on every page (`Person`, `Organization`, `WebSite`, `SoftwareApplication`, `FAQPage`, `BreadcrumbList`, `PrivacyPolicy`).
- Open Graph + Twitter cards on every page.
- Canonical URLs on every page.
- `sitemap.xml`, `robots.txt`, and `llms.txt` for traditional + AI crawlers (GPTBot, Google-Extended, PerplexityBot, ClaudeBot, anthropic-ai, CCBot).
- Question-format H2s on FAQ sections (LLMs prefer those).

## Privacy posture (whole site)

- No analytics, no Google Tag Manager, no Meta Pixel.
- No third-party fonts (uses system UI stack).
- Strict CSP on the FillPro pages.
- `referrer: no-referrer` on every page.

## License

The site source in this repo is © Stealthy Apps. Content is not open source. Inspecting and learning from the markup is fine.
