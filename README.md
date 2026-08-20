# Saint Kitts and Nevis Administrative Divisions / Saint Kitts and Nevis



## Overview

| Item | Details |
|------|---------|
| Parish | 14 |
| Locality | 119 |
| Coordinates | ✅ Included (all levels) |
| Formats | JSON, NDJSON, CSV |
| License | CC-BY-4.0 |
| Last Updated | 2026-08-20 |
| Website | [openadmindata.org/kn](https://openadmindata.org/kn/) |
| API | [openadmindata.org/api/kn](https://openadmindata.org/api/kn/) |
| Flag | [PNG](https://onlygames.me/flags-png/kn/) · [SVG](https://onlygames.me/flags-svg/kn/) · [PDF](https://onlygames.me/flags-pdf/kn/) |
| National Anthem | [🎵 Listen & Download Saint Kitts and Nevis National Anthem MP3](https://onlygames.me/national-anthems/kn/) |

## Browse by Parish

| # | Parish | Localitys | Link |
|---|----|----|------|
| 1 | Christ Church Nichola Town | 9 | [Browse](divisions/christ-church-nichola-town-kn01/) |
| 2 | Saint Anne Sandy Point | 4 | [Browse](divisions/saint-anne-sandy-point-kn02/) |
| 3 | Saint George Basseterre | 4 | [Browse](divisions/saint-george-basseterre-kn03/) |
| 4 | Saint George Gingerland | 18 | [Browse](divisions/saint-george-gingerland-kn04/) |
| 5 | Saint James Windward | 17 | [Browse](divisions/saint-james-windward-kn05/) |
| 6 | Saint John Capisterre | 8 | [Browse](divisions/saint-john-capisterre-kn06/) |
| 7 | Saint John Figtree | 13 | [Browse](divisions/saint-john-figtree-kn07/) |
| 8 | Saint Mary Cayon | 5 | [Browse](divisions/saint-mary-cayon-kn08/) |
| 9 | Saint Paul Capisterre | 7 | [Browse](divisions/saint-paul-capisterre-kn09/) |
| 10 | Saint Paul Charlestown | 3 | [Browse](divisions/saint-paul-charlestown-kn10/) |
| 11 | Saint Peter Basseterre | 12 | [Browse](divisions/saint-peter-basseterre-kn11/) |
| 12 | Saint Thomas Lowland | 6 | [Browse](divisions/saint-thomas-lowland-kn12/) |
| 13 | Saint Thomas Middle Island | 8 | [Browse](divisions/saint-thomas-middle-island-kn13/) |
| 14 | Trinity Palmetto Point | 5 | [Browse](divisions/trinity-palmetto-point-kn14/) |

## Data Files

| File | Format | Description |
|------|--------|-------------|
| [all-parish.json](data/all-parish.json) | JSON | All 14 parish records |
| [all-locality.json](data/all-locality.json) | JSON | All 119 locality records |
| [all-flat.json](data/all-flat.json) | JSON | Levels 1-1 flat array |
| [all-flat.ndjson](data/all-flat.ndjson) | NDJSON | Streaming format |
| [all-flat.csv](data/all-flat.csv) | CSV | Spreadsheet format |
| [hierarchy.json](data/hierarchy.json) | JSON | Nested tree |
| [schema.json](data/schema.json) | JSON Schema | Data schema |

## Quick Start

### Python

```python
import json

with open("data/all-parish.json", "r", encoding="utf-8") as f:
    data = json.load(f)

for r in data:
    print(f"{r['name']['local']} ({r['name']['en']}) — {r['children_count']['locality']} localitys")
```

### JavaScript

```javascript
import { readFileSync } from "fs";

const data = JSON.parse(readFileSync("data/all-parish.json", "utf-8"));
console.log(`Total: ${data.length} parishs`);
```

## Schema

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier |
| `level` | integer | 1=parish, 2=locality |
| `level_name` | object | Level label (local + English) |
| `name.local` | string | Name in local script |
| `name.en` | string | English name |
| `name.slug` | string | URL-safe slug |
| `parent` | object/null | Parent division reference |
| `ancestors` | array | Full ancestor chain |
| `children_count` | object | Count of children per level |
| `zip_codes` | array | Postal codes (where available) |
| `geo.lat` | string | Latitude (WGS84) |
| `geo.lon` | string | Longitude (WGS84) |

Full schema: [data/schema.json](data/schema.json)

## Hierarchy Browse

```
divisions/{parish-slug}/
```

Localitys are listed inline in each parish's README.

## AI Integration

- [llms.txt](docs/llms.txt) — Quick reference for AI agents
- [llms-full.txt](docs/llms-full.txt) — Summary with per-parish links
- [Per-parish data](docs/llms-full/) — Full data by parish

## Citation

```
Saint Kitts and Nevis Administrative Divisions Dataset (CC-BY-4.0)
URL: https://github.com/open-admin-data/saint-kitts-and-nevis-administrative-divisions
```

See [CITATION.cff](CITATION.cff) for machine-readable citation.

## License

- **Data**: [CC-BY-4.0](LICENSE)

## Related

- [Open Admin Data](https://openadmindata.org) — Browse, search and explore administrative divisions for every country
- [open-admin-data](https://github.com/open-admin-data) — GitHub organization with all country repos
- [ListBase](https://www.listbase.org) — Structured reference data for every country
