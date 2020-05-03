---
layout: post
title: Water Hyacinth Dispersion Changes
image: /img/icon_wh.JPG
tags: [Water hyacinth, LANDSAT, eCognition, R, object-based classification, Ethiopia]
bigimg: /img/wh_main2.jpg
comments: true
---

Water hyacinth (Eichhornia crassipes) is called the world’s worst aquatic weed because of its extremely rapid growth. It creates thick mats that deplete nutrients of freshwater by blocking oxygen and solar radiation and consequently induces habitat destruction. However, field observation of water hyacinth is difficult due to its habitat feature. Therefore, the number of remote sensing technologies applications on water hyacinth monitoring has increased.

![map_frame](/img/frame_main.jpg)

The aim of my master thesis was to compare pixel-based classification technologies to object-based classification that were used in previous studies for the water hyacinth detection using satellite images and to analyze water hyacinth dispersion changes in Lake Tana of Ethiopia. Landsat-5 TM (2011) and Landsat-8 OLI (2013-2018) imagery were used for the analysis.

![map_ndvi](/img/20180924_mappedndvi.jpg)
![map_fai](/img/20180924_mappedfai.jpg)

Three pixel-based classification techniques (slicing with NDVI threshold, slicing with FAI combined with NDWI(Green,SWIR), and maximum likelihood) and Object-based classification approach were applied to the sample image.
For pixel-based classifications, NDVI showed the lowest overall accuracy (90.8%), while maximum likelihood showed better overall accuracy (94.5%) and FAI combined with NDWI(Green,SWIR) showed similar overall accuracy (95.3%). For object-based classification with a ruleset, it showed the highest overall accuracy (98.9%) for the detection of water hyacinth area. Therefore, object-based image classification proved to be a reliable technology for water hyacinth detection.

**2011~2018 classification result**

![habitat](/img/habitat.gif)

Images from 2011 to 2018 were classified using the object-based image classification technique. The results confirmed that the water hyacinth infection has been increased in Lake Tana area. Initial water hyacinth infection area in 21.09.2011 was 592 ha and it increased to 3086 ha in 24.09.2018. Seasonal fluctuations were observed in the result, that grows during the rainy season and declines during the dry season due to the period of dormancy and removal actions. It demonstrates that one-time measure for water hyacinth is not enough and therefore, the importance of continuous removal campaigns must be publicized to local communities and municipalities.
