# my-maps

A map of the same streets, drawn in a style I choose. This repository is that idea, and it has no app code yet.

OpenStreetMap is the base. The geometry, names, and places come from OSM. The look does not. A cute map, a cybercity map, and a visitor-centric map are three themes on one set of data, not three maps.

## Base

Use OSM vector tiles, not the public raster tile images. Raster tiles are already painted. A theme cannot recolor them into neon streets or soft illustrated blocks. Vector tiles keep roads, water, buildings, landuse, and points of interest as data, and a style paints them.

The public `tile.openstreetmap.org` servers are for light use and already have a look. They are a reference for what the data contains, not the tiles this app serves. A theme needs a vector source that allows restyling, such as a Protomaps or OpenMapTiles extract, or tiles generated from an OSM dump for the cities being shown.

Every view credits OpenStreetMap contributors. That credit stays visible in every theme.

## Themes

A theme is a style document: colors, line weights, label type, icon set, and which layers are on. Switching theme does not change the place. The camera, the selection, and the route stay put.

| Theme | What the eye gets | What it hides |
| --- | --- | --- |
| Cute | Round corners, a short pastel palette, illustrated icons for food, parks, and transit, soft shadows | Industrial detail, most road numbers, raw POI clutter |
| Cybercity | Dark ground, neon edges on roads and rail, a faint grid, glow on the selected place | Pastel fills, decorative nature textures |
| Visitor | Walking time, landmarks, food, transit stops, and a clear "you are here" | Local-only addresses, minor service roads, duplicate shop pins |

Visitor is the content theme. Cute and cybercity are paint. A visitor theme can wear either paint: pastel landmarks, or neon landmarks. The default pairing is visitor content with one paint, and the other paint remains one switch away.

## What a visitor sees

Open the map already framed on a neighborhood, not on a continent. The first paint is the chosen theme. The first pins are few: a handful of landmarks, places to eat, and the nearest transit, each with a walking minute count from the current point.

Search jumps the camera and drops one selected place. Tapping the map does not open a raw OSM tag sheet. It opens a short card: name, kind of place, walking time, and the direction to walk. The full tag set stays available behind that card for when the data itself matters.

A route is a walk line drawn in the theme's accent color. It follows the OSM foot network. It does not invent a road the data does not have.

## What this does not do yet

It does not render a map, download a city extract, or pick a final theme. The next step is one city, one vector extract, and the two paints plus the visitor layer on top of both.
