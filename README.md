This public repository contains data sets used in courses I teach.  Every file can be downloaded directly from

```
https://dyerlabteaching.github.io/CourseData/<Category>/<file>
```

For example, in `R`:

```r
library( tidyverse )
url <- "https://dyerlabteaching.github.io/CourseData/Miscellaneous/Beer_Styles.csv"
beer <- read_csv( url )
```

Files here never change once published.  If a data set needs to be updated, it is added as a new file (e.g., `arapat_v2.csv`) so that older code keeps working.



## Environmental

Random environmental data sets.

- [`RiceRivers_2014.csv`](https://dyerlabteaching.github.io/CourseData/Environmental/RiceRivers_2014.csv): Atmospheric and water-quality measurements from the instrument station at the VCU [Rice Rivers Center](https://ricerivers.vcu.edu) on the James River, recorded every 15 minutes from 1 January to 27 March 2014 (8,197 records).  Columns include air temperature (°F), relative humidity, barometric pressure, rain (in), wind speed (mph) and direction, PAR, and water temperature (°C), specific conductance, salinity, pH, turbidity, chlorophyll *a*, blue-green algae, dissolved oxygen, and depth.  The units are part of each column name.  `DateTime` is text (e.g., `1/1/2014 12:00:00 AM`) and needs to be parsed.  Snapshot of the Google Sheet previously used in class.  *Used in: Tidyverse.*


## Genetic

Data sets that contain genetic marker data.  These commonly use the [gstudio](https://github.com/dyerlab/gstudio) package for analyses.

- [`mv_genos.csv`](https://dyerlabteaching.github.io/CourseData/Genetic/mv_genos.csv): Multivariate genotypes for the Sonoran Desert bark beetle *Araptus attenuatus* from Baja California (the `arapat` data in `gstudio`, converted with `to_mv()`).  Each of the 363 rows is an individual and each of the 58 columns (`L1`–`L58`) is an allele, coded 0, 0.5, or 1 as the proportion of that individual's genotype carrying the allele.  *Used in: Ordination.*


## Spatial

Data specifically used in demonstrating spatial analyses:

- [`alt_22.tif`](https://dyerlabteaching.github.io/CourseData/Spatial/alt_22.tif): A geotiff from WorldClim for ground elevation (m) measured on 1km grids (30 arc-second) covering Baja California, Mexico, and the surrounding region (120°W–90°W, 0°–30°N; WGS84).  *Used in: Raster-Data.*
- [`arapat.csv`](https://dyerlabteaching.github.io/CourseData/Spatial/arapat.csv): Locations of the 39 sampling sites for the bark beetle *Araptus attenuatus* in Baja California, with columns `Stratum` (site ID), `Longitude`, and `Latitude` (decimal degrees, WGS84).  *Used in: Data-Containers, GGPlot2_Graphics.*
- [`AraptusDispersalBias.csv`](https://dyerlabteaching.github.io/CourseData/Spatial/AraptusDispersalBias.csv): Sex-ratio and habitat data for 31 *Araptus attenuatus* sites in Baja California.  Columns are `Site`, counts of `Males` and `Females`, habitat `Suitability`, the male:female ratio `MFRatio`, genetic variation in the beetle (`GenVarArapat`) and its host plant *Euphorbia lomelii* (`GenVarEuphli`), and `Latitude`/`Longitude` (decimal degrees, WGS84).  *Used in: Spatial-Points, Raster-Data.*
- [`Richmond_Dogwoods.csv`](https://dyerlabteaching.github.io/CourseData/Spatial/Richmond_Dogwoods.csv): Locations of 58 dogwood maternal trees from an ongoing study along an urban-to-forest transect in and south of Richmond, Virginia.  Columns are `Type` (the habitat the tree was sampled in: `Cultivar` for 32 trees in suburban and urban Richmond and Chesterfield, `Native` for 26 trees in Pocahontas State Park), `Tree` (an ID), `Longitude` and `Latitude` (decimal degrees, WGS84), and `N` (the number of offspring, as seeds, collected from that maternal tree).  *Used in: Shapefiles.*
- [`Richmond_Roads.zip`](https://dyerlabteaching.github.io/CourseData/Spatial/Richmond_Roads.zip): Zipped shapefile of road centerlines (carriageways) for Richmond, Virginia, from the City of Richmond GIS Department (2020).  Unzips into a `Centerlines-shp/` folder containing `tran_Carriageway.shp` and its companion files (plus a `__MACOSX/` folder you can ignore).  *Used in: Shapefiles.*
- [`Richmond_ZoningDistricts.zip`](https://dyerlabteaching.github.io/CourseData/Spatial/Richmond_ZoningDistricts.zip): Zipped shapefile of zoning district polygons for Richmond, Virginia, from the City of Richmond GIS Department (2020).  Unzips directly into a set of `Zoning_Districts.*` files (no subfolder).  *Used in: Shapefiles.*
- [`Richmond_ZoningCodes.csv`](https://dyerlabteaching.github.io/CourseData/Spatial/Richmond_ZoningCodes.csv): Lookup table translating the 27 zoning codes in `Richmond_ZoningDistricts.zip` (`Name`, e.g., `R-53`) to a readable `Category` (e.g., *Single Family Residential*).  Join it to the districts by `Name`.  *Used in: Shapefiles.*


## Miscellaneous

Other random data sets.

- [`Beer_Styles.csv`](https://dyerlabteaching.github.io/CourseData/Miscellaneous/Beer_Styles.csv): Ranges of brewing characteristics for 100 beer styles.  For each style (`Styles`) and yeast type (`Yeast`: Ale, Lager, or Either), it gives the minimum and maximum alcohol by volume (`ABV`), bitterness (`IBU`), color (`SRM`), original gravity (`OG`), and final gravity (`FG`).  *Used in: Correlation, Ordination.*
- [`DietData.csv`](https://dyerlabteaching.github.io/CourseData/Miscellaneous/DietData.csv): Weight loss for 76 adults on one of three diets.  Columns are `Person`, `gender` (0/1), `Age` (years), `Height` (cm), `pre.weight` and `weight6weeks` (kg, before and after six weeks), and `Diet` (1, 2, or 3).  *Used in: Analysis-of-Variance.*
- [`EconomistData.csv`](https://dyerlabteaching.github.io/CourseData/Miscellaneous/EconomistData.csv): Human development and perceived corruption for 173 countries, from a 2011 graphic in *The Economist*.  Columns are `Country`, `HDI.Rank`, the Human Development Index (`HDI`), the Corruption Perceptions Index (`CPI`), and `Region`.  The first, unnamed column is a row number.  *Used in: GGPlot2_Graphics.*
