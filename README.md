# Earth Observation Data Analysis - Projects
Homeworks for the course Earth Observation Data Analysis, 2020, Sapienza University of Rome

This repository contains three pdf files, one for each project undertaken during the course Earth Observation Data Analysis (Control Engineering, DIAG, Sapienza University of Rome).

# Usage
All the homeworks have been done through the use of the Sentinel Application Platform (SNAP) toolbox, an open source software which is used for Earh Observation processing and analysis. You can finde more information [here](http://step.esa.int/main/toolboxes/snap/) and you can download it [here](http://step.esa.int/main/download/snap-download/).

# Homework 01: Remote sensing of vegetation from MODIS

Modis images from [NASA LAADS DAAC](https://ladsweb.modaps.eosdis.nasa.gov/search/).
The objective of this homework was the quantitative detection of the vegetation coverage between two MODIS images representing the same region of interest (ROI) in the winter and summer seasons.

Markup : 1. Download of a MODIS image at 1-km resolution over a ROI during summer season.
              1. Quality check
              2. Data analysis (spectrum, histogram, profile tools)
              3. Channel data correlation of whole image and selected ROI
              4. Principal Component Analysis computation
              5. Unsupervised and supervised classification with sea, land and cloud classes
          2. Application of the formulas of 2-band and 3-band vegetation index (VI)
          3. Unsupervised classification using a VI index in place of a MODIS channel
          4. Application of VI indices to the second MODIS image in the winter season
          5. Quantitative change detection of the vegetation coverage class by reprojecting the two MODIS images over the same grid in a ROI.
exploration of MODIS satellite data and the application of SNAP classification tools and vegetation indices. We 

# Homework 02: Surface mapping from MSI Sentinel-2 Data

Sentinel-2 MSI images downloaded from [Copernicus](https://scihub.copernicus.eu/).

The objective was the estimation of vegetation cover, inland water and chlorophyll-a sea concentration of Sentinel-2 MSI data and supervised classification within a ROI.



# Homework 03: Surface detection from SAR Sentinel-1 Data

Images downloaded from [Copernicus](https://scihub.copernicus.eu/) and provided by ESA.
