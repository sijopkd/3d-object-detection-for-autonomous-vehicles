# 3D-Object Detection for Autonomous Vehicles 
## *Can you advance the state of the art in 3D object detection?*
![Image description](lyft.jpeg) <br />

*Source: https://www.autonews.com/mobility-report/ipo-road-show-lyft-executives-look-lower-insurance-costs*

## Task 
With the rapid evolution in the world of technology, it becomes increasingly important for the automotive sector to keep up with the fast pace, just like any other industry. In recent times, self-driving cars have gained a lot of traction but there is a huge gap in expectation and the current state. Self Driving Vehicles are one of the most hyped technologies of the modern decade. Even though many companies may brand their driver assistance technology as “Autopilot” a truly self-driving vehicle, without a human driver on open roads, has not yet become a reality. Lyft has opensources its level5 dataset and it recently launched a kaggle competition to focus on a much harder problem - 3D object detection over semantic maps. 

## The Dataset
The Lyft dataset from the active Kaggle competition was a total of 85 GB. The data was split between testing and training sets and included a sample submission. The dataset gives a 3D point cloud and camera data from the Lyft test vehicles. The data was captured by 10 host cars on the roads of Palo Alto, California. Each of the host cars has seven cameras and one LiDAR sensor on the roof, and 2 smaller sensors underneath the headlights of the vehicle.

## Evaluation

The average precision is calculated at different thresholds of Intersection over Union (IoU) to evaluate the object detection model. The IoU of a 2D bounding box is the area of the overlapping region divided by the total area of union. The IoU is calculated at thresholds starting from 0.55 to 0.95 with a step size of 0.05.

#### Intersection Over Union (IOU) 

![Image description](iou.png) <br />

#### Mean absolute precision (mAP) 

   ![Image description](map.png) <br />


## Approach

1) Data was loaded into Google Cloud Platform instance using Kaggle API
2) Data preprocessing
   - Superimpose Lidar points from three sensors into one
   - Create Bird Eye View (BEV) using the superimposed Lidar pointclouds 
   - Transform the annotated bounding boxes to BEV to create target images 
   ![Image description](preprocessing.png = 24*48) <br />
   

## Results 

Final model -> 0.045 mAP 

## Future work 

