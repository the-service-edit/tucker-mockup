# Tucker Casuarina — Website Build Handover

Four linked, self-contained pages. No build step, no dependencies — open `index.html` in a browser or drop the folder onto Netlify / Vercel / Cloudflare Pages.

## Files
- `index.html` — Home
- `menu.html` — Menu (food + drinks, dietary filters, sticky tabs)
- `gift-vouchers.html` — Gift vouchers
- `bookings.html` — Group bookings form

## What I fixed / added
- **Completed the homepage** — it was truncated mid-tag with no footer.
- **Shared nav + footer on every page** — visitors can now move between pages. Mobile hamburger menu included. This was the biggest gap.
- **Corrected details against the live site (tuckercasuarina.com):**
  - Instagram handle was wrong → now `@tucker.casuarina`
  - Standardised contact email → `gday@tuckercasuarina.com` (homepage had a broken Cloudflare-obfuscated link)
  - Address → T1/480 Casuarina Way, Casuarina NSW 2487
- **SEO on all pages** — title, meta description, Open Graph + Twitter cards, favicon.
- **Filled the empty gift-voucher icons** with inline SVGs (they were blank boxes).
- **Fixed menu footer font** — it called Playfair Display, which was never loaded.
- **Added an optional "occasion / notes" field** to the booking form.

## ⚠️ Verify before launch

**1. OPENING HOURS DON'T MATCH — confirm which is correct.**
Your draft files and the current live site disagree:

| | Your draft files (used in this build) | Current live site |
|---|---|---|
| Mon–Fri food | 7am–1:30pm | 7am–2pm |
| Sat–Sun coffee | 7am–2pm | 7:30am–1pm |
| Sat–Sun food | 7am–1:30pm | 7:30am–1pm |

I used the **draft** values since that's what you've been working on, but wrong hours on a café site cost real walk-ins. Confirm and I'll correct all pages. Hours appear in: each page's footer, the homepage hours bar + "Find us" block, and the menu sub-header.

**2. Two placeholder integrations (marked `TODO` in the code):**
- **Gift vouchers** → `gift-vouchers.html` points at `app.gift-it.com.au/buy/tucker`. Confirm the real provider/URL.
- **Booking form** → `bookings.html` posts to `formspree.io/f/mvzwdney`. This looks like a placeholder Formspree ID — set up Tucker's own form endpoint so enquiries actually land in the inbox. (If the POST fails it falls back to opening an email to `gday@`, but don't rely on that.)

**3. Live links confirmed working:** me&u order pickup, Instagram, Loma Coffee.

## Known limitations
- **Images hotlink from the current Squarespace CDN.** Fine short-term; download and self-host them if you move off Squarespace, or they'll break if those URLs change.
- **Reviews (4.5 / 391) are hardcoded** and will go stale. Update manually, or wire a live Google reviews widget later.
- Scope was the 4 existing pages. The live site also has About, Contact and Store — not built here. Nav links don't reference them.
