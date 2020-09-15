# Road Lane Detection (for self driving cars)


## The Challenge
Detect road lanes (in real time ) in a video (of a motorway) so that it can guide an autonomous vehicle.


## Assumption
To detect a lane, we have to detect the white markings on either side of a lane, while ignoring other vehicles on the road, road-side barriers, street-lights etc. Also a video (taken from the vehicle camera) is made up of multiple frames. So, we have to read each frame, convert it to numerical (numpy) arrays, do image processing and detecting lanes with openCV and repeat the process with all the frames all in milliseconds so that the AI can run the vehicle on this lane.

## Key concept: Image Pre-Processing for Lane Detection
We have to first apply mask to all the frames in the input video. Then, we have to apply [image thresholding](https://en.wikipedia.org/wiki/Thresholding_(image_processing)) followed by [Hough Line Transformation](https://en.wikipedia.org/wiki/Hough_transform) to detect lane markings. Finally, combining all the processed frames back into one video to get the result.

## Data
We are using this sample [video](https://www.youtube.com/watch?reload=9&v=KWJaBJYJIjI) for this project and its frames can be downloaded from [here](https://drive.google.com/file/d/1e4cc4zFFna3Owyym6aq7ZXoquHA2l95O/view). 


## Result
    roads_v2.mp4

## Methodology
We will use [opencv-python 4.4.0.42](https://opencv.org/), which is an Open Source Computer Vision Library. 

Our steps:
- Load required libraries
- Read video frames
- Create Frame Mask 
- Process frames
    - Image Thresholding
    - Hough Line Transformation
    - Apply all these image pre-processing operations on every frame
- Prepare final video

## Requirements
    Python 3.8, (Jupyter Notebook), numpy-1.19.1, matplotlib-3.3.1, opencv-4.4.0, widgetsnbextension, ipywidgets

### Installing requirements
    conda install -c conda-forge opencv
    conda install -c conda-forge widgetsnbextension
    conda install -c conda-forge ipywidgets

## Resources
[1](https://docs.opencv.org/3.4/d9/db0/tutorial_hough_lines.html)  
[2](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_imgproc/py_houghlines/py_houghlines.html)  
[3](https://towardsdatascience.com/lines-detection-with-hough-transform-84020b3b1549)  
[4](https://en.wikipedia.org/wiki/OpenCV)

## Disclaimer
We have reproduced the code for educational and learning purposes only. Original article can be found [here](https://www.analyticsvidhya.com/blog/2020/05/tutorial-real-time-lane-detection-opencv/).



