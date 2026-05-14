# CS2 Skin Wishlist

Minimal static website for a CS2 skins wishlist.

## What it does

- Loads CS2 skin data from a public JSON source.
- Lets a user search and filter skins.
- Lets a user add skins to a local wishlist.
- Enforces max 5 skins per weapon.
- Saves wishlist in `localStorage`.
- Exports/imports wishlist as JSON.
- Works on GitHub Pages.

## Data source

This MVP uses:

```txt
https://raw.githubusercontent.com/ByMykel/CSGO-API/main/public/api/en/skins.json
```

Reason: it works from a static GitHub Pages frontend without exposing any private API key.

## Why not direct CSGOSKINS.GG API in frontend?

CSGOSKINS.GG has an official API, but it requires authentication and an active subscription. Do not put an API key into public frontend code on GitHub Pages. Anyone can copy it from DevTools.

Correct architecture for CSGOSKINS.GG API:

```txt
Browser → your backend/proxy → CSGOSKINS.GG API
```

For a simple static MVP, use public data without private keys.

## Run locally

Just open `index.html` in a browser.

Better:

```bash
python -m http.server 8000
```

Then open:

```txt
http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a new GitHub repository.
2. Upload `index.html`, `README.md`, `privacy.md`.
3. Go to repository `Settings`.
4. Go to `Pages`.
5. Source: `Deploy from a branch`.
6. Branch: `main`.
7. Folder: `/root`.
8. Save.

## Privacy

No login. No tracking. No analytics. Wishlist is saved in the user's browser via `localStorage`.
