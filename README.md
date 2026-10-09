# iSawIt

A simple offline-capable webapp (PWA) to quickly log wildlife sightings on **Barro Colorado Island (BCI), Panama** and export them as CSV.

## Taxa
Bats, Birds, Mammals and Insects. Species lists come from the BCI checklists (CSV files in this repo) and use scientific names for now (prototype). Mammal subspecies are excluded.

- **Insects:** the Quick list has only 50 species as a test; the full checklist (~1,940 species) is selectable as "Full checklist" at session start.
- Species not in a list can be added in the app.

## Spots
Placeholder BCI spots (Lab Clearing, Trail, Canopy Tower, Dock) live in `config.json`; more can be added in the app.

## Updating the species lists
Edit `build_config.py` (spots, insect quick-list size) and run:

    python build_config.py

This regenerates `config.json` from the `*.csv` files. Bump `CACHE` in `sw.js` after changing data so installed copies refresh.

## Run
Serve the folder over HTTP (e.g. `python -m http.server`) and open it in a browser; install as an app from the browser menu.
