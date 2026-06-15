# bosch-envision

Static, single-page proposal deck (Envision × Bosch).

## Deploy (Vercel)

No build step — it's plain HTML/CSS/JS served from the repo root.

1. Import the repo in Vercel (Framework Preset: **Other**, no build command, output = root).
2. `vercel.json` handles the rest:
   - `index.html` is served at `/`
   - clean URLs, and `/envision-bosch-2` redirects to `/`
   - cover images cached immutably for a year; HTML always revalidates

## Assets

- `cover-1.jpg … cover-5.jpg` — compressed cover-carousel photos (each < 300 KB)
- `cover-1.jpg` is preloaded; the rest lazy-load as the carousel advances
- The white Envision cover logo is inlined as base64; `Envision_PrimaryLogo_WHITE[49404].png` is its source
- `fit-finished-unit.jpg` / `fit-upstream.jpg` — Strategic Fit slide photos (resized to 1600px, < 200 KB each), sourced from the Envision capabilities and Streamlight decks
