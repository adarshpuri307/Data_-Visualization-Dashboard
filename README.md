# Data Visualization Dashboard

A clean, responsive dashboard that visualizes sample business data using [Chart.js](https://www.chartjs.org/) — featuring bar, line, and pie charts.

## Features

- 📊 **Bar Chart** — Monthly sales figures
- 📈 **Line Chart** — Website traffic trends over time
- 🥧 **Pie Chart** — Device usage breakdown (Desktop / Tablet / Mobile)
- 📱 Responsive grid layout that adapts to screen size
- 🎨 Clean white card UI on a blue gradient background

## Project Structure

```
data-viz-dashboard/
├── index.html    # App markup + Chart.js CDN import
├── styles.css    # Styling and layout
└── script.js     # Chart.js configuration and data
```

## Setup

No build step or dependencies to install — Chart.js is loaded via CDN.

1. Clone or download this project.
2. Open `index.html` in your browser.

That's it! All three charts render immediately with the sample data.

## Customizing the Data

All chart data lives in `script.js`. Each chart is a separate `new Chart(...)` call:

| Chart | Variable | What to edit |
|---|---|---|
| Bar Chart | `barCtx` | `labels` (months) and `data` (sales values) |
| Line Chart | `lineCtx` | `labels` (months) and `data` (traffic values) |
| Pie Chart | `pieCtx` | `labels` (device types) and `data` (percentages) |

To connect real data, replace the hardcoded `labels`/`data` arrays with values fetched from your own API or backend (e.g., via `fetch()`), then re-render or re-instantiate the charts.

## Dependencies

- [Chart.js](https://www.chartjs.org/) (loaded via CDN in `index.html`, no local install needed)

## Known Limitations / Ideas for Improvement

- Data is static/hardcoded — no live data source or API integration yet
- No dark mode toggle
- No way to filter by date range or export chart data
- Charts don't currently resize their container height explicitly, which can cause uneven sizing on some screens — consider wrapping each `<canvas>` with a fixed-height container if this becomes an issue

## License

MIT — feel free to use and modify.
