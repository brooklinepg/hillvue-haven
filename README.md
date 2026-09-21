# Hillvue Haven — CMS Site

Eleventy static site with Decap CMS for content editing.

## Setup

```bash
npm install
npm start        # dev server at localhost:8080
npm run build    # builds to _site/
```

## CMS Access

After deploying to Netlify:
1. Enable **Netlify Identity** in Site Settings → Identity
2. Enable **Git Gateway** in Identity → Services
3. Invite yourself as a user
4. Visit `yoursite.netlify.app/admin` to log in and edit content

## Content

All editable content lives in `_data/content.json`. The CMS edits this file directly via Git Gateway — every save triggers a Netlify rebuild and redeploy (~30 seconds).

## Deploy

Push this repo to GitHub, connect to Netlify:
- Build command: `npx @11ty/eleventy`
- Publish directory: `_site`
- Node version: 18

DNS:
- A record → 75.2.60.5
- CNAME www → [yoursite].netlify.app
