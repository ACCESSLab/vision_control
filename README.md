## Vision based Control for Lane Keeping

### Experimental Results
- Lane detection:
  - udacity video.(https://drive.google.com/file/d/1itWQYB3XyWjjB7FkS3jwFreRLPzb5TV0/view?usp=share_link)
- Lane keeping:
  | test speed| Google drive link|
  |------|-----|
  |10 mph  | https://drive.google.com/file/d/1eFe6Igph0WlnYdaqwkBvpYD3Lbf5cTPz/view?usp=share_link|
  |15 mph  | https://drive.google.com/file/d/15oczESI7VBMf6DfGg6XsCKEIbasLAsMl/view?usp=share_link|
  |17 - 19 mph | https://drive.google.com/file/d/1RdBTzxfykjmy-izDYmHEGaoI4tj5N91s/view?usp=share_link|
  |18 mph  | https://drive.google.com/file/d/1LT0UoUgoXXJxODhq8K0dqMcLA2BMTiZX/view?usp=share_link|
  |20 - 22 mph | https://drive.google.com/file/d/1EByMQuYTOXEqKouim4xNQvMEVKfEWg0k/view?usp=share_link|

### Nighttime driving test data with labels
  Image and label data 
 - https://drive.google.com/drive/folders/1QKEVOJP5nu5cNQ6HzNiZvBkv_AMhHk1i?usp=share_link
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

### Camera calibration
Intrinsic calibration matrices are in ```calibration.txt``` file.
