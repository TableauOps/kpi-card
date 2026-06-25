# Super KPI Card — a Tableau Viz Extension

A big, bold single-value KPI card you add to a worksheet's **Marks card**. Drop a
measure on the **Measure** tile (optionally a date on **Date**) and it renders an
abbreviated KPI value (`$48.2K`) on a dark card, with optional latest-period value,
a date caption, and a ▲/▼ period-over-period change.

This is a **viz extension** (not a dashboard extension): the manifest root is
`<worksheet-extension>` and it uses the worksheet's encoding shelves.

## Use it

1. Download **[`super-kpi-card.trex`](./super-kpi-card.trex)**.
2. In Tableau, on a worksheet's **Marks** card, choose **Add Extension** and select
   the `.trex` file.
3. Drop a continuous **measure** on the *Measure* shelf. Optionally drop a **date**
   dimension on the *Date* shelf.
4. Click the gear (top-right) to configure aggregation, prefix/suffix, decimals,
   abbreviation, title, date-caption text, change indicator, and colors.

The extension is hosted on GitHub Pages at
<https://tableauops.github.io/kpi-card/index.html> — that URL is baked into the
`.trex` `source-location`, so the `.trex` is all your audience needs.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The entire extension — vanilla HTML/CSS/JS, no build step. Renders the card (viz mode) and the settings dialog (`?dialog=1`). |
| `tableau.extensions.1.latest.min.js` | Tableau Extensions API library, hosted locally (Tableau does not publish it on a CDN). |
| `super-kpi-card.trex` | The manifest you load into Tableau. |

## Requirements

Tableau 2024.2+ (Extensions API **1.11+**, required for viz extensions).
