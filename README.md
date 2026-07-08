# WCS Cards — West Coast Swing Beginner Lead Moves

An installable phone web app (PWA) of flip cards for the first **20 beginner West Coast Swing lead patterns** — foot-placement diagrams, hand/connection leads, timing, and a tutorial video per move. Works offline once installed.

**Live app (after you enable Pages):** https://tomenglish.github.io/WCS_Beginner/

## Files
- `index.html` — the app (self-contained: HTML, CSS, JS, and all 20 moves)
- `manifest.webmanifest` — PWA manifest (name, icons, standalone display)
- `sw.js` — service worker (offline app-shell cache)
- `icons/` — app icons (192, 512, maskable, apple-touch, favicon)
- `wcs-beginner-moves.md` — the same content as a plain reference
- `.nojekyll` — tells GitHub Pages to serve files as-is

## Deploy to GitHub Pages
From this folder (it isn't a git repo yet), in Terminal:

```bash
cd "<this folder>"
git init
git add -A
git commit -m "WCS Cards PWA"
git branch -M main
git remote add origin https://github.com/TomEnglish/WCS_Beginner.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `/root` → Save.**
Give it ~1 minute, then open **https://tomenglish.github.io/WCS_Beginner/**.

> Already have the repo cloned somewhere else? Just copy `index.html`, `manifest.webmanifest`, `sw.js`, `.nojekyll`, and the `icons/` folder into that clone, then commit and push.

## Install on your phone
Open the live URL on your phone, then:
- **iPhone (Safari):** Share → **Add to Home Screen**.
- **Android (Chrome):** tap the **Install** prompt, or ⋮ menu → **Install app / Add to Home screen**.

Launch it from the home-screen icon — it opens full-screen and works offline (video links still need a connection).

## Test locally first (optional)
Service workers need a server (not a `file://` open):

```bash
cd "<this folder>"
python3 -m http.server 8080
# then visit http://localhost:8080/
```

## Updating the app
Edit `index.html`, then bump the cache name in `sw.js` (e.g. `wcs-cards-v1` → `v2`) so phones pick up the new version, commit, and push.

---
Diagrams are schematic memory aids (US convention: lead starts on the left foot). Footwork conventions vary slightly by school — the linked videos are the authority for exact technique.
