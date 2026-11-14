# earthrise-data

Prepared data for [Earthrise](https://github.com/Abulkosim/earthrise), a lunar landing site navigator
built for the NASA Space Apps Challenge 2026. The app loads these files in the browser.

Everything here is derived from public NASA data by `pipeline/scripts/build_web_data.py` in the
Earthrise repository. Nothing is edited by hand.

| Path | What | Source |
|---|---|---|
| `dem/far.bin.gz` | Elevation, 60-90 S, 960 m grid | LOLA `LDEM_60S_240M`, 4x4 block mean |
| `dem/mid.bin.gz` | Elevation, 80-90 S, 160 m grid | LOLA `LDEM_80S_80M`, 2x2 block mean |
| `dem/t80`, `dem/t40`, `dem/t20` | Elevation tiles at 80, 40 and 20 m (20 m south of 84 S) | LOLA `LDEM_80S_80M`, `_40M`, `_20M` |
| `ephem.bin` | Hourly Sun and Earth vectors seen from the Moon, 2023-2045 | JPL DE440 through SPICE (NAIF kernels) |
| `fixtures.json` | Reference answers for the engine check | Earthrise reference model |
| `validation/` | Crops of NASA Goddard's average visibility maps | `AVGVISIB_85S_060M_201608` |
| `manifest.json` | Projection, grid sizes, time base | |

Grids are int16, height = value x 0.5 m above a 1737.4 km sphere, each row delta-coded, then gzip.
Projection: south polar stereographic, spherical, longitude 0 up.

LOLA data: NASA / GSFC / MIT, Lunar Reconnaissance Orbiter, from the PDS Geosciences Node.
Ephemeris: NASA / JPL. NASA does not endorse this project.

The preparation code was written with AI assistance (Claude); see the Earthrise README.
