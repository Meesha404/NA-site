# North America DC Site Tools

Two connected static tools, no build step or API keys. Run on an ordinary web host; no ChatGPT app is required.

- `index.html` — Scanner for 68 U.S. reference locations. Canada and Mexico are not yet included in this shortlist.
- `atlas/index.html` — Explore nearby mapped features for a selected location.
- `scan-data.js` — Optional saved observations. The supplied file is empty: no geographic observations were successfully downloaded during this repair. Existing Atlas state electricity data is separate from these observations.

## Deploy

Extract this ZIP and commit its contents to your repository, with index.html at the published root and atlas/ beside it. Serve it through GitHub Pages or another static host.

1. Select a location and press **Load selected location**. A successful response adds observations to the map. An error means data was not loaded, not that the location failed the criteria.
2. If the source fails, the source menu lets you select another public Overpass server. Respect rate-limit messages before retrying.
3. Once one location loads, use **Scan remaining locations**. A full scan can take many minutes. Stop preserves completed results; three consecutive failures stop the scan automatically.
4. Checkboxes filter loaded results immediately. Successful results are also cached in this browser.
5. Press **Save loaded data for GitHub** and replace this project's scan-data.js with the downloaded file. Commit it to show those saved observations immediately on future visits, with their original dates.

The repair preserves progressive results during checkbox changes, shows loaded/failed/unloaded counts, handles incomplete source responses, and queries a fixed area covering all slider ranges. The linked Atlas uses the selected source too.

These are geographic screening leads, not confirmed buildable sites. Mapped water does not establish usable supply, mapped power lines do not establish spare capacity, industrial polygons do not establish land availability, and connectivity points do not establish fiber service. Policy coverage is partial. Unknown evidence does not pass a checked criterion. Public-source outages and missing map features remain possible.

Source: OpenStreetMap contributors, through public Overpass services. See https://wiki.openstreetmap.org/wiki/Overpass_API and https://www.openstreetmap.org/copyright .

Internet access is required at runtime for Leaflet, the OpenStreetMap Overpass
API, and Esri map tiles.
