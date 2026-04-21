# Zeilen met Ellen en Walter — Saronic Gulf June 2025

Sailing trip website for Walter, Ellen, Fleur & Sam.

## Setup

### 1. Enable GitHub Pages
Go to **Settings → Pages → Source** and select `main` branch, root folder. GitHub will serve the site at:
`https://[your-username].github.io/sailing-june-2025`

### 2. Add Google Photos album
1. On your iPhone: open Google Photos → tap your avatar → **Shared albums → Create shared album**
2. Name it "Zeilen June 2025" and share the link with the crew
3. In `index.html`, replace `GOOGLE_PHOTOS_LINK_HERE` with your actual shared album URL
4. Commit and push

### 3. Custom subdomain (sailing.silvertownconsulting.com)

**Step 1 — Add CNAME file to repo**
Create a file called `CNAME` (no extension) in the root of the repo containing:
```
sailing.silvertownconsulting.com
```

**Step 2 — Add DNS record**
In your domain registrar (wherever silvertownconsulting.com is managed), add:
```
Type:  CNAME
Name:  sailing
Value: [your-github-username].github.io
TTL:   3600
```

**Step 3 — Enable custom domain in GitHub**
Go to **Settings → Pages → Custom domain**, enter `sailing.silvertownconsulting.com` and save. GitHub will verify DNS (can take up to 30 min). Tick "Enforce HTTPS".

Done — the site will be live at `https://sailing.silvertownconsulting.com`

## Files
- `index.html` — main page (itinerary, route, photos section)
- `style.css` — all styling
- `script.js` — nav scroll + fade-in animations
- `CNAME` — custom domain (add this manually)

## Updating photos
No code needed. Add photos to the shared Google Photos album from any iPhone — they appear instantly for everyone via the shared album link.
