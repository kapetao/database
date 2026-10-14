# wiki datasets

Source-of-truth JSON for the wiki views, consumed there via the `database` submodule at
`scripts/data/wiki/`. The `src/**` views are **generated** from these — edit the JSON, then
run `npm run consumables` / `npm run playlists` / `npm run tasks`.

| Table | Files | Generates |
| --- | --- | --- |
| `consumables` | `grocery`, `household`, `pharmacy` | `src/consumables` views |
| `playlists` | `audiobooks`, `games`, `movies`, `music`, `podcasts`, `series`, `sounds` | `src/playlists` views |
| `tasks` | `government`, `health`, `housekeeping` | `src/tasks` views |
