# data-science datasets

JSON snapshots produced by the collectors in
[`kapetim/data-science`](https://github.com/kapetim/data-science) and rendered by its
static GitHub Pages UI. Consumed there as a submodule at `src/data/snapshots/data-science/`.

| Table | File | What |
| --- | --- | --- |
| markets | `markets/movements.json` | B3 movers — returns, moving averages, volatility, threshold events |
| news/brazil | `news/brazil.json` | Brazil headlines — volume, keywords |
| news/tech | `news/tech.json` | Tech headlines — volume, keywords |

Schema per file: `{ category, generated_at, items[] }`. Written by
`src/collectors/crawler.py`; do not edit by hand.
