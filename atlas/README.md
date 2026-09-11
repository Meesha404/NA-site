# North America Data Center Atlas — corrected source

Open index.html in a browser after extracting the ZIP. Bundled state boundaries and EIA electricity data are embedded in the page, so they no longer require a local server.

Opening the map automatically requests a Dallas–Fort Worth study area. This is an opening location, not a site recommendation. Change a checkbox to display/filter layers; if geographic data has not loaded, the selection starts a request. Loading and errors are shown directly on the map. After panning, use Load / retry this area.

Internet access is still required for the Leaflet map library, map tiles, the geographic converter, OpenStreetMap/Overpass and Canada/Mexico boundary queries. Geographic water, transmission, land and digital-infrastructure features are queried live and are not bundled. If the source is unavailable, the app cannot calculate geographic intersections; it will explain the failure. EIA state electricity context remains available independently.

Files: index.html, style.css, app.js, engine.js, energy.json, states.json.
No build step or API key is required. Optional local serving: python3 -m http.server 8000

Sources, attribution and coverage limitations are documented under Sources & methodology. The bundled electricity data is EIA 2024 for all 50 states plus D.C.; these are installed generation totals and all-sector retail prices, not spare grid capacity or data-center tariffs. State display boundaries come from the supplied prototype. Policy review remains limited to Texas and Illinois as of September 11, 2026. Water rights, available power, resilience, fiber availability and purchasable land remain unverified. Canada/Mexico electricity comparisons and most policy reviews are not integrated.

The corrected selection/loading logic and bundled data were checked programmatically. The live external map/data service connection has not been verified end to end in this workspace.
