# Prioritizing potential aquaculture

<img src="https://images.unsplash.com/photo-1519122295308-bdb40916b529?q=80&w=3174&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="marine aquaculture" width="800"/>

Image credits: [Unsplash](https://unsplash.com/photos/aerial-photography-of-white-frames-on-top-of-water-eUfnha6ev9g)

## About

Marine aquaculture has the potential to play an important role in the global food supply as a more sustainable protein option than land-based meat production (Hall et al. 2011). Gentry et al. mapped the potential for marine aquaculture globally based on multiple constraints, including ship traffic, dissolved oxygen, and bottom depth. They found that global seafood demand could be met using less than 0.015% of the global ocean area (Gentry et al. 2017). 

This repository contains a Quarto document and rendered HTML file for my analysis that determines which Exclusive Economic Zones (EEZ) on the West Coast of the US are best suited to developing marine aquaculture for several species of oysters and Dungeness crabs. Through my analysis, I use key concepts in geospatial analysis including:
- combining vector/raster data
- resampling raster data
- masking raster data
- map algebra
- function buildingg

## Repository content and structure

```
EDS223-HW4
│   .gitignore
│   HW4.html
│   HW4.qmd
│   README.md
│
└───data
    │   wc_regions_clean.dbf
    │   wc_regions_clean.prj
    │   wc_regions_clean.shp
    │   wc_regions_clean.shx
    │   depth.tif
    │   average_annual_sst_2008.tif
    │   average_annual_sst_2009.tif
    │   average_annual_sst_2010.tif
    │   average_annual_sst_2011.tif
    └───average_annual_sst_2012.tif
```

All of the code for my analysis can be found in HW4.qmd. This has been rendered into a report, HW4.html. 

## Data details

#### Suitable locations
Suitable locations are determined based on range of suitable sea surface temperature (SST) and depth values for each species. Suitable growing conditions are found on [SeaLifeBase](https://www.sealifebase.ca/search.php).

#### Sea Surface Temperature

I use average annual sea surface temperature (SST) from the years 2008 to 2012 to characterize the average sea surface temperature within the west coast regions. The data was originally generated from [NOAA’s 5km Daily Global Satellite Sea Surface Temperature Anomaly v3.1](https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php).

#### Bathymetry

To characterize the depth of the ocean, I use the [General Bathymetric Chart of the Oceans (GEBCO)](https://www.gebco.net/data_and_products/gridded_bathymetry_data/#area).

#### Exclusive Economic Zones

I designate maritime boundaries using Exclusive Economic Zones off of the west coast of US from [Marineregions.org](https://www.marineregions.org/eez.php).

## References

#### Data

**Suitable Growing Conditions:** Palomares, M.L.D. and D. Pauly. Editors. 2024. SeaLifeBase. World Wide Web electronic publication. www.sealifebase.org, version (08/2024). Accessed 2024-11-09.

**Sea Surface Temperature:** NOAA Coral Reef Watch. 2018, updated daily. NOAA Coral Reef Watch Version 3.1 5km Daily Global Satellite Sea Surface Temperature Anomaly Product, 2008-2012. College Park, Maryland, USA: NOAA Coral Reef Watch. Data set accessed 2024-11-09 at https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php.

**Bathymetry:** GEBCO Compilation Group (2024) GEBCO 2024 Grid (doi:10.5285/1c44ce99-0a0d-5f4f-e063-7086abc0ea0f). Data set accessed 2024-11-09 at https://www.gebco.net/data_and_products/gridded_bathymetry_data/#area.

**Exclusive Economic Zones:** Marine Regions (2024) Flanders Marine Institute. Data set accessed 2024-11-09 at https://www.marineregions.org/eez.php.

#### Literature

Hall, S. J., Delaporte, A., Phillips, M. J., Beveridge, M. & O’Keefe, M. Blue Frontiers: Managing the Environmental Costs of Aquaculture (The WorldFish Center, Penang, Malaysia, 2011).

Gentry, R. R., Froehlich, H. E., Grimm, D., Kareiva, P., Parke, M., Rust, M., Gaines, S. D., & Halpern, B. S. Mapping the global potential for marine aquaculture. Nature Ecology & Evolution, 1, 1317-1324 (2017).

## Acknowledgements

This repository was created as an assignment for the graduate course EDS 223: Geospatial Analysis and Remote Sensing in the [Masters of Environmental Data Science (MEDS) program](https://bren.ucsb.edu/masters-programs/master-environmental-data-science), taught by [Dr. Ruth Oliver](https://bren.ucsb.edu/people/ruth-oliver).


