[README.md](https://github.com/user-attachments/files/26436416/README.md)
# mrlongwell.com — GitHub Pages Migration

This repository hosts the replacement for [www.mrlongwell.com](https://www.mrlongwell.com), a career and technical education site for Lenape Technical School. The site is being built here first; the domain will be repointed once the migration is complete.

Live preview: **https://eric15774.github.io**

---

## Site Structure

```
/
├── index.html          Home page — links to all course/resource pages
├── style.css           Shared stylesheet (all pages reference this)
├── cdl/
│   └── index.html      CDL course page
├── robotics/
│   └── index.html      Robotics course page (placeholder)
└── links/
    └── index.html      Useful links (weather, news, education, etc.)
```

---

## Page Status

| Page | Status | Notes |
|---|---|---|
| Home | ✅ Complete | Needs review |
| CDL | ✅ Complete | Migrated from Google Sites; needs review |
| Robotics | 🔲 Placeholder | Content to be added |
| Links | ✅ Complete | Migrated from Google Sites; links may need culling |

### Not migrated
The following pages from the original site were intentionally left behind:

- **CDL Permit Quiz** — to be reconsidered separately
- **CDL Links** — consolidated into the main CDL page
- **PrinTec** — course being retired after this academic year
- **Extra Credit** — not needed on the new site

---

## Design

- Clean, minimal — white background, simple sticky navigation
- Fonts: DM Serif Display (headings) + DM Sans (body) via Google Fonts
- No frameworks or dependencies beyond the stylesheet and Google Fonts
- All pages share `style.css` at the root

---

## Domain Cutover

When the site is ready to go live at `www.mrlongwell.com`:

1. Add a file named `CNAME` to the root of this repo containing:
   ```
   www.mrlongwell.com
   ```
2. At your domain registrar, update the DNS records:
   - Add a `CNAME` record pointing `www` → `eric15774.github.io`
   - Or use `A` records pointing to GitHub's IPs if you need the apex domain (`mrlongwell.com` without `www`)
3. In the GitHub repo settings under **Pages**, confirm the custom domain is set and wait for the SSL certificate to provision (usually a few minutes).

GitHub's official guide: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
