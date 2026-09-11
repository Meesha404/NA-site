# North America DC Site Tools

Two connected tools, static site, no build step, no API keys.

- `index.html` — Hotspot Scanner. Scans 68 known industrial/power hubs across the
  US using live OpenStreetMap data and gives you a shortlist.
- `atlas/index.html` — Data Center Atlas. Detailed dense-grid local verification
  for a specific area. The scanner's "Verify in detail →" links open this,
  pre-centered on the chosen hotspot.

## Deploy

Upload this whole folder (keeping `atlas/` as a subfolder) to GitHub Pages or
Vercel. No configuration needed — the link between the two tools is a relative
path (`atlas/index.html`) that already matches this structure.

Internet access is required at runtime for Leaflet, the OpenStreetMap Overpass
API, and Esri map tiles.
