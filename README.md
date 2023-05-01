# Self-Driving Car Lane Detection using OpenCV
This project implements a self-driving car system that uses OpenCV to detect and follow lanes on the road. The system captures video from a camera mounted on the car and processes the video frames in real-time to identify the location of the lanes. The car then adjusts its steering to stay centered between the lanes.

# Overview
The goal of this project is to create a basic self-driving car system that can autonomously follow the lanes on the road. Lane detection is a fundamental component of any self-driving car system, and it involves detecting the edges of the lanes in the road and estimating their position relative to the car. OpenCV is a popular computer vision library that provides many powerful tools for lane detection, including edge detection, color thresholding, and perspective transformation.
The system consists of a camera mounted on the car, which captures video frames of the road ahead. Each frame is processed by the self-driving car software, which applies a series of computer vision algorithms to detect the lanes on the road. The system then uses the detected lanes to calculate the steering angle of the car, which is used to adjust the steering servo and keep the car centered between the lanes.

# Requirements
This project requires the following dependencies:

1. Python 3.7
2. OpenCV
3. NumPy

# Algorithm Overview
The self-driving car system consists of the following main steps:

1. Capturing frames from the camera: The system captures frames from the camera mounted on the car. Each frame is a 2D image that represents the current view of the road.

2. Preprocessing the frames: Before the frames can be processed for lane detection, they need to be preprocessed to improve the quality of the image. This may include operations such as cropping the image to remove irrelevant areas, resizing the image to a fixed size, and converting the image to grayscale.

3. Edge detection: The next step is to detect the edges of the lanes in the image. This is done using an edge detection algorithm such as the Canny edge detector. The output of this step is a binary image where the edges of the lanes are represented by white pixels, and everything else is black.

4. Region of interest selection: Since the lanes are only present in a specific area of the image, we can limit our lane detection to this region of interest (ROI) to improve the accuracy of the detection. This is typically a trapezoidal shape that covers the area of the road where the lanes are expected to appear.

5. Perspective transformation: The lanes in the ROI will appear as trapezoids in the image, but in reality, they are parallel lines. We need to transform the perspective of the image to a bird's-eye view so that the lanes appear as parallel lines. This is done using a perspective transformation matrix that maps the trapezoidal ROI to a rectangular region of interest.

6. Lane detection: With the perspective-transformed image, we can now perform lane detection using various computer vision techniques. This may include color thresholding to isolate the lanes from the rest of the image, sliding window search to find the lane pixels, and polynomial fitting to fit a curve to the lane pixels.

7. Lane tracking: Once the lanes have been detected, we can use this information to further process.