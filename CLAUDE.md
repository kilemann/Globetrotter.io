# Stedsnuser (repo Globetrotter.io)
Søk etter et sted og få en globus, innledning fra engelsk Wikipedia, artikler i nærheten og lenke til Google Maps. Én HTML-fil (`index.html`), ingen server eller API-nøkler.
Nettside: https://kilemann.github.io/Globetrotter.io/

## Regler for alt arbeid i dette repoet
- Svar brukeren på norsk. Commit-meldinger på norsk, med versjon først (f.eks. «Appnavn 1.4.0: kort beskrivelse»).
- Hver endring får nytt versjonsnummer (MAJOR.MINOR.PATCH) og en linje i endringsloggen. Versjonen skal være lik på alle stedene under.
- Lever rett på `main` når resultatet er godt nok og testene er grønne. Kjør `git fetch origin main` og rebase før push.
- Testdrevet utvikling (TDD) bare når brukeren ber om det. Eksisterende tester kjøres alltid før push.
- Tekniske påstander skal sjekkes mot dokumentasjon eller kilde, ikke gjettes.
- Appen står på samlesida (kilemann.github.io). Den skal vise navn, versjon og en (i)-knapp øverst til venstre. (i) åpner info-vinduet med bruksanvisning og versjonsliste. Oppdater versjonslista der ved hver ny versjon.
- Publiseres med GitHub Pages fra `main` (rot). Det tar noen minutter før endringen er ute.

## Versjon står her
- `index.html`: kommentaren øverst (`/* Stedsnuser vX.Y.Z` + changelog-linje), `const VERSION`, `<span class="ver" id="ver">` og versjonslista i info-vinduet
- `package.json`, `README.md` (tittel og «Versjoner»)

## Tester
Ingen automatiske tester ennå. Sjekk i nettleser før push.

## Viktig
- Kilder: MapLibre GL JS (unpkg), EOxCloudless (krever kildehenvisning), OpenFreeMap, Wikimedia REST og MediaWiki API, Nominatim (maks én forespørsel i sekundet).
