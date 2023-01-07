# Reproduction Package Eurodeer paper n. 016

Datasets and analysis scripts of Salvatori, De Groeve et al. (2022).

# Directory Structure 

The repository contains the following files and directories:


|  file(s)/directories                   |   description                                                                                      |
|----------------------------------------|----------------------------------------------------------------------------------------------------|
| **[./code/0_data_preparation.sql](https://github.com/EUROMAMMALS/RP016/blob/master/code/0_data_preparation.sql)**      | SQL-query extracting the raw data from the eurodeer database                                       |
| **[./code/0_data_preparation.R](https://github.com/EUROMAMMALS/RP016/blob/master/code/0_data_preparation.R)**        | preparation of gps_data/kde_data: calculation of HRs & intersection of GPS/KDE with TCD/CLC   | 
| **[./code/1_mismatch_and_modelling.Rmd](https://github.com/EUROMAMMALS/RP016/blob/master/code/1_mismatch_and_modelling.Rmd)**| CLC/TCD mismatch analysis and statistical modelling of day-night forest use in roe and red deer    | 
| **[./code/2_patchsize.Rmd](https://github.com/EUROMAMMALS/RP016/blob/master/code/2_patchsize.Rmd)**   | patch size analysis                                                                                | 
| **[./code/3_validation_gps.Rmd](https://github.com/EUROMAMMALS/RP016/blob/master/code/3_validation_gps.Rmd)**   | Validation confusion matrices of mismatching GPS location                                          | 
| **[./code/fncs/](https://github.com/EUROMAMMALS/RP016/blob/master/code/fncs/)**     | functions used in step 1, 2, 3                                                                     | 
| **[./data/raw/gps/](https://github.com/EUROMAMMALS/RP016/blob/master/data/raw/gps/)**       | RDS; raw gps data of roe and red deer as extracted from the eurodeer database                      |  
| **[./data/raw/rasters/](https://github.com/EUROMAMMALS/RP016/blob/master/data/raw/rasters/)**       | TIF; study area extracts of TCD and CLC rasters                                                    |  
| **[./data/1_analysis/](https://github.com/EUROMAMMALS/RP016/blob/master/data/1_analysis/)**             | CSV; absolute and proportion of forest and open habitat calculated for GPS/KDE with TCD/CLC        |  
| **[./data/2_patchsize/](https://github.com/EUROMAMMALS/RP016/blob/master/data/2_patchsize/)**             | CSV; GPS locations with patch sizes                                                                |  
| **[./data/3_validation_gps/](https://github.com/EUROMAMMALS/RP016/blob/master/data/3_validation_gps/)**         | CSV; 100 random gps locations per population, validated using a satellite layer as ground truth    |  
| **[./code/results/](https://github.com/EUROMAMMALS/RP016/blob/master/code/results/)**       | DIR; empty directory to store outputs      


# Directory tree 

```
. 
├── README.md
├── RP016.Rproj
├── code
│   ├── 0_data_preparation.R
│   ├── 0_data_preparation.sql
│   ├── 1_mismatch_and_modelling.R
│   ├── 2_patchsize.Rmd
│   ├── 2_patchsize.html
│   ├── 3_validation_gps.Rmd
│   ├── 3_validation_gps.html
│   └── fncs
│       ├── 00_basic.R
│       ├── 01_compute_kde.R
│       ├── 02_reclass_rast.R
│       ├── 03_intersect_rast_gps.R
│       ├── 04_intersect_rast_kde.R
│       ├── 11_boxplot_mismatch.R
│       ├── 11_confusion_scheme.R
│       ├── 11_forest_proportion_barboxplot.R
│       ├── 11_model_selection.R
│       ├── 11_plot_predictions.R
│       ├── 11_proportion_plot.R
│       └── 21_patch_statistics.R
├── data
│   ├── 1_mismatch_and_modelling
│   │   ├── gps_data.csv
│   │   ├── gps_for_model.csv
│   │   ├── kde_data.csv
│   │   └── kde_for_model.csv
│   ├── 2_patchsize
│   │   ├── red.csv
│   │   └── roe.csv
│   ├── 3_validation_gps
│   │   ├── red.csv
│   │   └── roe.csv
│   └── raw
│       ├── gps
│       │   ├── red_rds
│       │   └── roe_rds
│       └── rasters
│           ├── red_raster_clc_population_14.tif
│           ├── red_raster_clc_population_17.tif
│           ├── red_raster_clc_population_21.tif
│           ├── red_raster_clc_population_3.tif
│           ├── red_raster_clc_population_8.tif
│           ├── red_raster_tcd_population_14.tif
│           ├── red_raster_tcd_population_17.tif
│           ├── red_raster_tcd_population_21.tif
│           ├── red_raster_tcd_population_3.tif
│           ├── red_raster_tcd_population_8.tif
│           ├── roe_raster_clc_population_1.tif
│           ├── roe_raster_clc_population_15.tif
│           ├── roe_raster_clc_population_2.tif
│           ├── roe_raster_clc_population_25.tif
│           ├── roe_raster_clc_population_8.tif
│           ├── roe_raster_tcd_population_1.tif
│           ├── roe_raster_tcd_population_15.tif
│           ├── roe_raster_tcd_population_2.tif
│           ├── roe_raster_tcd_population_25.tif
│           └── roe_raster_tcd_population_8.tif
└── results
```

# References 

Salvatori M, De Groeve J, van Loon E, De Baets B, Morellet N, Focardi S, Bonnot NC,  Gehr B, Griggio M, Heurich M, Kroeschel M, Licoppe A, Moorcroft PRM, Pedrotti L, Signer J, Van de Weghe N, & Cagnacci F (2022) Day versus night use of forest by red and roe deer as determined by Corine Land Cover and Copernicus Tree Cover Density: assessing use of geographic layers in movement ecology. Landscape Ecology, 37: 1453-1468
