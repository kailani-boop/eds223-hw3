# EDS 223 HW 3: Prioritizing Potential Aquaculture

## Purpose
This repo contains the third homework assignment for EDS 223, Geospatial Analysis and Remote Sensing. The course introduces the spatial modeling and analytic techniques of geographic information science to data science students, with an emphasis on spatial data models and the analytic operations they enable.

Marine aquaculture has the potential to play an important role in the global food supply as a more sustainable protein option than land-based meat production (Hall et al., 2011). Gentry et al. (2017) mapped the global potential for marine aquaculture based on multiple constraints, including ship traffic, dissolved oxygen, and bottom depth, and found that global seafood demand could be met using less than 0.015% of the global ocean area. For this assignment, I determine which Exclusive Economic Zones (EEZs) on the U.S. West Coast are best suited for developing marine aquaculture for oysters and red abalone (*Haliotis rufescens*). Suitable locations are based on each species' range of suitable sea surface temperature (SST) and depth.


## Highlights
- Raster processing with `terra`: averaging, unit conversion, cropping, and resampling
- Reclassifying rasters and combining suitability layers with map algebra
- Calculating area by zone with `rasterize()`, `cellSize()`, and `zonal()`
- Building a reusable function that maps suitable area for any species
- Mapping results with `tmap`


## Repository Organization
```
EDS223-HW3
└─── README.md                    # Overview of the repository
└─── qmd/Rmd/Proj files
└─── red_abalone_analysis.qmd     # Quarto document with analysis
└───.gitignore                    # Excludes the data folder
    └───data                      # Not tracked on GitHub (see Data Access)
        └─── wc_regions_clean.shp           # West Coast EEZ boundaries (+ .dbf, .prj, .shx)
        └─── depth.tif                      # Bathymetry raster
        └─── average_annual_sst_2008.tif    # Average annual SST rasters
        └─── average_annual_sst_2009.tif
        └─── average_annual_sst_2010.tif
        └─── average_annual_sst_2011.tif
        └─── average_annual_sst_2012.tif
```

## Data Access
Because the files are too large for GitHub, the `data/` folder is listed in `.gitignore`. To run the analysis, download the data from [this Google Drive link](https://drive.google.com/file/d/1u-iwnPDbe6ZK7wSFVMI-PpCKaRQ3RVmg/view), unzip it, and place the files in a `data/` folder at the root of this repository.

The data includes:
- **Sea surface temperature** (`average_annual_sst_*.tif`): Average annual SST from 2008–2012, derived from NOAA Coral Reef Watch's 5km Daily Global Satellite Sea Surface Temperature Anomaly v3.1.
- **Bathymetry** (`depth.tif`): Ocean depth from the General Bathymetric Chart of the Oceans (GEBCO_2022 Grid).
- **Exclusive Economic Zones** (`wc_regions_clean.shp`): West Coast EEZ boundaries from Marineregions.org.
- **Species ranges:** Oyster SST and depth ranges were provided in the assignment instructions. Red abalone ranges (8–18°C, 0–24 m) are from SeaLifeBase.


## Author
Kailani Latimer ([GitHub](https://github.com/kailani-boop))

## References ****
- EDS 223 Homework 3 instructions: [EDS 223 HW 3](https://eds-223-geospatial.github.io/assignments/HW3.html)
- Gentry, R. R., Froehlich, H. E., Grimm, D., Kareiva, P., Parke, M., Rust, M., Gaines, S. D., & Halpern, B. S. (2017). Mapping the global potential for marine aquaculture. *Nature Ecology & Evolution*, 1, 1317–1324. [https://doi.org/10.1038/s41559-017-0257-9](https://doi.org/10.1038/s41559-017-0257-9)
- Hall, S. J., Delaporte, A., Phillips, M. J., Beveridge, M., & O'Keefe, M. (2011). *Blue Frontiers: Managing the Environmental Costs of Aquaculture*. The WorldFish Center, Penang, Malaysia.
- NOAA Coral Reef Watch. *5km Daily Global Satellite Sea Surface Temperature Anomaly, Version 3.1.* [https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php](https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php)
- GEBCO Compilation Group (2022). *GEBCO_2022 Grid.* doi:10.5285/e0f0bb80-ab44-2739-e053-6c86abc0289c. [https://www.gebco.net/data_and_products/gridded_bathymetry_data/](https://www.gebco.net/data_and_products/gridded_bathymetry_data/)
- Flanders Marine Institute. *Maritime Boundaries Geodatabase: Exclusive Economic Zones.* Marineregions.org. [https://www.marineregions.org/eez.php](https://www.marineregions.org/eez.php)
- Palomares, M. L. D., & Pauly, D. (Eds.). *SeaLifeBase*: *Haliotis rufescens* species summary. [https://www.sealifebase.ca/summary/Haliotis-rufescens.html](https://www.sealifebase.ca/summary/Haliotis-rufescens.html)
