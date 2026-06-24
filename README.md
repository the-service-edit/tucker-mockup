# Tucker Casuarina — Website

Static marketing site for Tucker Casuarina (coffee & brunch, Casuarina NSW). Four self-contained HTML pages — no build step, no dependencies.

## Pages
| File | Page |
|---|---|
| `index.html` | Home |
| `menu.html` | Menu (food + drinks, dietary filters, sticky tabs) |
| `gift-vouchers.html` | Gift vouchers |
| `bookings.html` | Group bookings form |

## Run locally
Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy
Drop the folder onto any static host — Netlify, Vercel, Cloudflare Pages, or GitHub Pages (Settings → Pages → deploy from `main`).

## Before launch — see `README-tucker-build.md`
Two items need confirming: the **opening hours** (draft files disagree with the current live site) and two **placeholder integrations** (gift voucher provider URL + booking form endpoint, both marked `TODO` in the code).

## Notes
- Images currently hotlink from the existing Squarespace CDN — self-host them if moving off Squarespace.
- Reviews (4.5 / 391) are hardcoded.
