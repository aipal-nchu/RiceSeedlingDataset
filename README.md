# Rice Shoot Counting Datasets
A repository to open rice shoot counting dataset.  

---

## Contents
  1. [Data Download Link (Google Drive)](#data-download-link-google-drive)
  2. [Rice Shoot Dataset](#rice-shoot-dataset)
  3. [CNN Classification Model](#a-simple-example-of-cnn-classification-model)
  4. [Detection Demo Dataset](#detection-demo-dataset)

## Data Download Link (Google Drive)  
### Orthomosaic image
>|Filename|Disk space|Image size|Spatial resolution|
>|:-:|:-:|:-:|:-:|
>|**[2018-08-07_ARI80_20m_Orthomosaic.tif](https://rebrand.ly/20180807ARI80Orthomosaic)**|465MB|19406 x 10413| 5.23 mm/pixel|
>|**[2018-08-14_ARI80_20m_Orthomosaic.tif](https://rebrand.ly/20180814ARI80Orthomosaic)**|610MB|19876 x 10687| 5.11 mm/pixel |
>|**[2018-08-23_ARI80_20m_Orthomosaic.tif](https://rebrand.ly/20180823ARI80Orthomosaic)**|557MB|18294 x 9823 | 5.55 mm/pixel |  

> These three links are the orthomosaic image of the field of number 80, TARI, with TWD97 / TM2 zone 121 (EPSG:3826) projection. The images were acquired in three consecutive growing stages.
---
### Trainning-Validation Dataset
**[RiceShootClassification_2class.tgz (uncompressed size 426MB)](https://rebrand.ly/riceshootdataset_2class)**
> This file includes two folders: riceshoot and bareland. Train-val and test datasets are all included.
---
### Detection Demonstration Dataset
**[RiceShootCouning.tgz (uncompressed size 48.5MB)](https://rebrand.ly/RiceshootcountingTgzE3355)**
> This file contains 8 detection demo images and the corresponging PASCAL VOC xml format annotations.  
---
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
|:-:|:-:|:-:|:-:|:-:|
| **Rice Shoot**  | 22,438 | 561   | 5,048 | 28,047 |
| **Bare Land**   | 21,265 | 532   | 4,784 | 26,581 |
| **Total**       | 43,703 | 1,093 | 9,832 | 54,628 |  

## A Simple Example of CNN Classification Model
**The architecture of the proposed network for rice shoot classification**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/Network Architechture-2class.png" width="768">

In the article, we proposed a simple CNN architecture which adopted the stacked convolution layer from VGG-16. The pre-trained model is provided in the [**model**](https://github.com/aipal-nchu/RiceShootCounting/tree/main/model) directory.  
  
The environments for the experiments are:
- host
  - Ubuntu 18.04.5 LTS Server 64bit
  - NVIDIA Display Driver 450.57 (cuda 11.0)
  - Docker CE 20.10.2
  - nvidia-docker2
- container (image: nvcr<span>.io/nvidia/tensorflow:20.03-tf2-py3 (from [Nvidia GPU Cloud](https://ngc.nvidia.com/catalog/containers/nvidia:tensorflow)))
  - tensorflow 2.2.0
  - python 3.6.9
  - matplotlib 3.3.0
  - scikit-image 0.17.2
  - scikit-learn 0.23.1
  - python3-opencv 3.2.0 (apt install)  
  
To test the provided model, simply call the `tf.keras.models.load_model()` and you're ready.

## Detection Demo Dataset
This dataset is used for patch-based object-detection scenario.  
- 8 images
- 8x8 meters region
- 1527x1527 pixels
- PASCAL VOC xml format annotation

**An overview of 8 detection demo images**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/DemoClip.png" width="768">


| Image Number | Raw Image | Prediction Image | Ground Truth Image|
|:-:|:-:|:-:|:-:|
|1|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/1.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/1_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/1_GT.jpg" width="300">|
|2|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/2.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/2_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/2_GT.jpg" width="300">|
|3|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/3.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/3_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/3_GT.jpg" width="300">|
|4|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/4.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/4_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/4_GT.jpg" width="300">|
|5|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/5.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/5_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/5_GT.jpg" width="300">|
|6|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/6.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/6_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/6_GT.jpg" width="300">|
|7|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/7.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/7_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/7_GT.jpg" width="300">|
|8|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/8.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/8_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/8_GT.jpg" width="300">|

**Comparison of Detection Result and Ground Truth**
| Image Number | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|**Prediction**  |735 |1006|1037|809 |1004|1050|1017|1032|
|**Ground truth**|898 |1000|1019|964 |971 |1002|1033|1005|
|**Error (%)**   |**18.15**|0.60|1.77|**16.08**|3.40|4.79|1.55|2.69|
