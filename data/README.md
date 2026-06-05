# Data Folder

The data files used in this analysis are **NOT included** in this repository because:
1. They are large (>100 MB)
2. They are owned by the original authors (Zimmer et al.)
3. They should be downloaded from the original source for proper attribution

## How to Get the Data

### Step 1 — Download from the Original Repository

Go to the official Zimmer et al. repository:
**https://github.com/zimmermaps/urban_demography**

Clone or download the following files from `01_data/04_final_demographic_data/01_static_boundaries/`:

| File | Used For |
|---|---|
| `gudd_annual_metrics_static_boundaries.csv.zip` | Yearly demographic indicators |
| `gudd_change_2000_2020_static_boundaries.csv.zip` | 2000–2020 change summary |

And from `01_data/02_auxiliary_data/03_mapping.zip`:

| File | Used For |
|---|---|
| `ne_50m_admin_0_countries.shp` (and accompanying .dbf, .shx, .prj) | World country boundaries for maps |

### Step 2 — Unzip and Place Here

After unzipping, your `data/` folder should look like:

```
data/
├── gudd_annual_metrics_static_boundaries.csv
├── gudd_change_2000_2020_static_boundaries.csv
└── mapping/
    ├── ne_50m_admin_0_countries.shp
    ├── ne_50m_admin_0_countries.dbf
    ├── ne_50m_admin_0_countries.shx
    ├── ne_50m_admin_0_countries.prj
    └── ne_50m_admin_0_countries.cpg
```

## Data Citation

When using these files, please cite:

> Zimmer, A., Brooks, N., Gaughan, A. E., Giezendanner, J., Tuholske, C. (2026). 
> *Global Urban Demographic Dataset (GUDD), version 1.* Harvard Dataverse.

> Zimmer, A., Brooks, N., Gaughan, A. E., Tuholske, C. (2026). 
> *Global Divergence in Urban Demographic Change and Migration Patterns.* Nature Cities.

Country boundaries are from **Natural Earth** (public domain):
**https://www.naturalearthdata.com/**
