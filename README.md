# PV-RCNN_Point-Voxel-Feature-Set-Abstraction-For-3D-Object-Detection Problem
PointVoxel-RCNN (PV-RCNN), is a two-stage 3D detection framework aiming at more accurate 3D object detection from point clouds.
3D detection approaches are based on either 3D voxel CNN with sparse convolution or PointNet-based networks as the backbone.
3D voxel CNNs with sparse convolution are more efficient and are able to generate high-quality 3D object proposals.
PointNet-based methods can capture more accurate contextual information with flexible receptive fields.

PV-RCNN consists of a 3D voxel CNN with sparse convolution as the backbone for efficient feature encoding and proposal generation.
Given each 3D object proposal, there are two novel operations to effectively pool its corresponding features from the scene:

1- voxel-to-keypoint scene encoding: summarizes all the voxels of the overall scene feature volumes into a small number of feature keypoints.

2- point-to-grid RoI feature abstraction: effectively aggregates the scene keypoint features to RoI grids for proposal confidence prediction and location refinement

## Problem Statement:
The object detection and object orientation estimation benchmark consists of 7481 training images and 7518 test images, comprising a total of 80.256 labeled objects. All images are color and saved as png. For evaluation, we compute precision-recall curves for object detection and orientation-similarity recall curves for joint object detection and orientation estimation. In the latter case not only the object 2D bounding box has to be located correctly, but also the orientation estimate in bird's eye view is evaluated. To rank the methods we compute average precision and average orientation similarity. We require that all methods use the same parameter set for all test pairs. Our development kit provides details about the data format as well as MATLAB / C++ utility functions for reading and writing the label files.

We evaluate object detection performance using the PASCAL criteria and object detection and orientation estimation performance using the measure discussed in our CVPR 2012 publication. For cars we require an overlap of 70%, while for pedestrians and cyclists we require an overlap of 50% for a detection. Detections in don't care areas or detections which are smaller than the minimum size do not count as false positive. Difficulties are defined as follows:

● Easy: Min. bounding box height: 40 Px, Max. occlusion level: Fully visible, Max. truncation: 15 %

● Moderate: Min. bounding box height: 25 Px, Max. occlusion level: Partly occluded, Max. truncation: 30 %

● Hard: Min. bounding box height: 25 Px, Max. occlusion level: Difficult to see, Max. truncation: 50 %
All methods are ranked based on the moderately difficult results. Note that for the hard evaluation ~2 % of the provided bounding boxes have not been recognized by humans, thereby upper bounding recall at 98 %. Hence, the hard evaluation is only given for reference.

# What is Our Purpose?
to achieve high performance 3D object detection by designing novel point-voxel integrated networks and to design novel point-voxel integrated networks to learn better 3D features from irregular point clouds.

# What is the importance of 3D object detection?
As it is used in wide applications in various fields such as autonomous driving and robotics.
