# Hillvue Haven — www.hillvuehaven.com.au

Static website for Hillvue Haven, 46 Mustang Close, Hillvue NSW 2340.  
A Brookline SDA Property — Fully Accessible (House) and Improved Liveability (Villa).

## Stack

- Pure HTML/CSS/JS — no build step, no dependencies
- Netlify for hosting + form handling
- Google Fonts (Fraunces + DM Sans)

## Project structure

```
hillvuehaven/
├── index.html          # Full site — single page
├── images/
│   ├── hero.jpg        # Front aerial — hero section
│   ├── img01.jpg       # Open plan living (welcome section)
│   ├── img02.jpg       # Kitchen — house card
│   ├── img03.jpg       # Kitchen — villa card
│   ├── img04.jpg       # Covered alfresco (outdoor section bg)
│   ├── img05–15.jpg    # Gallery images
├── netlify.toml        # Netlify build + cache headers
├── _redirects          # SPA fallback redirect
├── robots.txt
├── sitemap.xml
└── README.md
```

## Deploy to Netlify

### Option A — Drag and drop (fastest)
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag the entire `hillvuehaven/` folder onto the deploy zone
3. Done — live in ~30 seconds

### Option B — GitHub + Netlify (recommended for ongoing edits)
1. Push this folder to a new GitHub repo:
   ```bash
   git init
   git add .
   git commit -m "Initial deploy"
   git remote add origin https://github.com/brooklinepg/hillvuehaven.git
   git push -u origin main
   ```
2. In Netlify: New site → Import from Git → select the repo
3. Build settings: leave blank (no build command, publish dir = `.`)
4. Deploy

### Custom domain
1. Netlify dashboard → Site settings → Domain management → Add custom domain
2. Enter `hillvuehaven.com.au` and `www.hillvuehaven.com.au`
3. Point DNS at your registrar:
   - `A` record: `75.2.60.5` (Netlify load balancer)
   - `CNAME` record: `www` → `[your-site-name].netlify.app`
4. Netlify auto-provisions SSL (Let's Encrypt) — usually within 5 minutes

## Contact form

The contact form uses **Netlify Forms** — no backend required.  
Form submissions appear in: Netlify dashboard → Forms → `contact`

To add email notifications: Site settings → Forms → Form notifications → Add notification → Email

## Providers

| Role | Organisation |
|------|-------------|
| Developer | Brookline Property Group |
| SDA Provider | ADAPT Housing |
| SIL Provider | Challenge Community Services |

## Contact

office@brooklinepg.com.au  
brooklinepg.com.au
