# Globetrotter v1.0.0
For fun searching around the world.

App: https://kilemann.github.io/Globetrotter.io/

Søk etter et land, en by eller et sted, og få:
- innledningen fra engelsk Wikipedia, med bilde og lenke til hele artikkelen
- kart (OpenStreetMap via Leaflet) med punktet Wikipedia oppgir
- knapp som åpner stedet i Google Maps (app på mobil, nettside på PC)

Én HTML-fil, ingen server og ingen API-nøkler.

## Kilder og teknikk
- Sammendrag: Wikimedia REST API `page/summary/{tittel}` (tekst, bilde, koordinater, lenke)
- Forslag og søk: MediaWiki Action API (`generator=prefixsearch` / `generator=search`, `origin=*` for CORS)
- Kart: Leaflet 1.9.4 fra unpkg med integritetsnøkler, fliser fra tile.openstreetmap.org
- Google Maps: offisielt Maps URLs-format `https://www.google.com/maps/search/?api=1&query=...` (trenger ingen nøkkel)

Googles innebygde kart (Maps Embed API) krever API-nøkkel og Google Cloud-konto, derfor brukes OpenStreetMap inne i appen.

## Ny versjon
Sett `version` i `package.json`, `VERSION` og kommentaren øverst i `index.html`, og før opp endringen i info-vinduet og her.

## Versjoner
- 1.0.0 – Første versjon: søk med forslag, utdrag fra engelsk Wikipedia, kart og lenke til Google Maps.
