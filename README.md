# Rice Seedling Datasets
A repository to open rice seedling dataset.  

## Related Publications
The data descriptor was published on Remote Sensing, MDPI. (open access)  
[A UAV Open Dataset of Rice Paddies for Deep Learning Practice](https://doi.org/10.3390/rs13071358)  

An application of rice seedling detection using transfer learning was published on Remote Sensing, MDPI. (open access)  
[Rice Seedling Detection in UAV Images Using Transfer Learning and Machine Learning](https://doi.org/10.3390/rs14122837)

### MDPI and ACS Style  
  1. Yang, M. D.; Tseng, H. H.; Hsu, Y. C.; Yang, C. Y.; Lai, M. H.; Wu, D. H. A UAV Open Dataset of Rice Paddies for Deep Learning Practice. *Remote Sens.* **2021**, 13, 1358. doi:10.3390/rs13071358  
  2. Tseng, H. H.; Yang, M. D.; Saminathan, R.; Hsu, Y. C.; Yang, C. Y.; Wu, D. H. Rice Seedling Detection in UAV Images Using Transfer Learning and Machine Learning. *Remote Sens.* **2022**, 14, 2837. doi:10.3390/rs14122837  

---

## Contents
- [Rice Seedling Datasets](#rice-seedling-datasets)
  - [Related Publications](#related-publications)
    - [MDPI and ACS Style](#mdpi-and-acs-style)
  - [Contents](#contents)
  - [1. Data Download Link](#1-data-download-link)
    - [2018 Orthomosaic image](#2018-orthomosaic-image)
    - [Expansion Orthomosaic image (2019-2020)](#expansion-orthomosaic-image-2019-2020)
    - [Dataset of Rice Seedling Classification (Train-Val)](#dataset-of-rice-seedling-classification-train-val)
    - [Dataset of Rice Seedling Detection (Train-Val)](#dataset-of-rice-seedling-detection-train-val)
    - [Dataset of Detection Demonstration (Test)](#dataset-of-detection-demonstration-test)
  - [2. Dataset of Rice Seedling Classification](#2-dataset-of-rice-seedling-classification)
  - [3. Dataset of Rice Seedling Detection](#3-dataset-of-rice-seedling-detection)
  - [4. A Simple Example of CNN Classification Model](#4-a-simple-example-of-cnn-classification-model)
  - [5. Detection Demo Dataset](#5-detection-demo-dataset)

## 1. Data Download Link

The data access is moved to the page **[Rice Seedling Dataset 水稻秧苗辨識資料集]**, powered by [NCHU Open AI Model and Dataset Platform].  

You'll be asked to sign-in for the data access, while it is free to register.  
Once you have logged in the platform, direct to the webpage and press the following botton (red rectangle highlighted).  
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/Accept_botton.png" width="512">  

Then accept the license term to proceed the data access.  
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/Accept_term.png" width="512">  


### 2018 Orthomosaic image
>|Filename|File size|Image size (pixels)|Spatial resolution (mm/pixel)|
>|:-:|:-:|:-:|:-:|
>|**[2018-08-07_ARI80_20m_Orthomosaic.tif](https://rebrand.ly/20180807ARI8020mOrthomosaic)**|465MB|19406 x 10413| 5.23 |
>|**[2018-08-14_ARI80_20m_Orthomosaic.tif](https://rebrand.ly/20180814ARI8020mOrthomosaic)**|610MB|19876 x 10687| 5.11 |
>|**[2018-08-23_ARI80_20m_Orthomosaic.tif](https://rebrand.ly/20180823ARI8020mOrthomosaic)**|557MB|18294 x 9823 | 5.55 |  

> These three links are the orthomosaic image of paddy No.80, TARI, which were in TWD97 / TM2 zone 121 (EPSG:3826) projection. The images were acquired in three consecutive growing stages in 2018.

### Expansion Orthomosaic image (2019-2020)
>|Filename|File size|Image size (pixels)|Spatial resolution (mm/pixel)|
>|:-:|:-:|:-:|:-:|
>|**[2019-03-26_ARI78_20m_Orthomosaic.tif](https://rebrand.ly/20190326ARI7820mOrthomosaic)**|485MB|20192 x 10858| 5.04 |
>|**[2019-04-02_ARI78_20m_Orthomosaic.tif](https://rebrand.ly/20190402ARI7820mOrthomosaic)**|418MB|19061 x 10250| 5.33 |
>|**[2019-08-12_ARI78_20m_Orthomosaic.tif](https://rebrand.ly/20190812ARI7820mOrthomosaic)**|503MB|21998 x 11829| 4.62 |  
>|**[2019-08-20_ARI78_20m_Orthomosaic.tif](https://rebrand.ly/20190820ARI7820mOrthomosaic)**|605MB|21265 x 11435| 4.78 |  
>|**[2020-03-12_ARI78_40m_Orthomosaic.tif](https://rebrand.ly/20200312ARI7840mOrthomosaic)**|278MB|15933 x 8568 | 6.38 |  
>|**[2020-03-17_ARI78_40m_Orthomosaic.tif](https://rebrand.ly/20200317ARI7840mOrthomosaic)**|317MB|15941 x 8572 | 6.38 |  
>|**[2020-03-26_ARI78_40m_Orthomosaic.tif](https://rebrand.ly/20200326ARI7840mOrthomosaic)**|385MB|15962 x 8583 | 6.37 |  
>|**[2020-08-12_ARI78_40m_Orthomosaic.tif](https://rebrand.ly/20200812ARI7840mOrthomosaic)**|330MB|15966 x 8586 | 6.37 |  
>|**[2020-08-18_ARI78_40m_Orthomosaic.tif](https://rebrand.ly/20200818ARI7840mOrthomosaic)**|382MB|15977 x 8591 | 6.36 |  
>|**[2020-08-25_ARI78_40m_Orthomosaic.tif](https://rebrand.ly/20200825ARI7840mOrthomosaic)**|402MB|15979 x 8593 | 6.36 |  

> These 10 links are the orthomosaic image of paddy No.78, TARI, which were in TWD97 / TM2 zone 121 (EPSG:3826) projection. The images were acquired in 2019 and 2020.
---
### Dataset of Rice Seedling Classification (Train-Val)
**[RiceSeedlingClassification.tgz (uncompressed size 426MB)](https://rebrand.ly/RiceSeedlingClassification)**
> This file includes two folders: riceseedling and arableland. Train-val and test datasets are all included.
---
### Dataset of Rice Seedling Detection (Train-Val)
**[RiceSeedlingDetection.tgz (uncompressed size 19.1MB)](https://rebrand.ly/RiceseedlingDetectionVOC)**
> This is a PASCAL VOC format object-detection dataset, which includes two folders: JPEGImaegs and Annotations.
---
### Dataset of Detection Demonstration (Test)
**[RiceSeedlingDemo.tgz (uncompressed size 48.5MB)](https://rebrand.ly/RiceseedlingDemoVOC)**
> This file contains 8 detection demo images and the corresponging PASCAL VOC xml format annotations.  
---
**An overview of the region of different datasets**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/Datasets_Area_Overview.png" width="768">  
> An overview of the field no. 80 (cyan bounding area) in TARI, Taichung. Image acquired on August 7, 2018. The green bounding area represents the area for training-validation dataset, and the red bounding area represents the subsets for object detection demonstration dataset.  

## 2. Dataset of Rice Seedling Classification
  This dataset contains two classes: 
   - `rice seedling`
   - `arable land`

**An overview of image dataset**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/dataset.png" width="768">



**The number of images used for training, validation, and testing in the rice seedling dataset.**  

| Class       | Training Samples | Validation Samples | Testing Samples | Total Samples |
|:-:|:-:|:-:|:-:|:-:|
| **Rice Seedling**  | 22,438 | 561   | 5,048 | 28,047 |
| **Arable Land**    | 21,265 | 532   | 4,784 | 26,581 |
| **Total**          | 43,703 | 1,093 | 9,832 | 54,628 |  

## 3. Dataset of Rice Seedling Detection
This dataset is used for object-detection model training and validation.  
- PASCAL VOC xml format annotation
- 3 consecutive mission: Aug 7<sup>th</sup>, Aug 14<sup>th</sup> and Aug 23<sup>rd</sup>
- 8 subsets
- 25 samples/subset
- 600 samples total
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/Detection_Dataset.png" width="768">  

**Examples of three growth stages of the rice seedling detection dataset**

## 4. A Simple Example of CNN Classification Model
**The architecture of the proposed network for rice seedling classification**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/Network Architechture-2class.png" width="768">

In the article, we proposed a simple CNN architecture which adopted the stacked convolution layer from VGG-16. The pre-trained model is provided in the [**model**](https://github.com/aipal-nchu/RiceSeedlingDataset/tree/main/model) directory.  
  
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

## 5. Detection Demo Dataset
This dataset is used for patch-based object-detection scenario.  
- 8 subsets
- 8m x 8m region
- 1527 x 1527 pixels
- PASCAL VOC xml format annotation

**An overview of 8 detection demo images**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/DemoClip.png" width="768">


| Subset No. | Raw Image | Prediction Image | Ground Truth Image|
|:-:|:-:|:-:|:-:|
|1|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/1.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/1_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/1_GT.jpg" width="300">|
|2|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/2.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/2_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/2_GT.jpg" width="300">|
|3|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/3.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/3_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/3_GT.jpg" width="300">|
|4|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/4.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/4_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/4_GT.jpg" width="300">|
|5|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/5.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/5_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/5_GT.jpg" width="300">|
|6|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/6.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/6_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/6_GT.jpg" width="300">|
|7|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/7.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/7_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/7_GT.jpg" width="300">|
|8|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/8.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/8_bbox.jpg" width="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceSeedlingDataset/main/images/8_GT.jpg" width="300">|

**Comparison of Detection Result and Ground Truth** 
 
| Subset No. | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|**Prediction**  |735 |1006|1037|809 |1004|1050|1017|1032|
|**Ground truth**|898 |1000|1019|964 |971 |1002|1033|1005|
|**Error (%)**   |**18.15**|0.60|1.77|**16.08**|3.40|4.79|1.55|2.69|


[Rice Seedling Dataset 水稻秧苗辨識資料集]: https://rebrand.ly/nchu-riceseedlingdataset
[NCHU Open AI Model and Dataset Platform]: https://rebrand.ly/nchu-aiopendata