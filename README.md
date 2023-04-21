# Vision-based Perception and Control for Lane Keeping of Autonomous Vehicles

### Experimental Results
- <a target="_blank" href="https://drive.google.com/file/d/1itWQYB3XyWjjB7FkS3jwFreRLPzb5TV0/view?usp=share_link"> Lane detection result</a> on a test video from [Udacity](https://github.com/udacity/CarND-Advanced-Lane-Lines). 
<!--   (https://drive.google.com/file/d/1itWQYB3XyWjjB7FkS3jwFreRLPzb5TV0/view?usp=share_link) -->
- Lane keeping test on AggieAuto platform -Lincoln MKZ hybrid:
  - <a target="_blank" href="https://drive.google.com/file/d/1eFe6Igph0WlnYdaqwkBvpYD3Lbf5cTPz/view?usp=share_link"> 10 mph </a>
  - <a target="_blank" href="https://drive.google.com/file/d/15oczESI7VBMf6DfGg6XsCKEIbasLAsMl/view?usp=share_link"> 15 mph </a>
  - <a target="_blank" href="https://drive.google.com/file/d/1RdBTzxfykjmy-izDYmHEGaoI4tj5N91s/view?usp=share_link"> 17-19 mph </a>
  - <a target="_blank" href="https://drive.google.com/file/d/1LT0UoUgoXXJxODhq8K0dqMcLA2BMTiZX/view?usp=share_link"> 18 mph </a>
  - <a target="_blank" href="https://drive.google.com/file/d/1EByMQuYTOXEqKouim4xNQvMEVKfEWg0k/view?usp=share_link"> 20-22 mph </a>
 
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
