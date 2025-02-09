# DeeplearningProject

## Vahid Shahiri  99301051  and Seyed Reza Hoseini Najrkolaei 99301016

## There are two reports  files which are the same except that one of them is in two columns format and the other one is in one column.

### Yolov5.ipynb is for object detection.

### Our_Implemented_Depth_Estimation.ipynb is our implemented depth estimation network.

### Depth_Estimation_Hybrid_CNN.ipynb is also for depth estimation.

### JOINT_DEPTH_OBJECT_DETECTION.ipynb is combined network for both object detection and depth estimation.

# Abstract
Given an image, the purpose of object detection is to obtain the location and category information
of each object instance in it. As an important part of computer vision, object detection has a broad
range of applications in many areas such as autonomous driving, robot vision and surveillance system.
However, some applications (e.g. autonomous driving) not only need the positions of objects in the
image but also require these detected objects actual depth. In this project we utilize the state of the art
YOLO v5 object detection network to obtain the category information of the objects and then we pass
the resulting bounding boxes to a hybrid CNN (convolutional neural network) to infer the depth value.
Our code requires the user to enter a value for maximum target depth so that at the output any object
closer than this target value will be labeled. The label of the bounding boxes at the output of our code,
shows both the object type and the estimated depth.

# Architecture Description
We note that our own strategy to combine object detection and depth estimation networks is
the same as the joining method used in  <a href="https://ieeexplore.ieee.org/document/8805052">Joint Object Detection and Depth Estimation in Multiplexed Image</a>. In other words, the input image is passed through
the object detection network (in our case YOLO v5) and after acquiring the bounding boxes of
respecting objects, these bounding boxes are fed to the depth estimation network (in our case
hybrid CNN). Then according to ”mean” or ”median” strategy described in report, we can decide whether the specific object is closer than the range user has passed
to the code or not. As shown in report such joining strategy can yield shorter run-times and
better EPE metric outcomes.

# Final Test
## Testing our joint object detection and depth estimation method by images from NYU-v2 dataset
<p align="center">
<image align="center" src = "images/finaltest_1_1.png" width="800">
</p>
  
<p align="center">
<image align="center" src = "images/finaltest_1_2.png" width="800">
</p>
