# From Fringe to Floor Vote

**Live visualization:** https://reymuniziii-svg.github.io/fringe-to-floor-vote/

An interactive, scrollytelling visualization of how Universal Basic Income moved from fringe idea to mainstream policy attention.

## What this shows
- A Google Trends time series (2004–2023) for UBI-related search interest.
- A curated milestone timeline layered on top of the trend line.
- Era highlighting to show shifts in attention (intellectual, wilderness, silicon, yang, covid, aftermath).

## Data
- `data/trends_ubi.json` — Google Trends time series (normalized 0–100).
- `data/milestones.json` — Milestones, eras, and key figures used for annotations.

Note: The timeline includes events before 2004; Google Trends data begins in 2004. Earlier eras are shown via milestones only.

## Local development
```bash
cd ~/.claude/visualizations/attention
python3 -m http.server 8080
# open http://localhost:8080/
```

## Project structure
- `index.html` — Main visualization (self-contained)
- `data/` — JSON datasets
- `assets/` — (reserved for images or media)

## Credits / Sources
- Google Trends (trend time series)
- Milestone timeline compiled from public records and widely cited historical events
