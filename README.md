# Vision-based Perception and Control for Lane Keeping of Autonomous Vehicles
 ----
# Abstract
This paper proposes a vision-based control method for autonomous vehicle lane keeping. This approach is intended to provide a reliable alternative solution for localization and path planning related issues in environments where GPS is unavailable or unreliable such as in tunnels and urban areas. The proposed method consists of a robust lane detection algorithm to generate a reference path of the vehicle and a model predictive controller (MPC) for tracking the reference path. The lane detector extracts lane markings from image frames to find ego-lane boundaries from which the lane center is calculated in the vehicle’s coordinate frame. The MPC uses a kinematic vehicle model to generate the lateral and longitudinal control values to smoothly track the reference path. The proposed technique is implemented and tested on a Lincoln MKZ hybrid vehicle equipped with a computing platform with Intel’s quad-core Xeon processors. Experimental results show that the proposed vision-based lane detection method works well on various road segments despite challenging road conditions such as shadows, road texture variations, interference from other road signs, and missing lane boundaries. The multithreaded implementation of lane detection and the MPC allowed us to run the integrated system at the speed of 25 HZ. The integration of lane detection and MPC resulted in smoothly keeping the car in the center of the lane over a curved test track while respecting the physical constraints of the car.
 
----
### Experimental Results
- <a target="_blank" href="https://drive.google.com/file/d/1ngpegivYYYi-MNU1f1ENg10IcjexBM1c/view?usp=share_link"> Lane detection result</a> on a test video from [Udacity](https://github.com/udacity/CarND-Advanced-Lane-Lines). 
<!--   (https://drive.google.com/file/d/1itWQYB3XyWjjB7FkS3jwFreRLPzb5TV0/view?usp=share_link) -->
- Lane keeping test on AggieAuto platform -Lincoln MKZ hybrid:
  - <a target="_blank" href="https://drive.google.com/file/d/1yPO2pz2oI7kPlyG4CvHWLIBVwqPX6npS/view?usp=share_link"> 10 mph </a>
  - <a target="_blank" href="https://drive.google.com/file/d/1JLlLjxpWWoN2B_klsbc9Sdpz_Ov8sHTV/view?usp=share_link"> 15 mph </a>
  - <a target="_blank" href="https://drive.google.com/file/d/1JIadkfWS8ncQwKYNGoMUn8n9EcTvHX1x/view?usp=share_link"> 17-19 mph </a>
  - <a target="_blank" href="https://drive.google.com/file/d/1WQVJX6qEgZQv_oPNKTs0gPPxK81JA_Bo/view?usp=share_link"> 18 mph </a>
  - <a target="_blank" href="https://drive.google.com/file/d/1Dovhesq5M89a4QSf4PgNxD97uBW9ixFA/view?usp=share_link"> 20-22 mph </a>
- Lane detection on Caltech dataset
  
- 
 ----
### Nighttime driving dataset
  <a target="_blank" href="https://drive.google.com/drive/folders/1QKEVOJP5nu5cNQ6HzNiZvBkv_AMhHk1i?usp=share_link">Image and label data.</a>
- Folder structure
```
 nighttime_driving_data
          └─images
          |   └─img0.png
          |   └─img1.png
          |   └─ ...
          └─labels
              └─img0.json
              └─img1.json
              └─ ...
```
For each image in the ```images``` folder, there is a corrosponding label in the ```labels``` folder with the same name.
The labels are created using [labelme](https://github.com/wkentaro/labelme.git) app.
#### Label content
  The label is for ```left``` and ```right``` lane boudaries as shown below.

---
### Camera

<!-- ### Camera calibration
Intrinsic calibration matrices are the following. 
* The images in the dataset are already corrected.
```
## Camera Matrix
cam_mtx = np.array([[2.07260223e+03, 0.00000000e+00, 8.25522002e+02],
                    [0.00000000e+00, 2.07577055e+03, 4.92533698e+02],
                    [0.00000000e+00, 0.00000000e+00, 1.00000000e+00]
                  ])

## Distortion coefficients
dist_coeff =np.array([[-0.60676022,  0.49186421,  0.00113308,  0.01104831, -0.45043961]])


## Refined camera matrix obtained by OpenCV's getOptimalNewCameraMatrix()
refined_cam_mtx = np.array([[1.75234119e+03, 0.00000000e+00, 7.96353770e+02],
                            [0.00000000e+00, 1.98220215e+03, 4.88376415e+02],
                            [0.00000000e+00, 0.00000000e+00, 1.00000000e+00]
                          ])
```
 -->
### Evaluation script
### 
