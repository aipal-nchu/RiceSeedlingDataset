# Data Preprocessing
This page presents the detail of data preprocessing  

---

**The workflow of semi-auto annotation**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/Preprocessing-2.png" width="768" height="441">



## Workflow
  1. [Image stitching](#1-image-stitching)
  2. [Calculate Index](#2-calculate-index)
  3. [Image Binarization](#3-image-binarization)
  4. [Morphological Process](#4-morphological-process)
  5. [Contour Feature Extraction](#5-contour-feature-extraction)  

### 1. Image stitching
Images are stiched using [Agisoft Metashape](https://www.agisoft.com/) from a series of nadir-view UAV images.  

### 2. Calculate Index  
The excess green minus excess red (ExGR) index is introduced to enhance the feature of vegatation.  

<img src="https://latex.codecogs.com/svg.latex?ExGR%20=%203\times%20G-2.4\times%20R-G" width="400">  

### 3. Image Binarization
[Yen’s thresholding method](https://dx.doi.org/10.1109/83.366472) was applied to obtain a binary map. In practice, we adopted the binarizing function from [scikit-image](https://scikit-image.org/docs/dev/api/skimage.filters.html?highlight=otsu#skimage.filters.threshold_yen), function name: `skimage.filters.threshold_yen`.

### 4. Morphological Process


### 5. Contour Feature Extraction

