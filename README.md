# US Urban Migration Patterns (2000–2020) 🏙️

An exploratory analysis of demographic change in U.S. cities between 2000 and 2020, focusing on the **Top 10 Growing** and **Top 10 Shrinking** cities. This project builds on the Global Urban Demographic Dataset (GUDD) and applies the visualization style of Zimmer et al. (2026) to the U.S. context.

---

## 📌 Overview

This repository contains:

- Interactive maps of US cities showing population growth/decline 2000–2020
- Static maps in the style of the published *Nature Cities* paper
- Animated trajectory plots showing how cities evolved across **population**, **migration**, and **births**
- A focused comparison of the **Sunbelt boom** vs **Rust Belt decline**

> ⚠️ **Note:** This is an exploratory project for learning and personal research. It uses the original GUDD dataset without modification and reuses code patterns from the official Zimmer et al. (2026) repository, with full attribution.

---

## 🎯 Cities Analyzed

### Top 10 Growing US Cities (2000–2020)
Los Angeles · Las Vegas · Miami · Phoenix · Dallas · Mesa · Washington · Orlando · Sacramento · Portland

### Top 10 Shrinking US Cities (2000–2020)
Chicago · Detroit · New Orleans · Cleveland · St. Louis · Pittsburgh · Buffalo · Cincinnati · Dayton · Toledo

---

## 📊 Data Source

This project uses the **Global Urban Demographic Dataset (GUDD)** developed by Zimmer et al.:

> Zimmer, A., Brooks, N., Gaughan, A. E., Giezendanner, J., Tuholske, C. (2026). *Global Urban Demographic Dataset (GUDD), version 1.* Harvard Dataverse.

**Original Paper:**

> Zimmer, A., Brooks, N., Gaughan, A. E., Tuholske, C. (2026). *Global Divergence in Urban Demographic Change and Migration Patterns.* Nature Cities.

**Original Code Repository:**
[https://github.com/zimmermaps/urban_demography](https://github.com/zimmermaps/urban_demography)

**Interactive Data Explorer:**
[https://zimmermaps.github.io/urban_demography/gudd-explorer/maps/index.html](https://zimmermaps.github.io/urban_demography/gudd-explorer/maps/index.html)

---

## 🚀 Quick Start

### 1. Clone this repository
```bash
git clone https://github.com/YOUR_USERNAME/us-urban-migration.git
cd us-urban-migration
```

### 2. Set up a Python environment (Python 3.11 recommended)
```bash
python3.11 -m venv .venv
source .venv/bin/activate       # macOS/Linux
# .venv\Scripts\activate        # Windows
```

### 3. Install dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Download the GUDD dataset
The dataset is not included in this repository (it's too large). Download it directly from the original source:

- **Harvard Dataverse:** [Link in original paper](https://github.com/zimmermaps/urban_demography)

Place the unzipped CSV files in `data/` so the structure looks like:
```
data/
├── gudd_annual_metrics_static_boundaries.csv
├── gudd_change_2000_2020_static_boundaries.csv
└── ne_50m_admin_0_countries.shp  (and accompanying .dbf, .shx, etc.)
```

### 5. Launch Jupyter
```bash
jupyter lab
```

Open the notebooks in `notebooks/` and run them.

---

## 📁 Repository Structure

```
us-urban-migration/
├── README.md                          ← this file
├── LICENSE                            ← MIT License
├── CITATION.cff                       ← how to cite this work
├── requirements.txt                   ← Python dependencies
├── .gitignore
│
├── notebooks/
│   └── migration_pattern_analysis.ipynb   ← main analysis notebook
│
├── figures/                           ← generated GIFs and plots
│   ├── us_focus_migration_colored.gif
│   ├── us_focus_births_colored.gif
│   └── us_top_growing_shrinking_map.html
│
└── data/                              ← (not tracked) place GUDD data here
    └── .gitkeep
```

---

## 🔑 Key Findings

| Pattern | Insight |
|---|---|
| **Sunbelt Boom** | Phoenix, Las Vegas, Miami grew primarily through migration |
| **Rust Belt Decline** | Detroit, Chicago, Cleveland lost hundreds of thousands |
| **New Orleans Anomaly** | Shrank due to Hurricane Katrina (2005), not industrial decline |
| **Texas / Florida** | Multiple cities in top growers — migration-driven |
| **Births** | Generally declined across all cities, but more pronounced in shrinking ones |

---

## 🛠️ Built With

- **pandas** — data manipulation
- **geopandas** — geographic data
- **matplotlib** — static plots and animations
- **folium** — interactive maps
- **branca** — colormap legends for folium
- **seaborn** — plot styling

---

## 🙏 Credits & Acknowledgments

This project would not be possible without:

1. **The Zimmer et al. team** for creating and openly publishing the GUDD dataset and analysis code under the MIT License.
2. **The CIESIN data center at Columbia University** for hosting the dataset.
3. **Natural Earth** for the public-domain country boundary shapefiles ([naturalearthdata.com](https://www.naturalearthdata.com/)).
4. **Global Human Settlement Layer (GHSL)** for the urban boundaries underlying the GUDD dataset.

The visualization style (color palettes, font choices, plot structure) is reused with attribution from the official `07_fun_figures.ipynb` and `09_figure4a_migration_map.ipynb` notebooks in the original Zimmer et al. repository.

---

## 📜 License

This project is released under the **MIT License** — see [LICENSE](LICENSE).

The underlying GUDD dataset is licensed separately by Zimmer et al.; refer to their [original repository](https://github.com/zimmermaps/urban_demography) for data licensing terms.

---

## 📝 Citation

If you use this analysis, please cite both this repository AND the original Zimmer et al. paper:

```bibtex
@article{zimmer2026global,
  title   = {Global Divergence in Urban Demographic Change and Migration Patterns},
  author  = {Zimmer, Andrew and Brooks, Nick and Gaughan, Andrea E. and Tuholske, Cascade},
  journal = {Nature Cities},
  year    = {2026}
}
```

See [CITATION.cff](CITATION.cff) for how to cite this repository.

---

## 👤 Author

**Najiba** — PhD researcher at Oregon State University

If you have questions or want to collaborate, please open an issue.
