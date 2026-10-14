# 🗄️ datasets

Account-wide **data tier** — generated/accumulating datasets shared across deployables.
A repo-shaped stand-in for a database: each folder is a *table*, each file holds rows
(and could later move to a real DB, one table per folder).

Consumed as a **git submodule** where a project needs it (e.g. `data-science` mounts this
repo at `src/data/snapshots/data-science/`).

## 📇 Catalog

| Dataset | Project | Source | Cadence | Visibility |
| --- | --- | --- | --- | --- |
| `data-science/markets/movements.json` | data-science | brapi.dev (B3), Yahoo `.SA` fallback | scheduled | public |
| `data-science/news/brazil.json` | data-science | RSS | scheduled | public |
| `data-science/news/tech.json` | data-science | RSS | scheduled | public |

## 🗂️ Layout

```text
<project>/<table>/<file>.json
```

Each `<project>/` should carry its own `README.md` documenting its tables (schema, source, cadence, retention).

## 🚫 Not here

Private/personal data (`private`, `documents`, `life-events`) stays in its own repos — repo
visibility is the trust boundary, so public and private datasets can't share one repo.
Application code, build logic, and static presentation assets (`ui-assets`) live elsewhere.
