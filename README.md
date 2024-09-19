# Mahalanobis-Distance-based-Multi-view-Optimal-Transport-for-Multi-view-Crowd-Localization
Mahalanobis Distance-based Multi-view Optimal Transport for Multi-view Crowd Localization, ECCV 2024

![mvot](https://github.com/zqyq/Mahalanobis-Distance-based-Multi-view-Optimal-Transport-for-Multi-view-Crowd-Localization/blob/main/mvot.png)

## Abstract
Multi-view crowd localization predicts the ground locations of all people in the scene. Typical methods usually estimate the crowd
density maps on the ground plane first, and then obtain the crowd locations. However, existing methods’ performances are limited by the ambiguity of the density maps in crowded areas, where local peaks can be
smoothed away. To mitigate the weakness of density map supervision, optimal transport-based point supervision methods have been proposed in
the single-image crowd localization tasks, but have not been explored for
multi-view crowd localization yet. Thus, in this paper, we propose a novel
Mahalanobis distance-based multi-view optimal transport (M-MVOT)
loss specifically designed for multi-view crowd localization. First, we replace the Euclidean-based transport cost with the Mahalanobis distance,
which defines elliptical iso-contours in the cost function whose long-axis
and short-axis directions are guided by the view ray direction. Second,
the object-to-camera distance in each view is used to adjust the optimal transport cost of each location further, where the wrong predictions
far away from the camera are more heavily penalized. Finally, we propose a strategy to consider all the input camera views in the model loss
(M-MVOT) by computing the optimal transport cost for each groundtruth point based on its closest camera. Experiments demonstrate the
advantage of the proposed method over density map-based or common
Euclidean distance-based optimal transport loss on several multi-view
crowd localization datasets.


## Overview
We release the PyTorch code for the M-MVOT, a multi-view crowd localization method with promising performance on CVCS,
Wildtrack, and MultiviewX datasets. 

## Dependencies
- python
- pytorch & torchvision
- numpy
- matplotlib
- pillow
- opencv-python
- kornia
- tqdm
- argparse
- shutil


## Training
For training, please firstly pretrain camera-view encoder and decoder with camera-view loss. And then load pretrained camera-view model for full pipline training with both camera-view loss and ground-plane loss.

## Pretrained models
You can download the checkpoints at this link.

## Acknowledgement
This work was supported in parts by NSFC (62202312, U21B2023, U2001206),
Guangdong Basic and Applied Basic Research Foundation (2023B1515120026),
DEGP Innovation Team (2022KCXTD025), City University of Hong Kong Strategic Research Grant (7005665), Shenzhen Science and Technology Program (KQTD
20210811090044003, RCJC20200714114435012), Guangdong Laboratory of Artificial Intelligence and Digital Economy (SZ), and Scientific Development Funds
from Shenzhen University.


