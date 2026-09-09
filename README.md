# Lavoc Limited — website

Single-page static site. No build step, no dependencies.

## Files

- `index.html` — the whole site (HTML + CSS + a one-line script for the copyright year)
- `favicon.svg` — tab icon
- `.nojekyll` — tells GitHub Pages to serve files as-is

## Before publishing

Open `index.html` and search for `EDIT`:

1. Contact email (`hello@lavoc.ie`, appears twice)
2. Company registration number and registered address in the footer

## Deploy to GitHub Pages

1. Create a repo (e.g. `lavoc-site`) and push these files to the `main` branch.
2. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
3. The site is live at `https://<username>.github.io/lavoc-site/` within a minute or two.

## Custom domain (optional)

1. Add a file named `CNAME` containing only the domain, e.g. `lavoc.ie` or `www.lavoc.ie`.
2. At your DNS provider, add a CNAME record pointing `www` to `<username>.github.io`, and for the apex domain add A records for GitHub's IPs (listed in the GitHub Pages docs under "Managing a custom domain").
3. Back in **Settings → Pages**, enter the domain and tick **Enforce HTTPS** once the certificate is issued.

## Editing

Everything is in `index.html`. Colours and spacing are CSS variables at the top of the `<style>` block. The layer-line effect on the wordmark is a CSS mask; the "print" animation is a single `clip-path` keyframe and is disabled for users with reduced-motion enabled.
