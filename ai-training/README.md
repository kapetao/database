# ai-training datasets

Data for [`kapetao/ai-training`](https://github.com/kapetao/ai-training), consumed there via the
`database` submodule (mounted at `src/data/`). **Stub — no data committed yet.**

| Table | Status | Source | What |
| --- | --- | --- | --- |
| `sudoku/` | planned | `browser-games/puzzles/{sudoku,logic-puzzles,crosswords}` | preprocessed puzzle→solution pairs for the game **player** (solver), split easy/medium/hard |
| `images/` | planned | `ui-assets` (`src/img/**`) | image-recognition samples — labels/manifests only; image blobs stay in `ui-assets` |

Notes:
- Derived/preprocessed text-shaped data lands here; the upstream sources stay in `browser-games/`
  and `ui-assets` (no duplication of the raw banks/blobs).
- Model **weights** are not data — they live as release artifacts, referenced from
  `ai-training/src/models/`.
