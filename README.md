# Nomi delle strade OSM

[![AI Slop Inside](https://sladge.net/badge.svg)](https://sladge.net)

A single-page guide for writing Italian street names in OpenStreetMap, live at **https://name.giope.re/**.

It follows the street-name conventions of the [Italian OSM wiki](https://wiki.openstreetmap.org/wiki/IT:Editing_Standards_and_Conventions#Nomi_delle_strade) and the Istat [instructions for street naming](https://www.agenziaentrate.gov.it/portale/documents/20143/266134/Informativa+Istat_Istruzioni+ordinamento+ecografico.pdf/c7cd141f-4acb-cf5a-42b3-04ade2c69474). The page has:

- a step-by-step flowchart from the name on the street sign to the OSM tags;
- a checker that fixes common problems (all caps, abbreviations, numbers, saints' prefixes, titles) and proposes `name`, `alt_name`, `old_name` and `ref`;
- an optional `name:etymology` and `name:etymology:wikidata` suggestion, found with a Wikidata SPARQL query that only returns people;
- a table of where OSM and Istat differ, and a short tag reference.

The page is in Italian, and its suggestions are a starting point: always check them against the street sign or the municipality's street register.

## Wikidata queries

The page calls `query.wikidata.org` from the browser. To keep the load low, it sends one query at a time, waits at least 5 s between queries, follows `Retry-After` when asked to slow down, and caches results for 7 days in the browser.

## Running it

It is one static `index.html` with no build step: open it in a browser or serve the folder with any static server. Pushes to `main` deploy it to GitHub Pages.

## License

[GPL-3.0](LICENSE)
