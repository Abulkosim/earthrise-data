# earthrise-data

Prepared terrain data for [Earthrise](https://github.com/Abulkosim/earthrise), a map of the Moon's south pole made for the NASA Space Apps Challenge 2026.

This repository holds the manifest, the ephemeris table, the comparison maps for the validation page, and the terrain at 960 m, 160 m, 80 m and 40 m.

The files are derived from NASA data: the Lunar Orbiter Laser Altimeter (LOLA) elevation maps as adjusted at NASA Goddard (Barker et al. 2021, 2023), SPICE ephemerides, and NASA Goddard's illumination maps. Sources, papers and licences are listed in the project's [CREDITS.md](https://github.com/Abulkosim/earthrise/blob/main/CREDITS.md). `pipeline/scripts/build_web_data.py` in the project builds these files from the originals.

This project is not endorsed by NASA.

Written with AI assistance (Claude); see the project's README.
