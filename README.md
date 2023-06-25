#Human Detection using OpenCV
This repository contains a Python script for detecting humans in images and videos using OpenCV's HOG (Histogram of Oriented Gradients) algorithm. It provides a simple and straightforward way to identify and draw bounding boxes around people in real-time video streams or from static images.

#Requirements
To run the script, you need to have the following dependencies installed:

Python 3.x
OpenCV
imutils
argparse
You can install the required packages by running the following command:

Copy code
pip install opencv-python imutils argparse

#Usage
The script can be executed from the command line with the following options:

-v or --video: Path to a video file for human detection.
-i or --image: Path to an image file for human detection.
-c or --camera: Set this flag to true if you want to use the camera for live human detection.
-o or --output: Path to the optional output video file (only applicable for video detection).

#Examples
To detect humans in a video file:
python human_detection.py -v path/to/video.mp4

To detect humans in an image file and save the output image:
python human_detection.py -i path/to/image.jpg -o path/to/output.jpg

To perform live human detection using the camera:
python human_detection.py -c true

#Algorithm
The script utilizes OpenCV's HOGDescriptor class and its pre-trained SVM (Support Vector Machine) model for human detection. It uses the detectMultiScale function to detect humans in frames with bounding box coordinates and confidence weights.

The detected humans are drawn with bounding boxes and labeled with sequential person numbers. The total number of detected persons is displayed on the output frame.
