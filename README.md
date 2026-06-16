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

- `cover-1.jpg … cover-5.jpg` — compressed photo-carousel frames (each < 300 KB), shared by the home cover and the Contact ("Let's Build It Together") hero. `cover-1.jpg` (Wichita campus) is preloaded; the rest lazy-load as the carousel advances. Any `.cover-carousel` on the page rolls independently.
- The white Envision cover logo is inlined as base64; `Envision_PrimaryLogo_WHITE[49404].png` is its source
- Slide photography is pulled from the Envision capabilities and Streamlight decks, resized and compressed to web size (< 250 KB each), each matched to what the slide shows:
  - `campus-map-wichita.jpg` / `campus-map-dallas.jpg` — Campuses slide card headers (campus photo + location map, from the capabilities deck)
  - `mission-child.jpg` / `mission-walk.jpg` — Mission band, flanking the quote (child development center / White Cane Day Walk, from the capabilities deck)
  - `opp-kitting.jpg` / `opp-print.jpg` / `opp-wiring.jpg` / `fit-upstream.jpg` — Proposal tiles + modals (`fit-upstream.jpg` is the Sheet Metal / press image)
  - `why-reliable.jpg` / `why-equipment.jpg` — Why It Works cards
  - `floor-tour.jpg` — Next Steps floor banner

The Capabilities & Services slide is text-only: each tile shows its title, and the overview paragraph (sourced from the capabilities deck's modal summaries) is revealed on hover/focus — no pop-up.
