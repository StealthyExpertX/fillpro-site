# FillPro Public Site

![FillPro logo](assets/fillpro-logo.svg)

Public GitHub Pages site for FillPro.

This repo only contains the public-facing Pages surface used for the Chrome Web Store listing and direct support links. It stays intentionally static: plain HTML, plain CSS, one small contact script, no framework, no analytics, and no build step.

## What this repo includes

- `index.html` - product landing page
- `support.html` - setup help, troubleshooting, local-data guidance, and contact form
- `privacy-policy.html` - privacy policy and permission summary
- `changelog.html` - public release notes
- `styles.css` - shared visual system for the whole site
- `contact.js` - tiny mailto-based contact flow
- `assets/fillpro-logo.svg` - shared FillPro logo asset

## Live pages

- Landing: https://stealthyexpertx.github.io/fillpro-site/
- Support: https://stealthyexpertx.github.io/fillpro-site/support.html
- Privacy policy: https://stealthyexpertx.github.io/fillpro-site/privacy-policy.html
- Changelog: https://stealthyexpertx.github.io/fillpro-site/changelog.html

## Why this site is static

- Faster load times and fewer moving parts
- Easier policy and privacy review
- No extra backend or client-side tracking surface
- Easy to audit for accuracy against the actual extension

## Accuracy rules for this repo

- Keep product claims narrow and truthful.
- Do not imply FillPro bypasses CAPTCHA, anti-bot systems, login walls, or blocked embedded frames.
- Keep privacy language aligned with the shipped extension behavior.
- Remember that free-use profile data stays local to the extension on the user's device.
- The contact form opens a local email draft. It does not submit to a server.

## Local preview

Open `index.html` directly in a browser for a quick check, or serve the folder with any static server if you want proper local URLs.

## Deployment

The included GitHub Actions workflow publishes the repository root to GitHub Pages.

## Maintenance notes

- Keep relative links for internal navigation.
- Keep the shared branding, palette, and copy consistent across all pages.
- If the extension behavior changes, update the privacy, support, and changelog pages in the same pass.
