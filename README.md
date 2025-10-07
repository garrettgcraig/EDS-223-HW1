# Environmental Justice Analysis: Superfund Sites in New Mexico

## Purpose

This project analyzes environmental justice concerns in New Mexico by examining the spatial distribution of Superfund sites and their relationship to vulnerable populations, with particular focus on Indigenous communities. The analysis uses EPA EJScreen data to explore how proximity to contaminated sites intersects with demographic vulnerability, highlighting environmental burdens on Native American tribal lands in a state with a significant history of uranium mining and nuclear weapons testing.

## Repository Contents

```
EDS223-HW1/
├── ej_screen.qmd          # Main Quarto analysis document
├── ej_screen.html         # Rendered HTML output
├── data/                  # Data files (not tracked in git)
│   ├── ejscreen/         # EPA EJScreen geodatabase
│   └── tl_2020_us_aiannh/ # Census TIGER/Line tribal boundaries
└── README.md
```

## Data Access

This analysis requires two datasets:

1. **EPA EJScreen Data (2023)**: Download from [EPA EJScreen](https://www.epa.gov/ejscreen/download-ejscreen-data)
   - Required file: `EJSCREEN_2023_BG_StatePct_with_AS_CNMI_GU_VI.gdb`
   - Place in `data/ejscreen/` directory

2. **Census TIGER/Line Shapefiles (2020)**: Download from [Census Bureau](https://www.census.gov/cgi-bin/geo/shapefiles/index.php?year=2020&layergroup=American+Indian+Area+Geography)
   - Required: American Indian/Alaska Native/Native Hawaiian Areas shapefiles
   - Place in `data/tl_2020_us_aiannh/` directory

## Installation

### Required Software
- R (version 4.0 or higher)
- RStudio (recommended)
- Quarto

### R Package Dependencies
```r
install.packages(c("tidyverse", "sf", "here", "tmap", "spData",
                   "biscale", "cowplot", "ggspatial"))
```

### Running the Analysis
1. Clone this repository:
   ```bash
   git clone https://github.com/garrettgcraig/EDS223-HW1.git
   ```
2. Download required datasets (see Data Access section)
3. Open `ej_screen.qmd` in RStudio
4. Render the document using Quarto

## Output

The analysis produces four maps:
1. **Superfund Site Distribution by County** - County-level aggregation of NPL sites
2. **Environmental Justice Index** - Statewide Superfund Proximity EJ Index
3. **Cibola County Focus** - Detailed view highlighting Native American lands
4. **Demographic Vulnerability Patterns** - Bivariate analysis of people of color and low-income populations

All maps include compass roses, scale bars, and appropriate legends. The rendered HTML document is self-contained with embedded resources.

## Author

**Garrett Craig**
Master of Environmental Data Science
Bren School of Environmental Science & Management, UC Santa Barbara

## Acknowledgements

- **Data Sources**:
  - U.S. Environmental Protection Agency (EPA) - EJScreen Environmental Justice Screening and Mapping Tool
  - U.S. Census Bureau - TIGER/Line Shapefiles for American Indian/Alaska Native/Native Hawaiian Areas

- **Course**: EDS 223 - Spatial Analysis, Bren School, UCSB

## License

This project is available under the MIT License.
