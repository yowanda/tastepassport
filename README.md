# TastePassport — Same city. Different trip.

A generic travel itinerary ignores who you are. TastePassport grounds a 1-day trip
in your taste graph via Qloo, and proves it with a side-by-side: a generic tourist
trip vs your taste-grounded trip for the SAME city.

## How it works

1. Pick 3–5 favorites (music artist, film, cuisine, brand) or tap a preset.
2. Pick a destination city (Tokyo, Paris, New York, Jakarta).
3. Generate: a 1-day itinerary (Morning / Afternoon / Evening) with a one-line
   "Why this fits" taste reasoning per stop, plus a Taste DNA strip.
4. Compare: the generic tourist trip vs your taste trip, side by side. Or compare
   two taste profiles for the same city.

## Modes

- **Demo mode (default):** curated dataset of 40 recommendations (10 per city),
  scored by taste-tag overlap. Works fully offline, no key needed.
- **Live mode:** paste your Qloo hackathon API key (stored in browser localStorage
  only, sent only to `hackathon.api.qloo.com`). Calls `GET /v2/insights` with
  `filter.type` `urn:entity:place` / `movie` / `artist` / `brand`. Any API error
  falls back silently to demo data with an honest "demo data" badge.

## Run it

Open `index.html` in any browser. Zero install, no build step.

## Live demo

https://yowanda.github.io/tastepassport/

## Built for

Qloo Agentic Hackathon (Devpost) — deadline Oct 31, 2026.

## Privacy

No user data leaves the browser except the optional Qloo API request. No tracking,
no backend, no account.
