# 🌿 DIY Yard Pro

> Professional landscaping & hardscaping tutorials for homeowners who want to do it right.

**Live site:** [diy-yard-pro.com](https://diy-yard-pro.com)  
**Deploy:** Netlify (auto-deploy on push to `main`)  
**Stack:** HTML · CSS · Vanilla JS — no frameworks, no build step

---

## 📁 Project Structure

```
diy-yard-pro/
├── index.html                 # Homepage
├── CLAUDE.md                  # AI assistant context (read this first)
├── README.md                  # This file
│
├── assets/
│   ├── css/
│   │   ├── main.css           # Homepage styles
│   │   └── article.css        # Shared styles for ALL articles
│   ├── js/
│   │   └── main.js
│   └── images/
│
├── articles/                  # Blog posts (HTML files)
│   ├── stone-patio-construction.html
│   ├── low-maintenance-landscaping.html
│   ├── budget-backyard-makeover.html
│   ├── garden-walkway-construction.html
│   ├── raised-garden-beds.html
│   ├── outdoor-lighting-design.html
│   ├── retaining-wall-construction.html
│   ├── lawn-care-basics.html
│   ├── garden-bed-edging.html
│   └── complete-mulching-guide.html
│
├── privacy-policy.html
├── terms-of-service.html
├── sitemap.xml
├── robots.txt
├── netlify.toml
└── _redirects
```

---

## 🚀 Deploy

This site deploys automatically via Netlify when you push to `main`.

```bash
git add .
git commit -m "your message here"
git push
# Netlify picks it up — live in ~60 seconds
```

To preview locally, just open `index.html` in your browser. No server needed.

---

## ✍️ Adding a New Article

1. Copy `articles/stone-patio-construction.html` — it's the master template
2. Update the `<head>`: title, meta description, canonical URL, Open Graph tags, Schema.org JSON-LD
3. Write your content using the existing component classes (`.step-card`, `.tip-box`, `.warning-box`, `.product-card`)
4. Add affiliate product links with `rel="nofollow sponsored noopener"`
5. Add the new article to `sitemap.xml`
6. Add it to the article grid in `index.html`
7. Add it to the "Related Articles" section of at least 2 existing articles

**Never write CSS inline in article files.** All styles go in `assets/css/article.css`.

---

## 💰 Monetization

| Channel | Status | ID / Account |
|---|---|---|
| Google AdSense | ✅ Active | `ca-pub-2556661491647206` |
| Google Analytics 4 | ✅ Active | `G-K663C48D8T` |
| Amazon Associates | ⚠️ Links pending | ID: `theart198604-20` — links not yet added |
| Home Depot Affiliate | ⚠️ Pending | Setup needed |
| MailerLite Newsletter | ✅ Active | Signup forms embedded |

---

## 🎨 Design Tokens

```css
--primary:   #1a5f3a   /* Dark green */
--secondary: #2d8659   /* Mid green */
--accent:    #ff6b35   /* Orange — CTAs */
--text-dark: #1f2937
--radius:    12px
```

Font: **Inter** (Google Fonts)

---

## 📋 Current Roadmap

- [ ] Activate Amazon affiliate links across all 10 articles
- [ ] Audit articles 7–10 for design consistency with articles 1–6
- [ ] Connect social media (YouTube, Instagram, Pinterest)
- [ ] "About" page with Arturo's professional background
- [ ] Category pages (Patios, Walkways, Lighting, Lawn Care…)
- [ ] YouTube channel — each article is a video script
- [ ] Performance optimization (WebP images, CSS minification)

---

## ⚠️ Important Rules

- Do **not** add CSS inline to article files
- Do **not** remove affiliate disclosure banners (legally required)
- Do **not** remove Analytics or AdSense code
- Always use `rel="nofollow sponsored noopener"` on affiliate links
- Keep the green/orange color palette — it's the brand identity

---

*Built with ❤️ and 10+ years of field experience.*