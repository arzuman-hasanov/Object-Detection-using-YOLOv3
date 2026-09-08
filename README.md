# Train Detection using YOLOv3 

A custom object detection project that uses YOLOv3 and OpenCV to detect trains in images.

The model was trained using a custom dataset with a single object class, Train, and can identify trains by drawing bounding boxes around detected objects.

📌 Project Overview

This project demonstrates how to build and use a custom YOLOv3 object detection model.

The trained model processes input images and:

Detects trains
Calculates detection confidence
Draws bounding boxes around detected trains
Applies Non-Maximum Suppression (NMS) to remove overlapping detections
Displays the detection results using OpenCV
🧠 Model

The project uses a customized YOLOv3 architecture configured for a single object class.

Object class:

Train

Input resolution:

416 × 416

Number of classes:

1

The YOLO configuration contains three detection scales, allowing the model to detect objects of different sizes.

🛠️ Technologies Used
Python
OpenCV
NumPy
YOLOv3
Darknet
OpenCV DNN module
🔍 How It Works

The detection pipeline follows these steps:

Input Image
     ↓
Image Preprocessing
     ↓
Resize to 416 × 416
     ↓
Create YOLO Blob
     ↓
YOLOv3 Inference
     ↓
Calculate Confidence
     ↓
Bounding Box Detection
     ↓
Non-Maximum Suppression
     ↓
Display Detected Train
📂 Project Files
.
├── yolov3_testing.cfg
├── yolov3_training_last.weights
├── detection.py
├── sample images/
└── README.md

The exact filenames may vary depending on how the model and dataset are organized in the repository.

⚙️ Installation

Clone the repository:

git clone https://github.com/your-username/your-repository.git
cd your-repository

Install the required Python packages:

pip install opencv-python numpy
▶️ Running the Detector

Make sure the following files are available:

yolov3_training_last.weights
yolov3_testing.cfg

Update the image path in the Python script if necessary:

images_path = glob.glob("path/to/images/*.jpg")

Then run:

python detection.py

The program will open each image and display detected trains with bounding boxes.

🎯 Detection Settings

The detector currently uses:

Confidence threshold: 0.3
NMS threshold: 0.4
YOLO input size: 416 × 416
Number of classes: 1

Example detection logic:

if confidence > 0.3:
    # Object detected

Non-Maximum Suppression is then applied to reduce duplicate or overlapping bounding boxes.

🏋️ Training Configuration

The YOLOv3 configuration was modified for custom training with one class.

Important parameters include:

width = 416
height = 416
classes = 1
learning_rate = 0.001
momentum = 0.9
decay = 0.0005

The final convolutional layers are configured with:

filters = 18

This follows the YOLOv3 formula:

filters = (classes + 5) × 3

For one class:

(1 + 5) × 3 = 18
