# EDS 223 HW 2: Exploring Patterns of Environmental Justice in LA County

## Purpose
This repo contains the second homework assignment for EDS 223, Geospatial Analysis and Remote Sensing. The course introduces the spatial modeling and analytic techniques of geographic information science to data science students, with an emphasis on spatial data models and the analytic operations they enable.

This assignment explores the legacy of historical redlining in Los Angeles County. Part 1 examines how Home Owners' Loan Corporation (HOLC) grades from the 1930s relate to present-day environmental and socioeconomic conditions (PM2.5, low life expectancy, and low income). Part 2 examines how HOLC grades relate to bike and pedestrian crashes and fatalities from 2020–2025.

## Repository Organization
```
eds223-hw2
│   README.md           # Overview of the repository
│   HW2.qmd             # Quarto document with analysis
│   Rmd/Proj files
│
└───.gitignore
     └───data
         └───ejscreen
         └───SWITRS_LA
         └───mapping-inequality
```

## Data Access
Because the files are too large for GitHub, the `data/` folder is listed in `.gitignore`. To run the analysis, download the data from [this Google Drive link](https://drive.google.com/file/d/1nG6Nj1bXfzQFOVMO8Km3eNy4SWu1YcIQ/view?usp=sharing), unzip it, and place the files in a `data/` folder at the root of this repository.

The data includes:
- **EJScreen** (`data/ejscreen/`): U.S. EPA environmental and demographic data at the census block group level (2023, Version 2.2).
- **HOLC redlining maps** (`data/mapping-inequality/`): Digitized HOLC grade boundaries for Los Angeles from the Mapping Inequality project.
- **Bike and pedestrian crashes** (`data/SWITRS_LA/`): Collision reports from 2020–2025 from the Statewide Integrated Traffic Records System (SWITRS), accessed through the Transportation Injury Mapping System (TIMS).

## Author
Kailani Latimer ([GitHub](https://github.com/kailani-boop))

## References
- EDS 223 Homework 2 instructions: [https://eds-223-geospatial.github.io/assignments/HW2V2.html](https://eds-223-geospatial.github.io/assignments/HW2V2.html)
- U.S. Environmental Protection Agency. (2023). *EJScreen: Environmental Justice Screening and Mapping Tool* (Version 2.2). [https://pedp-ejscreen.azurewebsites.net/](https://pedp-ejscreen.azurewebsites.net/)
- U.S. Environmental Protection Agency. (2023). *EJScreen Technical Documentation, Version 2.2.*
- Nelson, R. K., Winling, L., Marciano, R., Connolly, N., et al. "Mapping Inequality." *American Panorama*, ed. R. K. Nelson and E. L. Ayers. [https://dsl.richmond.edu/panorama/redlining/](https://dsl.richmond.edu/panorama/redlining/)
- Safe Transportation Research and Education Center, University of California, Berkeley. *Transportation Injury Mapping System (TIMS)*. Statewide Integrated Traffic Records System (SWITRS) data, 2020–2025. [https://tims.berkeley.edu/](https://tims.berkeley.edu/)
- Taylor, N. L., Porter, J. M., Bryan, S., Harmon, K. J., & Sandt, L. S. (2023). Structural racism and pedestrian safety: Measuring the association between historical redlining and contemporary pedestrian fatalities across the United States, 2010–2019. *American Journal of Public Health*, 113(4).
- Gee, G. C. (2008). A multilevel analysis of the relationship between institutional and individual racial discrimination and health status. *American Journal of Public Health*, 98(Supplement_1), S48–S56.
- Nardone, A., Rudolph, K. E., Morello-Frosch, R., & Casey, J. A. (2021). Redlines and greenspace: The relationship between historical redlining and 2010 greenspace across the United States. *Environmental Health Perspectives*, 129(1), 017006.
- Hoffman, J. S., Shandas, V., & Pendleton, N. (2020). The effects of historical housing policies on resident exposure to intra-urban heat: A study of 108 US urban areas. *Climate*, 8(1), 12.
