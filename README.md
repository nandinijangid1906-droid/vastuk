# VASTUK — Vastu-Guided Floor Plan Studio

A single-page, client-side web app that generates a Vastu Shastra–guided
floor plan from a short project brief: plot size, facing, bedrooms,
bathrooms, kitchen type, staircase preference, parking/garden/pooja room,
budget tier, and elevation style.

No backend, no database, no API key. Everything — the room-placement
rule engine, the 2D blueprint, the 3D dollhouse massing model, and the
compliance report — runs entirely in the visitor's browser off a single
HTML file.

## What's inside

- `vastuk.html` — the entire app (HTML + CSS + JS in one file).

## Run it locally

Just double-click `vastuk.html` and it opens in your default browser.
No install, no build step, no server required for the core app.

> The **3D Massing** tab loads the Three.js library at runtime from
> `cdnjs.cloudflare.com`, so an internet connection is needed for that
> one tab. The 2D Blueprint and Compliance Report tabs work fully offline.

## Deploy it to a public URL (free, no login required for a quick link)

**Netlify Drop — fastest**
1. Go to https://app.netlify.com/drop
2. Drag this folder (or just `vastuk.html`) onto the page
3. You'll get an instant live URL like `random-name.netlify.app`

**GitHub Pages — free and permanent**
1. Create a new GitHub repository and upload `vastuk.html`
2. Go to Settings → Pages → set the source branch to `main`
3. Your site will be live at `yourusername.github.io/reponame`

**Vercel or Cloudflare Pages**
Both support the same drag-and-drop style deploy and give you a
`.vercel.app` or `.pages.dev` URL on their free tiers.

## How the rule engine works, briefly

The plot is divided into a directional grid mapped to the eight
compass zones of the Vastu Purusha Mandala (N, NE, E, SE, S, SW, W, NW)
plus the center (Brahmasthan). Each requested room is placed into the
zone that best matches classical Vastu guidance — e.g. kitchen →
South-East, master bedroom → South-West, pooja room → North-East,
staircase → South/West — using a scored, priority-ordered greedy
placement, then graded for a compliance report.

## Disclaimer

This is a concept-stage planning tool, not a substitute for a licensed
architect, structural engineer, or a professional Vastu consultant.
Always validate any layout against local building codes before
construction.
