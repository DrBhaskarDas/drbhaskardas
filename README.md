# drbhaskardas.com

Personal/professional site for Dr. Bhaskar Das — Interventional Radiologist. Plain HTML/CSS/JS, no build step, deployed via GitHub Pages.

## Structure

```
index.html       Home — hero, link tiles, about, IR overview, contact
learning.html     Learning Resources — Dr. Bhaskar's IR Notes, links, teaching
research.html      Research — ongoing Y90 TARE study, publications, awards
journey.html        The Journey — career timeline + photo gallery
assets/css/style.css  design system incl. light/dark themes
assets/js/main.js     nav, theme toggle, scroll reveal
assets/img/           optimized photos + favicon.svg
CNAME                 custom domain for GitHub Pages
sitemap.xml, robots.txt   SEO
```

## Publish to GitHub Pages

1. Create a new **public** repo on GitHub named exactly `DrBhaskarDas.github.io`.
2. From this folder:
   ```
   git remote add origin https://github.com/DrBhaskarDas/DrBhaskarDas.github.io.git
   git branch -M main
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main` / `root`. Save.
4. Still on **Settings → Pages**, under "Custom domain" enter `drbhaskardas.com` and save (this confirms the `CNAME` file). Wait for the DNS check to go green, then tick **Enforce HTTPS**.

## Point the GoDaddy domain at GitHub Pages

In GoDaddy → *My Products → DNS* for `drbhaskardas.com`, set:

**A records** (apex domain, host `@`) — add all four, delete any existing `@` A record first:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME record** (so `www.drbhaskardas.com` also works):
```
Host: www
Points to: drbhaskardas.com
```

DNS changes can take anywhere from a few minutes to a few hours to propagate.

## Editing content later

Everything is static — open any `.html` file and edit the text directly, or swap files in `assets/img/`. No build step, no dependencies.

## Known TODOs

- Radicles is intentionally unmentioned on the site while it's under construction; reintroduce it on `learning.html` when ready.
- Hero/gallery photos were sourced from WhatsApp-compressed originals; swap in higher-resolution versions in `assets/img/` if better source files become available.
- After going live, submit `sitemap.xml` to Google Search Console to speed up indexing.
