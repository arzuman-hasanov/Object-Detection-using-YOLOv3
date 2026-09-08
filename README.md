# Train Detection using YOLOv3 🚆

This project demonstrates custom **YOLOv3 object detection** for detecting trains in images.

The model:

* Detects trains
* Calculates detection confidence
* Draws bounding boxes
* Applies Non-Maximum Suppression (NMS)
* Displays detection results using OpenCV

## 🧠 Model

* **Architecture:** YOLOv3
* **Object class:** Train
* **Input resolution:** 416 × 416
* **Number of classes:** 1
* **Detection scales:** 3

## 🛠️ Technologies

* Python
* OpenCV
* NumPy
* YOLOv3
* Darknet
* OpenCV DNN

## 🔍 Detection Pipeline

```text
Input Image
    ↓
Preprocessing
    ↓
YOLOv3 Inference
    ↓
Confidence Calculation
    ↓
Bounding Box Detection
    ↓
Non-Maximum Suppression
    ↓
Detected Train
```

## 📂 Project Files

```text
.
├── yolov3_testing.cfg
├── yolov3_training_last.weights
├── detection.py
├── sample_images/
└── README.md
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

Install dependencies:

```bash
pip install opencv-python numpy
```

## ▶️ Usage

Make sure the model files are available:

```text
yolov3_testing.cfg
yolov3_training_last.weights
```

Update the image path in `detection.py`:

```python
images_path = glob.glob("path/to/images/*.jpg")
```

Run the detector:

```bash
python detection.py
```

Detected trains will be displayed with bounding boxes.

## 🎯 Detection Settings

| Setting              | Value     |
| -------------------- | --------- |
| Input size           | 416 × 416 |
| Classes              | 1         |
| Confidence threshold | 0.3       |
| NMS threshold        | 0.4       |
| Learning rate        | 0.001     |
| Momentum             | 0.9       |
| Weight decay         | 0.0005    |

## 🏋️ Training Configuration

The YOLOv3 configuration was modified for a single object class.

The final detection layers use:

```text
filters = 18
```

This is calculated using:

```text
filters = (classes + 5) × 3
       = (1 + 5) × 3
       = 18
```
