# Stedsnuser v2.0.0
For fun searching around the world. (Repoet heter Globetrotter.io, appen heter Stedsnuser.)

App: https://kilemann.github.io/Globetrotter.io/

- Søk etter et land, en by eller et sted, med forslag mens du skriver
- Globus med bryter mellom satellitt og kart. Roterer ved start, flyr til stedet du søker på
- Sett en pin (klikk på PC, trykk og hold på mobil): appen finner stedet og viser Wikipedia-artikler innen 10 km
- Innledningen fra engelsk Wikipedia, med bilde og lenke til hele artikkelen
- Knapp som åpner stedet i Google Maps (app på mobil, nettside på PC)

Én HTML-fil, ingen server og ingen API-nøkler.

## Kilder og teknikk
- Globus: MapLibre GL JS 5.24.0 (unpkg), globusprojeksjon med atmosfære
- Satellitt: EOxCloudless 2024 (Copernicus Sentinel-2) fra EOX – gratis for ikke-kommersiell bruk, krever kildehenvisning
- Kart: OpenFreeMap, stilen «liberty» (OpenStreetMap-data, ingen nøkkel)
- Sammendrag: Wikimedia REST API `page/summary/{tittel}`
- Forslag, søk og «i nærheten»: MediaWiki Action API (`prefixsearch`, `search`, `geosearch` med radius 10 km, som er maks)
- Pin → stedsnavn: Nominatim reverse (OpenStreetMap), maks én forespørsel i sekundet; Wikidata gir engelsk Wikipedia-tittel
- Google Maps: offisielt Maps URLs-format `https://www.google.com/maps/search/?api=1&query=...`

## Ny versjon
Sett `version` i `package.json`, `VERSION` og kommentaren øverst i `index.html`, og før opp endringen i info-vinduet og her.

## Versjoner
- 2.0.0 – Globus i stedet for flatt kart, med bryter mellom satellitt og kart. Pin viser stedet og Wikipedia-artikler i nærheten.
- 1.1.0 – Nytt navn: Stedsnuser (tidligere Globetrotter).
- 1.0.0 – Første versjon: søk med forslag, utdrag fra engelsk Wikipedia, kart og lenke til Google Maps.
