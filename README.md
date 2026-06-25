# From Fringe to Floor Vote

A scrollytelling visualization of how Universal Basic Income traveled from academic obscurity to pandemic-era policy. Live here: [reymuniziii-svg.github.io/fringe-to-floor-vote](https://reymuniziii-svg.github.io/fringe-to-floor-vote/). As you scroll, a Google Trends search-interest line for UBI animates beneath a timeline of the milestones that drove each spike, color-coded by era.

## What it shows

- A monthly Google Trends series for UBI search interest, 2004 to 2023 (402 points, normalized 0 to 100).
- 32 milestone events layered on the trend line, from the 1962 intellectual roots through the 2020 pandemic and its aftermath.
- Six eras (intellectual, wilderness, silicon, yang, covid, aftermath), plus key figures and polling snapshots, used to annotate the shifts in attention.

The timeline reaches back to 1962, but Google Trends data only begins in 2004, so events before then appear as milestones without a corresponding trend line.

## Stack

One self-contained `index.html`, no build step and no framework. It uses [D3.js](https://d3js.org/) v7 for the chart and [Scrollama](https://github.com/russellsamora/scrollama) v3 for the scroll-driven steps, both loaded from the unpkg CDN, with Google Fonts for type. At runtime it `fetch`es the two JSON files in `data/`. No server-side code, no API keys, no environment variables.

## Data

- `data/trends_ubi.json`: the Google Trends time series, an array of `{ date, interest }` records.
- `data/milestones.json`: an object with `eras`, `events`, `key_figures`, and `polling`, used for the annotations.

## Run it locally

Because the page fetches JSON, serve it over HTTP rather than opening the file directly. From the repo root:

```bash
python3 -m http.server 8080
# then open http://localhost:8080/
```

Any static file server works. There is nothing to install or compile.

## Project structure

- `index.html`: the entire visualization, markup, styles, and D3 logic.
- `data/`: the two JSON datasets above.

## Sources

Google Trends for the search-interest series. The milestone timeline was compiled from public records and widely cited historical events.

## License

MIT. See [LICENSE](LICENSE).
