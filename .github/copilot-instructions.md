# Copilot Instructions for AI Agents

## Project Overview
This project is a minimal Leaflet.js web map demo, consisting of a single `index.html` file. It demonstrates how to embed an interactive map using the Leaflet library and OpenStreetMap tiles.

## Key Files
- `index.html`: Main entry point. Contains all HTML, CSS, and JavaScript for the map.

## Architecture & Patterns
- Uses CDN links for Leaflet CSS and JS (no local dependencies or build steps).
- All logic is in a single `<script>` block in `index.html`.
- The map is initialized with `L.map('map').setView([lat, lng], zoom)`.
- Tile layer uses OpenStreetMap: `L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', ...)`.
- Example marker and popup are added for demonstration.

## Developer Workflows
- No build, test, or deployment scripts are present.
- To view the project, open `index.html` directly in a browser.
- No package manager or external configuration files are used.

## Project-Specific Conventions
- All code is inline; no modularization or external JS/CSS files.
- Map container uses `#map` with `height: 100vh; width: 100%` for full viewport display.
- No custom Leaflet plugins or advanced features are used.

## Integration Points
- Relies on Leaflet and OpenStreetMap via CDN.
- No backend, API, or cross-component communication.

## Example: Adding a Marker
```js
L.marker([lat, lng]).addTo(map).bindPopup('Popup text');
```

## Guidance for AI Agents
- Focus on editing or extending `index.html`.
- When adding features, follow the inline style (add JS in the existing `<script>` block).
- If introducing new files or structure, document the rationale in this file.
- Keep the project simple and dependency-free unless requirements change.
