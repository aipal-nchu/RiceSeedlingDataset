# Rice Shoot Counting Datasets
A repository to open rice shoot counting dataset.  

---

## Contents
  1. [Data Download Link (Google Drive)](#data-download-link-google-drive)
  2. [Rice Shoot Dataset](#rice-shoot-dataset)
  3. [CNN Classification Model](#a-simple-example-of-cnn-classification-model)
  4. [Detection Demo Dataset](#detection-demo-dataset)

## Data Download Link (Google Drive)
**[RiceShootClassification_2class.tgz (uncompressed size 426MB)](https://rebrand.ly/riceshootdataset_2class)**
> This file includes two folders: riceshoot and bareland. Train-val and test datasets are all included.

**[RiceShootCouning.tgz (uncompressed size 48.5MB)](https://rebrand.ly/RiceshootcountingTgzE3355)**
> This file contains 8 detection demo images and the corresponging PASCAL VOC xml format annotations.

**[2018-08-07_ARI80_20m_Orthomosaic.tif (size 465MB)](https://rebrand.ly/20180807ARI80Orthomosaic)**
> This is the orthomosaic image of the field of number 80, TARI, with TWD97 / TM2 zone 121 (EPSG:3826) projection. Image size is 19406 x 10413 pixels.  

**An overview of the region of different datasets**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/Datasets_Area_Overview.png" width="768">  
> An overview of the field no. 80 (cyan bounding area) in TARI, Taichung. Image acquired on August 7, 2018. The green bounding area represents the area for training-validation dataset, and the red bounding area represents the area for object detection demonstration dataset.

## Rice Shoot Dataset
  This dataset contains two classes: 
   - `rice shoot`
   - `bare land`

**An overview of image dataset**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/dataset.png" width="768">



**The number of images used for training, validation, and testing in the rice shoot dataset.**
| Class       | Training Samples | Validation Samples | Testing Samples | Total Samples |
|:-----------:|:----------------:|:------------------:|:---------------:|:-------------:|
| **Rice Shoot**  | 22,438 | 561   | 5,048 | 28,047 |
| **Bare Land**   | 21,265 | 532   | 4,784 | 26,581 |
| **Total**       | 43,703 | 1,093 | 9,832 | 54,628 |  


## A Simple Example of CNN Classification Model
**The architecture of the proposed network for rice shoot classification**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/Network Architechture-2class.png" width="768">

## Detection Demo Dataset
This dataset is used for patch-based object-detection scenario.  
- 8 images.
- 8x8 meters region.
- 1527x1527 pixels.
- PASCAL VOC xml format annotation.

**An overview of 8 detection demo images**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/DemoClip.png" width="768">


| number | original image | result image |
|:-:|:-:|:-:|
|1|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/1.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/1_bbox.jpg" width="300">|
|2|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/2.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/2_bbox.jpg" width="300">|
|3|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/3.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/3_bbox.jpg" width="300">|
|4|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/4.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/4_bbox.jpg" width="300">|
|5|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/5.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/5_bbox.jpg" width="300">|
|6|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/6.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/6_bbox.jpg" width="300">|
|7|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/7.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/7_bbox.jpg" width="300">|
|8|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/8.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/8_bbox.jpg" width="300">|

**Comparison of Detection Result and Ground Truth**
| Image No. | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|**Prediction**  |814 |1009|1038|913 |959 |1023|1011|1015|
|**Ground truth**|898 |1000|1019|964 |971 |1002|1033|1005|
|**Error (%)**   |9.35|0.90|1.86|5.29|1.24|2.10|2.13|1.00|
