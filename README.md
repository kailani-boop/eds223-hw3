# EDS 223 HW 3: Prioritizing Potential Aquaculture

## Purpose
This repo contains the third homework assignment for EDS 223, Geospatial Analysis and Remote Sensing. The course introduces the spatial modeling and analytic techniques of geographic information science to data science students, with an emphasis on spatial data models and the analytic operations they enable.

Marine aquaculture has the potential to play an important role in the global food supply as a more sustainable protein option than land-based meat production. The potential for marine aquaculture globally was based on multiple constraints, including ship traffic, dissolved oxygen, and bottom depth. It was found that global seafood demand could be met using less than 0.015% of the global ocean area. For this assignment, I'm tasked with determining which Exclusive Economic Zones (EEZ) on the West Coast of the US are best suited to developing marine aquaculture for several species of oysters and red abalone. Suitable locations will be determined based on range of suitable sea surface temperature (SST) and depth values for the species. 

## Repository Organization
```
EDS223-HW3
└─── README.md                    # Overview of the repository
└─── qmd/Rmd/Proj files
└─── red_abalone_analysis.qmd     # Quarto document with analysis
└───.gitignore
    └───data
        └─── wc_regions_clean.shp
        └─── depth.tif
        └─── average_annual_sst_2008.tif
        └─── average_annual_sst_2009.tif
        └─── average_annual_sst_2010.tif
        └─── average_annual_sst_2011.tif
        └─── average_annual_sst_2012.tif
```

## Data Access
Because the files are too large for GitHub, the `data/` folder is listed in `.gitignore`. To run the analysis, download the data from [this Google Drive link](https://drive.google.com/file/d/1u-iwnPDbe6ZK7wSFVMI-PpCKaRQ3RVmg/view), unzip it, and place the files in a `data/` folder at the root of this repository.

The data includes: *****
- **EJScreen** (`data/ejscreen/`): U.S. EPA environmental and demographic data at the census block group level (2023, Version 2.2).
- **HOLC redlining maps** (`data/mapping-inequality/`): Digitized HOLC grade boundaries for Los Angeles from the Mapping Inequality project.
- **Bike and pedestrian crashes** (`data/SWITRS_LA/`): Collision reports from 2020–2025 from the Statewide Integrated Traffic Records System (SWITRS), accessed through the Transportation Injury Mapping System (TIMS).

## Author
Kailani Latimer ([GitHub](https://github.com/kailani-boop))

## References ****
- EDS 223 Homework 3 instructions: [EDS 223 HW 3](https://eds-223-geospatial.github.io/assignments/HW3.html)
- U.S. Environmental Protection Agency. (2023). *EJScreen: Environmental Justice Screening and Mapping Tool* (Version 2.2). [https://pedp-ejscreen.azurewebsites.net/](https://pedp-ejscreen.azurewebsites.net/)
- U.S. Environmental Protection Agency. (2023). *EJScreen Technical Documentation, Version 2.2.*
- Nelson, R. K., Winling, L., Marciano, R., Connolly, N., et al. "Mapping Inequality." *American Panorama*, ed. R. K. Nelson and E. L. Ayers. [https://dsl.richmond.edu/panorama/redlining/](https://dsl.richmond.edu/panorama/redlining/)
- Safe Transportation Research and Education Center, University of California, Berkeley. *Transportation Injury Mapping System (TIMS)*. Statewide Integrated Traffic Records System (SWITRS) data, 2020–2025. [https://tims.berkeley.edu/](https://tims.berkeley.edu/)
- Taylor, N. L., Porter, J. M., Bryan, S., Harmon, K. J., & Sandt, L. S. (2023). Structural racism and pedestrian safety: Measuring the association between historical redlining and contemporary pedestrian fatalities across the United States, 2010–2019. *American Journal of Public Health*, 113(4).
- Gee, G. C. (2008). A multilevel analysis of the relationship between institutional and individual racial discrimination and health status. *American Journal of Public Health*, 98(Supplement_1), S48–S56.
- Nardone, A., Rudolph, K. E., Morello-Frosch, R., & Casey, J. A. (2021). Redlines and greenspace: The relationship between historical redlining and 2010 greenspace across the United States. *Environmental Health Perspectives*, 129(1), 017006.
- Hoffman, J. S., Shandas, V., & Pendleton, N. (2020). The effects of historical housing policies on resident exposure to intra-urban heat: A study of 108 US urban areas. *Climate*, 8(1), 12.
