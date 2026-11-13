# Changelog

Every public release of AlphaNav, newest first. Each version's installers are on the
[Releases](https://github.com/giomengu/alphanav-releases/releases) page.

<!-- releases: the publishing workflow adds each new version below this line -->

## 1.3.3

- The processor runs on a core rate (25 Hz by default). Calculations have a default rate and their own, and the screens and every output send on a whole fraction of it: each output picks its rate from those (Processor ▸ Outputs). The screens' rate carries over from the old "publish" setting. Processor ▸ Core sets the core rate and the decoders.
- IMU mounting: say where the sensor's axes point in the boat, or level it with one tap (Processor ▸ IMU). The IMU gives the boat's heel, trim, heading and roll, pitch and yaw rates with the usual signs (heel to starboard positive, bow up positive).
- Motion-corrected apparent wind: a calculation can correct the masthead's wind for the mast's motion and become the boat's apparent wind, which the NMEA 0183 and NMEA 2000 outputs send, with true wind from it. New helpers for heel-levelled apparent wind. Mast-motion helpers now take the IMU's boat rates (formulas that used the raw gyroscope need updating).
- Raspberry Pi server: the processor builds as a fully static Linux program; the IMU's 3 Mbaud serial link and SocketCAN work in it.
- Devices and roles, the processor's own API, the storage core and many fixes from the last weeks.

## 1.3.2

Security update: install it in place of 1.2.9 or 1.3.0.

Before updating from 1.2.9: polars you uploaded were stored inside the app and the update replaces them. Export them from the polar editor first, then upload them again.

- Wi-Fi: earlier versions shipped a set of Wi-Fi networks with their passwords in the app's network settings. This version removes them from your settings and from your saved settings backups the first time it starts. Networks you added yourself are kept.
- Web pages from the internet can no longer change AlphaNav's settings or files, or open its live data, through a browser on the boat's network.
- Polar and other file requests accept plain file names only; an uploaded file can no longer be run as code.
- Your polars and sail charts are now kept in your settings folder, so updates no longer replace them. The app ships one default polar and the default sail chart.
- AIS collision and distress alarms are computed by the instrument core, for VHF and web AIS targets alike.
- Polars, sail chart tables and routing checks now run in AlphaNav's Swift core. GRIB files no longer need Java.
- Routing with a currents GRIB works again.
- Server components updated with security fixes.

## 1.3.0

Co-Authored-By: Claude Opus 5.5 <noreply@anthropic.com>

## 1.2.9

- Weather routing: a single routing engine, the newer frontier, for every run. It keeps a well-spread frontier at each step, finds routes around land and marks more reliably, and needs no engine or frontier choice any more.
- Weather routing: reverse isochrones, arrive-by, currents, wind and polar percentages and variation sweeps are always available, with no "needs another engine" warnings.
- Weather routing: "Best of N" is a plain option in the Solver section, for ensemble runs with their own beam, temperature and jitter.
- Weather routing: forecasts are read by their time and area index only, so routing starts sooner and uses less memory on large GRIB files.
- Weather routing: earlier saved runs, forms, pivots and automator flows open and recompute on the new engine as they are.
- Web Page widget: a site that refuses to be shown inside another page no longer leaves a blank white box. The widget says why, and offers "Open in its own window" or "Try here anyway".
- Widgets: retired legacy widgets are gone from the widget list. A saved layout that still holds one shows a small placeholder you can remove.
- Updates: the app tidies away downloaded installers and the previous version's files after updating.
- Installers: macOS (arm64), Windows (x64), Debian/Ubuntu (amd64), Fedora/RHEL (x86_64).

## 1.2.8

- Routing: every routing on the map carries its boat at the map's time, between its points and turning with the leg; a settings tab; run names from a template; reverse isochrones and arrive-by fixed; the frontier filters in place instead of copying ~20k nodes a step.
- Licence: the Swift processors (instrument, routing, charts, grib, zones, weather) check the licence themselves, so run on their own they do no work for an unlicensed install. Installs from the repository (development, the Pi) are unaffected.
- A boat's position at a time, for the tracks and the map.
- Installers: macOS (arm64), Windows (x64), Debian/Ubuntu (amd64), Fedora/RHEL (x86_64).

## 1.2.7

AlphaNav 1.2.7

## 1.2.5

Co-Authored-By: Claude Opus 5.5 <noreply@anthropic.com>

## 1.2.4

AlphaNav 1.2.4

## 1.2.2

AlphaNav 1.2.2

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
