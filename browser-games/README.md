# browser-games datasets

Puzzle banks for [`kapetao/browser-games`](https://github.com/kapetao/browser-games),
consumed there via the `database` submodule at `src/data/browser-games/puzzles/`.

| Table | Files | What |
| --- | --- | --- |
| `puzzles/sudoku` | `easy.json`, `medium.json`, `hard.json` | 9×9 sudoku grids (+ solutions) |
| `puzzles/crosswords` | `easy.json`, `medium.json`, `hard.json` | word grids + clues |
| `puzzles/logic-puzzles` | `easy.json`, `medium.json`, `hard.json` | logic-grid puzzles (clues, categories) |

## Catalog

| Table | File | What |
| --- | --- | --- |
| `catalog/games` | `catalog/games.yaml` | the game catalog (source of truth): slug, title, `/play/<slug>` route, status, tags |
| `catalog/tags` | `catalog/tags.yaml` | generic tags used on games, issues, and PRs |
| `catalog/manifest` | `catalog/manifest.yaml` | catalog manifest |
