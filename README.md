# Earth Observation Data Analysis - Project :earth_africa: :artificial_satellite:
Homeworks for the course **Earth Observation Data Analysis**, 2020, Sapienza University of Rome

This repository contains three pdf files, one for each project undertaken during the course Earth Observation Data Analysis (Control Engineering, DIAG, Sapienza University of Rome).

## Usage
All the homeworks have been done through the use of the Sentinel Application Platform (SNAP) toolbox, an open source software which is used for Earh Observation processing and analysis. You can finde more information [here](http://step.esa.int/main/toolboxes/snap/) and you can download it [here](http://step.esa.int/main/download/snap-download/).

## Data download
The satellite image data are available from the following sources:
* MODIS data from Terra and Aqua satellites from [NASA LAADS DAAC](https://ladsweb.modaps.eosdis.nasa.gov/search/)
* MSI Sentinel-2 data from [Copernicus](https://scihub.copernicus.eu/)
* SAR Sentinel-1 data from [Copernicus](https://scihub.copernicus.eu/)

## Homework 01: Remote sensing of vegetation from MODIS :leaves: :fallen_leaf:

Modis images from [NASA LAADS DAAC](https://ladsweb.modaps.eosdis.nasa.gov/search/).
The objective of this homework was the quantitative detection of the vegetation coverage between two MODIS images representing the same region of interest (ROI) in the winter and summer seasons.


1. Download of a MODIS image at 1-km resolution over a ROI during summer season.
   1. Quality check
   2. Data analysis (spectrum, histogram, profile tools)
   3. Channel data correlation of whole image and selected ROI
   4. Principal Component Analysis computation
   5. Unsupervised and supervised classification with sea, land and cloud classes
2. Application of the formulas of 2-band and 3-band vegetation index (VI)
3. Unsupervised classification using a VI index in place of a MODIS channel
4. Application of VI indices to the second MODIS image in the winter season
5. Quantitative change detection of the vegetation coverage class by reprojecting the two MODIS images in July and January.

Here is the vegetation coverage of Italy in July and January seasons:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/julyReprojection.jpg" width="420"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/januaryReprojection.jpg" width="400">

Quantitative change detection:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/legenda.jpg" width="512">                                                                                                                       
## Homework 02: Surface mapping from MSI Sentinel-2 Data :herb: :droplet:

Sentinel-2 MSI images downloaded from [Copernicus](https://scihub.copernicus.eu/).

The objective was the estimation of vegetation cover, inland water and chlorophyll-a sea concentration of Sentinel-2 MSI data and supervised classification within a ROI.

1. Data exploration: download of two summer and winter MSI images choosing a coastal target area (Tiber river estuary in Italy).

Winter images of Ronciglione lake:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/february_RGB.jpg" width="420"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/february_ronciglione_RGB.jpg" width="400">

Summer images of Ronciglione lake:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/july17_RGB.jpg" width="420"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/july17_ronciglione_RGB.jpg" width="400">

   1. Combination of the B2, B3, B4 channels to create an RGB image
   2. L2 MSI products for scene classification masks: cloud, vegetation, soil, water.
   3. SNAP Graph Builder tool applied to a subset around a lake or a river, resampling of the channels at 10 meters and their visualization.

  
2. Water and vegetation normalized index: NDWI and NDWI2 on winter product. 
   1. Apply NDWI to highlight water content in the leaves and NDWI2 to build a water mask estimate chlorophyll-a (Chl-a) and total suspended sediments (TSS).
   2. Computation of NDVI on winter and summer MSI resampled products.
   
February and August water masks and difference water mask:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/february_ronciglione_NDWI2_waterMask.jpg" width="320"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/august_ronciglione_NDWI2_waterMask.jpg" width="300"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/waterMask_difference_feb-aug_ronciglione.jpg" width="300"> 

3. Sea Chlorophyll-a and sediment estimation of an estuary/delta
   1. EmpReg regressive algorithm to Chl-a and TSS estimation
   2. Comparison with MCI (Maximum Chlorophyll Index) plugged-in algorithm
   3. Comparison with Chl-a and TSS products (from [Copernicus Marine Service](http://marine.copernicus.eu))

February and August Tiber river images:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/tevere_febbraio_RGB.jpg" width="320"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/tevere_agosto_RGB.jpg" width="300">

Chlorophyll-a and Total Suspended Sediments differences between the two seasons:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/C_chla_difference.jpg" width="300"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/TSM_difference.jpg" width="300">

4. Scene classification
   1. Scene classification masks over an L2 MSI summer image defining vegetation, water, urban and bare soil as training areas.
   2. Reprojection and SNAP supervised classification algorithms (Maximum Likelihood and Random Forest).
   3. Comparison between the classifiers
  
<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/ronciglione_class_masks_SUBSET.jpg" width="250"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/ronciglione_class_ML_SUBSET.jpg" width="250"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/ronciglione_class_RF_SUBSET.jpg" width="250">


## Homework 03: Surface detection from SAR Sentinel-1 Data 

Images downloaded from [Copernicus](https://scihub.copernicus.eu/) and provided by ESA.

1. Earthquake detection by SAR differential interferometry (Amatrice Earthquake in 2016, Italy) 	:world_map:
   1. DInSAR processing steps

Displacement map:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/displacement.jpg" width="300">

Displacement map terrain corrected and displacement map in Google Earth:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/displacement_terrain_correction_JET_palette.jpg" width="300"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/googleearth.jpg" width="320">

2. Ship detection by SAR backscattering (Messina strait in 2020, Italy) :ship:
   1. SAR processing steps

Detected ship in the Messina strait:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/ship%20detection_db.jpg" width="500">

3. Flood detection by SAR backscattering (Flood in Mozambico, 2019) :cloud_with_lightning_and_rain:
   1. DInSAR processing steps
   
Pre-event and post-event acquisitions:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/flood_intensity_13_3_19.jpg" width="300"> <img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/flood_intensity_19_3_19.jpg" width="320">

Change detection after color manipulation:

<img src="https://github.com/GioiaMancini/EarthObservationDataAnalysis/blob/main/docs/flood_RGB.jpg" width="500">



