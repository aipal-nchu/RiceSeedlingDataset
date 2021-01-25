# Rice Shoot Counting
A repository to open rice shoot counting dataset.


## Data Download link (Google Drive)
#### [RiceShootClassification.tgz](https://rebrand.ly/RiceshootclassificationTgz85fd7)
> This file includes three folders: riceshoot, grass, bareland. Train-val and test datasets are included.

#### [RiceShootCouning.tgz](https://rebrand.ly/RiceshootcountingTgzE3355)
> This file contains 8 detection demo images.

#### [2018-08-07_ARI80_20m_Ortho.tif](https://rebrand.ly/OrthoTif7b85b)
> This is the orthomosaic image of the field of number 80, TARI, with TWD97 / TM2 zone 121 (EPSG:3826) projection.

## Rice Shoot Dataset
  This dataset contains three classes: 
   - `rice shoot`
   - `grass`
   - `bare land`

**An overview of image dataset**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/dataset.jpg" width="784" height="305">



**The number of images used for training, validation, and testing in the rice shoot dataset.**
| Class       | Training Samples | Validation Samples | Testing Samples | Total Samples |
|:-----------:|:----------------:|:------------------:|:---------------:|:-------------:|
| **Rice Shoot**  | 22,438 | 561   | 5,048  | 28,047 |
| **Grass**       | 15,006 | 375   | 3,376  | 18,757 |
| **Bare Land**   | 21,265 | 532   | 4,784  | 26,581 |
| **Total**       | 58,709 | 1,468 | 13,208 | 73,385 |

## A Simple Example of CNN Classification Model
**The architecture of the proposed network for rice shoot classification**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/Network_Architechture.jpg" width="784" height="371">

## Detection Demo Dataset
This dataset is used for patch-based object-detection scenario.  
- 8 images.
- 8x8 meters region.
- 1527x1527 pixels.
- PASCAL VOC xml format annotation.

**An overview of 8 detection demo images**
<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/DemoClip.png" width="784" height="303">


| number | original image | result image |
|:-:|:-:|:-:|
|1|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/1.jpg" width="300" height="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/1_bbox.jpg" width="300" height="300">|
|2|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/2.jpg" width="300" height="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/2_bbox.jpg" width="300" height="300">|
|3|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/3.jpg" width="300" height="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/3_bbox.jpg" width="300" height="300">|
|4|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/4.jpg" width="300" height="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/4_bbox.jpg" width="300" height="300">|
|5|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/5.jpg" width="300" height="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/5_bbox.jpg" width="300" height="300">|
|6|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/6.jpg" width="300" height="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/6_bbox.jpg" width="300" height="300">|
|7|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/7.jpg" width="300" height="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/7_bbox.jpg" width="300" height="300">|
|8|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/8.jpg" width="300" height="300">|<img src="https://raw.githubusercontent.com/aipal-nchu/RiceShootCounting/main/images/8_bbox.jpg" width="300" height="300">|

**Comparison of Detection Result and Ground Truth**
| Image No. | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|**Prediction**  |814 |1009|1038|913 |959 |1023|1011|1015|
|**Ground truth**|898 |1000|1019|964 |971 |1002|1033|1005|
|**Error (%)**   |9.35|0.90|1.86|5.29|1.24|2.10|2.13|1.00|
