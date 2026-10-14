# TastePassport — Devpost write-up

## Elevator pitch

Same city. Different trip. TastePassport turns your taste — the artists, films,
foods and brands you love — into a 1-day travel itinerary grounded in Qloo's taste
graph, and proves it side by side against the generic tourist trip.

## Inspiration

Two friends land in the same city with the same guidebook and get the same boring
day. One loves indie film and ramen; the other lives for street food and hip-hop.
The guidebook serves neither. Travel recommendations are generic because they know
nothing about who you are. Qloo's taste graph knows what people love — we built the
trip planner that finally uses it.

## What it does

Pick 3–5 favorites (music artist, film, cuisine, brand) or tap a preset like
"Indie film lover" or "Street food hunter", pick a city, and TastePassport builds
a 1-day itinerary: Morning / Afternoon / Evening, each stop with a one-line "Why
this fits" taste reasoning and its Qloo entity type. A Taste DNA strip shows the
inferred tags behind the plan. Then the killer demo: the generic tourist trip vs
your taste trip, side by side, for the same city — or two taste profiles compared
head to head. The same city gives two completely different days, because taste
travels.

## How we built it

Single-file HTML + CSS + vanilla JavaScript (zero install, GitHub Pages).
Demo mode runs on a curated dataset of 40 recommendations scored by taste-tag
overlap, so judges can try it with no key. Live mode calls Qloo's Insights API
(`GET /v2/insights`, `filter.type` place / movie / artist / brand) with a
user-supplied hackathon key stored only in browser localStorage. Any API error
falls back silently to demo data with an honest "demo data" badge — the demo
never breaks.

## Challenges we ran into

Qloo's Insights API silently ignores parameters that are not valid for the chosen
`filter.type`, returning an empty list with no error. We learned to validate every
parameter against the entity-type guide and to treat the curated demo dataset as
the reliability backbone, not a placeholder.

## Accomplishments that we're proud of

The side-by-side comparison makes the value of cultural intelligence visible in
one scroll: same city, different taste, different trip. And the app never fails
the demo — live Qloo data when the key is present, honest demo data otherwise.

## What we learned

Cultural intelligence is the difference between "technically functional" and
"actually good." A recommendation engine that knows what you love does not just
rank better — it changes what a day in a new city feels like.

## What's next for TastePassport

More cities and multi-day trips, group mode (merge a whole travel party's tastes
into one plan), and saved taste passports you can reuse across trips.

## Built with

HTML, CSS, JavaScript, Qloo Taste AI API
