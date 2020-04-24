---
layout: post
title: Soil Erosion Risk Analysis
image: /img/soil_sat.png
tags: [LULC, Soil erosion risk, LANDSAT]
comments: true
---
The overall purpose of the study was the soil erosion risk analyis to provide land use planning support for the surrounding area of Lake Waging, located in the district of Traunstein, Bavaria, Germany.

![Satellite](/img/soil_sat.png)

The land use of Waging region is constantly changing. Intensive farming, housing and development of infrastructure take place at the same time and challenge the aesthetic values of the present. However, there has been still no research of the changes of land-use change in Lake waging region. Now, a multi-disciplinary approach is required.
Therefore, the study seeks to understand the risk of soil erosion in this area, assess soil erosion risk regarding agriculture and to make management strategies that consider mitigation.

In the study, the USLE (Universal Soil Loss Equation) was applied. USLE is a parametric model that calculates the average annual soil erosion by precipitation per unit area. It is used to measure the spatial distribution of soil loss and is derived from geographical information that includes land coverage, soil type, precipitation and topography.


**Land Use Clasification**

![soil](/img/soil_landuse.jpg)

Six classes, including crop field, maize field, forest, grassland, urban area and water bodies, were used to determine erosion risk. First, the whole map was divided into land and water. Vegetation and non-vegetation areas were assigned based upn normalized difference vegetation index (NDVI) thresholds. Forest and non-forest area were determined by the mean of shortwave infrared and brightness. Non-forest was classified as grassland and cropland according to their respective NDVI values. Since the satellite image was taken in October, harvested cropland with low vegetation was assumed to be maize fields.

**Land Use Clasification**

![soil_universe](/img/soil_universe.png)

The K-factor represents soil erodibility, defined as the soil loss rate per erosion index unit (Wischmeier et al., 1978). In this study, K-factors were already assigned from empirical knowledge.
The R-factor, the rainfall and runoff factor, defined as the number of rainfall erosion index units, plus a factor for runoff from snowmelt of applied water (Wischmeier et al., 1978). R-factors within Bavaria have already been assigned by Schwertmann et al. (1987). Therefore R-factor was assigned according to municipal area.
The S-factor is the slope-steepness factor, which is defined as the ratio of soil loss from the field slope gradient to that from 9 percent slope under otherwise identical conditions (Wischmeier et al., 1978). In this study, a digital elevation model (DEM) was used and S assigned according to Auerswald et al. (1986).
L factor is the slope-length factor, which is defined as the ratio of soil loss from the field slope length (Wischmeier et al., 1978).


**Soil Erosion Risk**

![soil_erosion](/img/soil_risk.jpg)

The annual erosion risk assessment for the Lake Waging region, expressed in ton/ha/year, is displayed. The average soil erosion risk of Lake Waging area is calculated as 1878 ton/ha/year. Crop (without maize) fields are at risk of losing 1575 ton/ha/year, maize fields by 11592 ton/ha/year, forest by 0.283 ton/ha/year, grassland by 0.743 ton/ha/year, urban areas by 0.199 ton/ha/year, and water by 0.001 ton/ha/year.
