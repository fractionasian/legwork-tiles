# legwork-tiles

Pre-baked OSM path tiles for **[Legwork](https://github.com/fractionasian/legwork)** — the running/cycling route planner.

This repo is **generated data**, not hand-edited. The build script (`scripts/build-tiles.js` in the `legwork` repo) queries Overpass, splits each configured city into ~5.5 km GeoJSON tiles, and publishes the result here. The Legwork app fetches `manifest.json` + `tiles/<city>/<row>_<col>.json` from this repo's GitHub Pages site.

- **Manifest:** [`manifest.json`](manifest.json) — tile index with per-city bounds, grid, suburb names, version hash.
- **Served at:** `https://fractionasian.github.io/legwork-tiles/`
- **History:** intentionally squashed each build — this repo carries current tiles only, no version history (keeps it light).

Why a separate repo: keeps the `legwork` code repo small and fast to clone; map data lives here.
