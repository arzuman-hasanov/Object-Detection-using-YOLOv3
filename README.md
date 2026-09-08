Train Detection using YOLOv3 🚆

A custom object detection project using YOLOv3 and OpenCV to detect trains in images.

Features
Custom YOLOv3 model trained for Train detection
Detects objects and draws bounding boxes
Uses confidence thresholding and Non-Maximum Suppression (NMS)
Supports image-based detection
Technologies
Python
OpenCV
NumPy
YOLOv3
Darknet
Usage

Install dependencies:

pip install opencv-python numpy

Make sure the following files are available:

yolov3_testing.cfg
yolov3_training_last.weights

Update the image path in the Python script and run:

python detection.py

The detected trains will be displayed with bounding boxes.

Model Configuration
Input size: 416 × 416
Classes: 1 (Train)
Confidence threshold: 0.3
NMS threshold: 0.4
