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
- Slide photography is pulled from the Envision capabilities and Streamlight decks, resized and compressed to web size (< 250 KB each), each matched to the operation it illustrates:
  - `fit-finished-unit.jpg` / `fit-upstream.jpg` — Strategic Fit cards (assembly line / component press)
  - `campus-wichita.jpg` / `campus-dallas.jpg` — Campuses slide card headers
  - `mission-workforce.jpg` — Mission slide (team member with a guide dog on the floor)
  - `opp-kitting.jpg` / `opp-print.jpg` / `opp-wiring.jpg` — Proposal tiles + modals (`fit-upstream.jpg` doubles as the Sheet Metal image)
  - `why-reliable.jpg` / `why-equipment.jpg` — Why It Works cards
  - `floor-tour.jpg` — Next Steps floor banner
