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


## Privacy

No login. No tracking. No analytics. Wishlist is saved in the user's browser via `localStorage`.
