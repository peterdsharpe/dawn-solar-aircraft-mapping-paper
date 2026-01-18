# An Optimization Approach to Mapping the Feasible Mission Space of a High-Altitude Long-Endurance Solar Aircraft

This repository contains the LaTeX source for the following paper:

> **Peter D. Sharpe, Annick J. Dewald, and R. John Hansman**, "An Optimization Approach to Mapping the Feasible Mission Space of a High-Altitude Long-Endurance Solar Aircraft," *AIAA AVIATION 2021 FORUM*, 2021.

**DOI:** [10.2514/6.2021-2451](https://arc.aiaa.org/doi/abs/10.2514/6.2021-2451)

## Abstract

High-Altitude Long-Endurance (HALE) aircraft are uniquely equipped to fill major gaps in current understanding of rapid and irreversible climate change. This paper presents a Multidisciplinary Design Optimization (MDO) framework - the *Dawn Design Tool* - to map the feasible mission space of solar-electric HALE aircraft.

Key findings include:
- Solar flux (latitude and time of year) and atmospheric conditions (steady winds, cruise altitude, gusts) are primary mission drivers
- Battery specific energy and solar cell efficiency are critical technological parameters
- Perennial flight requires wingspans exceeding 40 meters, while summer operations at high latitudes enable aircraft with sub-20-meter wingspans
- Two climate monitoring missions are analyzed: stratospheric ozone chemistry over CONUS and Arctic glacial dynamics observation

## Related Software

The optimization framework described in this paper is implemented in Python and freely available:

- **Dawn Design Tool:** [github.com/peterdsharpe/DawnDesignTool](https://github.com/peterdsharpe/DawnDesignTool)
- **AeroSandbox** (underlying optimization framework): [github.com/peterdsharpe/AeroSandbox](https://github.com/peterdsharpe/AeroSandbox)

## Repository Structure

```
.
├── main.tex           # Main LaTeX document
├── references.bib     # BibLaTeX bibliography
├── new-aiaa.cls       # AIAA LaTeX class file
├── new-aiaa.bst       # AIAA bibliography style
└── figures/           # Figures and diagrams
    ├── DawnIllustration.png
    ├── render.png
    ├── solarflux.png
    ├── winds_at_cruise.png
    ├── 30kg_payloadw_mission.png
    ├── max_payload.png
    ├── batt_spec_energy_sweep.png
    ├── xdsm.tikz
    └── ...
```

## Compilation

To compile the document, run:

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

Or use `latexmk`:

```bash
latexmk -pdf main.tex
```

**Requirements:** A LaTeX distribution with `biblatex`, `biber`, and TikZ packages.

## Citation

```bibtex
@inproceedings{Sharpe2021,
    author    = {Peter D. Sharpe and Annick J. Dewald and R. John Hansman},
    title     = {An Optimization Approach to Mapping the Feasible Mission Space
                 of a High-Altitude Long-Endurance Solar Aircraft},
    booktitle = {AIAA AVIATION 2021 FORUM},
    year      = {2021},
    doi       = {10.2514/6.2021-2451},
    url       = {https://arc.aiaa.org/doi/abs/10.2514/6.2021-2451}
}
```

## License

This is the authors' manuscript. The final published version is available at the AIAA Digital Library.
