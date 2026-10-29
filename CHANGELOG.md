# Changelog

Every public release of AlphaNav, newest first. Each version's installers are on the
[Releases](https://github.com/giomengu/alphanav-releases/releases) page.

<!-- releases: the publishing workflow adds each new version below this line -->

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
