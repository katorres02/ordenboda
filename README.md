# Camila & Carlos — Wedding Seating 💍

Interactive seating chart for the wedding at **1445 Bd Roberval E, Longueuil**.
Everything lives in a single file (`index.html`) with **no external dependencies** —
works offline and deploys straight to GitHub Pages.

**Live site:** https://katorres02.github.io/ordenboda/

## Features

- **Venue** tab: 3D recreation of the backyard — house, pool, cottage, the couple's
  canopy (the carport) with its driveway and garden gate. Toggle between the
  ceremony and dinner setups; hover a chair to see who sits there.
- **Ceremony** tab: two seating sections with a center aisle, couple at the altar.
- **Dinner** tab: U-shaped table — main table (5) on top, two arms going down.
- **Floor plan / 3D view** toggle on both seating tabs.
- **Guest search**: type a name to highlight their seat in pistachio green.
- **Editor sign-in**: only the signed-in editor can move guests, add/remove them,
  adjust the layout or reset. Everyone else can view and print.
- Changes save automatically to the browser (localStorage), per device.

## Editor PIN

Click **🔒 Sign in to edit** and enter the PIN. The default PIN is **`1445`** —
change it by editing the `EDITOR_PIN` constant near the top of the `<script>`
in `index.html`.

> Note: this is a light client-side gate to prevent accidental edits — not real
> security. Anyone who reads the source can find the PIN.

## Editing

- Tap a guest chip, then tap a seat — or drag & drop (desktop).
- Tap an occupied seat to pick that guest up and move them.
- Drag a guest back to the "Unassigned" list to free their seat.
- **⚙︎ Adjust layout** changes the number of seats/rows per section.

## Publishing changes

The published site shows the default seating hard-coded in `index.html`
(each visitor's edits stay on their own device). To make a new arrangement
the default for everyone, update `defaultState()` in `index.html` and push:

```bash
git add index.html && git commit -m "Update seating" && git push
```

GitHub Pages redeploys automatically in ~1 minute.
