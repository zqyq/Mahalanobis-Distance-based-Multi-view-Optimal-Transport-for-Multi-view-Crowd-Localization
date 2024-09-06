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
