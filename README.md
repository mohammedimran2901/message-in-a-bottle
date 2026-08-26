# Message in a Bottle 🌊

*Let the tide decide.*

A slow-messaging web app prototype. Write a message, cast it into the ocean,
and watch your bottle drift across the world along simulated currents for days
or months — until it washes ashore for a stranger. Meanwhile, strangers'
bottles occasionally wash up on **your shore**.

Inspired by the deliberate-slowness philosophy of apps like Carrier Pidge:
we spent a decade making messages instant. This app makes you wait on purpose.

## Features

- **Cast a bottle** — write a message (280 chars) and launch it from one of six
  ports around the world
- **Procedural ocean currents** — a smooth vector field of gyres and swirls
  carries each bottle on a unique, watchable journey across a dark map
- **Time-lapse drift** — 72 simulated hours pass per real second, so a
  months-long voyage plays out in minutes
- **The Shore** — your inbox: bottles the tide brings you from strangers.
  Read them, or toss them back into the sea
- **Persistence** — your bottles survive reloads via `localStorage`

## Run it

No build step, no dependencies to install — it's a single HTML file.

```bash
cd message-in-a-bottle
python3 -m http.server 8737
# open http://localhost:8737
```

(Or just open `index.html` directly in a browser.)

## Tech

- Vanilla HTML/CSS/JS, single file
- [Leaflet](https://leafletjs.com/) + CartoDB dark basemap
- Cormorant Garamond + Jost (Google Fonts)
- Procedural current simulation (value noise + gyre rotation)

## Roadmap ideas

- Real ocean current data (NOAA)
- A tiny backend so bottles truly travel between users
- Push notifications when a bottle washes ashore
- Reply threads, rare "message from the past" events
