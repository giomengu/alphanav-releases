# Changelog

Every public release of AlphaNav, newest first. Each version's installers are on the
[Releases](https://github.com/giomengu/alphanav-releases/releases) page.

<!-- releases: the publishing workflow adds each new version below this line -->

## 1.1.1

Race tracking
- Adrena / FTP position reports: import a .dcc competitor file, passwords included; boats get their class, hulls, foiler flag and colours.
- Race list actions: show track, boat settings, and Route competitor.

Routing
- Competitor routing: route any competitor from its last report, with its own polar and polar % (automatic, or fixed and saved to the boat).
- Live isochrones now show the whole search while the routing runs.

Weather
- Every weather layer in a list with its own settings, and a colour palette per quantity.
- Map popup: all quantities at the point, and a meteogram over time; both configurable and saved with the map.

Map
- Light and dark colours for every map in one table; dark is automatic until you set it. Depth shading keeps its gradient.
- Readable hover labels on routes, waypoints, zones, boats and weather routings; easier to point at routes.
- GRIB downloads show the model's area and only move in the sides of the box that are out of bounds.

App
- Updates: AlphaNav checks for new versions and installs them in place (checksum verified).
- Settings: network access for phones and tablets with its live status; alarm sounds, volume, tone and halo with tests; a clearer Layout tab.
- Collision (CPA) alarms ring and show the halo.
- Tables: drag columns to reorder them, saved per widget.
- Phones: new Map + sheet and Split layouts, a touch-sized workbench, and an instrument strip.
- Instruments: capture and replay recording, logging improvements, NMEA 2000 output over CAN.

## 1.0.7

- macOS: signed with Developer ID and notarised by Apple — it opens with no security warning.

## 1.0.5

- ECMWF 9 km (and 0.25°) downloads are saved as GRIB2 in the GRIB download folder, ready for Adrena and other software.
- GRIB downloads keep going, with their progress, when you switch tabs; an optional notification tells you when one finishes or fails.
- Settings ▸ Map Files is shorter and shows your GRIB download folder.
- macOS: no more Keychain prompt ('Safe Storage') at every launch.

## 1.0.4

- Installs that already had AlphaNav update their database on start (a copy is kept): routes, map
  zones and route marks save again after an update.
- Routing avoids land everywhere with Natural Earth's world coastline built in; CM93 charts,
  OpenFreeMap or OpenWaters can be chosen instead, with Natural Earth wherever they have no data.
- Polar export, rename and duplicate, and every "save as", work in the desktop app.
- Desktop: an AlphaNav menu (About, Licence, Settings, network access), the window opens where it was,
  links open in the browser, a crashed window reloads itself.

## 1.0.3

- Weather routing: variation sweeps — the same routing for a few polar %, wind % or departure times,
  with the band between the routes on the map.
- Licence keys (1, 3, 6, 12 months or no end date) and a 30-day free trial.
- New installs start with the default layout, theme, map and weather settings.
