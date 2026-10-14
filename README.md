# 🗄️ database

Account-wide **data tier** — a repo-shaped stand-in for a deployable database.
One folder per project (= schema); a subfolder per table; each file holds rows.

Consumed as a **git submodule** where a project needs it
(e.g. `data-science` mounts this at `src/data/snapshots/`).

## 🧭 What goes here (the rule)

Move content into `database` when it is **data** — a source of truth or an accumulating record:

- structured content: JSON / CSV / TSV / NDJSON / records
- catalogs, puzzle banks, scores / leaderboards, curated lists, snapshots

**Stays in the source repo:**
- code and **scripts** (any size — logic, not data)
- **small inline fixtures/examples** used directly by code (≤ the floor below)
- build config the code reads: `defaults.json`, linters, `tsconfig`, `devcontainer.json`

**Belongs in `ui-assets` instead** (the other tier):
- presentation binaries: images, audio, fonts, `css`, `tokens`
- anything whose weight is *bytes, not rows*

## 📏 Size thresholds (tunable)

| Size / kind | Where |
| --- | --- |
| ≤ 4 KB and only used as a code fixture | keep in the repo |
| > 4 KB **structured data** (rows) | `database` |
| > ~1–2 MB, or binary/presentation | `ui-assets` (or LFS) |
| scripts / build logic | stay in the repo (size-independent) |

## 📇 Catalog

| Project | Tables | Source | Cadence | Visibility |
| --- | --- | --- | --- | --- |
| `data-science/` | `markets/movements`, `news/brazil`, `news/tech` | brapi.dev (B3) · RSS | scheduled | public |
| `browser-games/` | `puzzles/{sudoku,crosswords,logic-puzzles}`, `catalog/*` | hand-authored banks · game catalog | on change | public |
| `wiki/` | `consumables/*`, `playlists/*`, `tasks/*` | source of truth for the wiki views | on change | public |

## 🗂️ Layout

```text
<project>/<table>/<file>.json      # one project per folder, one table per subfolder
```

Each `<project>/` carries its own `README.md` documenting its tables (schema, source, cadence, retention).

## 🚫 Not here

Private/personal data (`private`, `documents`, `life-events`) — repo visibility is the
trust boundary, so public and private datasets can't share one repo. Application code,
build logic, and static presentation assets (`ui-assets`) live elsewhere.
