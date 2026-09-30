### Vision-based Perception and Control for Lane Keeping of Autonomous Vehicles
 ----
### Abstract
This paper proposes a vision-based control method for autonomous vehicle lane-keeping. This approach aims to provide a reliable alternative solution for localization and path planning-related issues in environments where GPS is unavailable or unreliable, such as in tunnels and urban areas. The proposed method consists of a robust lane detection algorithm to generate a reference path of the vehicle and a model predictive controller (MPC) for tracking the reference path. The lane detector extracts lane markings from image frames to determine ego-lane boundaries, from which the lane center is calculated in the vehicle’s coordinate frame. The MPC uses a kinematic vehicle model to generate the lateral and longitudinal control values necessary for smoothly tracking the reference path. The proposed technique has  been implemented and tested on a Lincoln MKZ hybrid vehicle equipped with a computer powered by Intel’s quad-core Xeon processors. Experimental results demonstrate that the proposed vision-based lane detection method performs well under various challenging road conditions, such as shadows, road texture variations, interference from other road signs, and missing lane boundaries.  

> Full paper is available on <a target="_blank" href="https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10480914"> IEEE Xplore </a>
----
### Experimental Results
- Test vehicle: Lincoln MKZ hybrid
 <img src="/images/lincoln_mkz.jpg" width="400" /> 

- Lane Detection result on Caltech dataset
 <img src="/images/caltech_output.png" width="400" /> 

- MPC Path tracking for a 525-meter test road where the maximum lateral error is 0.2m.
 <img src="/images/path_tracking.png" width="400" />
 <img src="/images/pos_error.png" width="400" /> 
- MPC control signals (Steering and Acceleration)
 <img src="/images/actuator_output.png" width="400" /> 
 
- Lane-keeping test experimental results using AggieAuto AV platform - Lincoln MKZ hybrid:
  - <a target="_blank" href="https://youtu.be/834FkeyPn50"> 10 mph </a>
  - <a target="_blank" href="https://youtu.be/8wNal90Jz5Y"> 17-19 mph </a>
  - <a target="_blank" href="https://youtu.be/P8f7fRq5gt8"> 20-22 mph </a>
  - <a target="_blank" href="https://youtu.be/cW0o2JX0zUU"> Two-lane and curved road </a>
  - <a target="_blank" href="https://youtu.be/WELfQEpWJEc?si=io5sxL5SEgi2qtKh"> 30-40 mph on public road </a>
  
 ----
### Nighttime driving dataset
  Nighttime driving test data (201 images and labels) collected in Greensboro, NC  is  <a target="_blank" href="https://drive.google.com/drive/folders/1_lgOapqE9pCGMLeOuGcNV-FYEGEkyayL?usp=drive_link"> available here </a>.
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
For each image in the ```images``` folder, there is a corresponding label in the ```labels``` folder with the same name.
The labels are created using [labelme](https://github.com/wkentaro/labelme.git) app. The label contains the ego-lane boundaries as ```left``` and ```right```.

---
### Camera
The camera used in our experiment is <a target="_blank" href="https://www.leopardimaging.com/product-category/usb30-cameras/"> Leopard USB3.0 box camera </a> with the following intrinsic parameters determined using the technique presented in <a target="_blank" href="https://docs.opencv.org/4.x/dc/dbb/tutorial_py_calibration.html">OpenCV</a>.
<!-- ### Camera calibration -->
Intrinsic calibration matrices are the following. 
* The images in the dataset are already undistorted/corrected.
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
---

### Citation
```
@ARTICLE{10480914,
  author={Getahun, Tesfamichael and Karimoddini, Ali},
  journal={IEEE Transactions on Intelligent Transportation Systems}, 
  title={An Integrated Vision-Based Perception and Control for Lane Keeping of Autonomous Vehicles}, 
  year={2024},
  volume={25},
  number={8},
  pages={9001-9015},
  keywords={Lane detection;model predictive control (MPC);visual perception;lane keeping;autonomous vehicles},
  doi={10.1109/TITS.2024.3376516}}
```


