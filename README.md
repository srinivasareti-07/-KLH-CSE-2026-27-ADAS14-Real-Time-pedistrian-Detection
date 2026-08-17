# 🚶 Real-Time Pedestrian Detection Using Computer Vision and Deep Learning

## 📌 Project Title

**Real-Time Pedestrian Detection Using YOLO, OpenCV and Deep Learning for Intelligent Road Safety**

---

## 👥 Team Members

| Name            | ID Number      |
| --------------- | -------------- |
| **A. Srinivas** | **2420030349** |
| **M. Pranay**   | **2420030562** |
| **S. Roshan**   | **2420030528** |

---

## 👨‍🏫 Supervisor

**Supervisor Name:** V. Ramya

---
---

## Abstract

The abstract of the project is provided as a separate PDF document.

[*View Abstract*](docs/projectADAS.pdf)
[*View Research Paper*](docs/Researchpaper.pdf)

---

## 📖 Abstract

Pedestrian detection is an important computer vision problem with applications in **Advanced Driver Assistance Systems (ADAS), autonomous vehicles, intelligent transportation systems, surveillance, and road-safety applications**.

This project proposes a **Real-Time Pedestrian Detection System** capable of identifying pedestrians from live camera feeds, recorded videos, and images using deep learning-based object detection.

The proposed system uses **YOLO (You Only Look Once)** for fast object detection and **OpenCV** for real-time video processing and visualization. Each incoming video frame is processed by the detection model, which identifies pedestrians and generates bounding boxes around them. The system can additionally estimate the relative position of pedestrians and generate warnings when a pedestrian is detected within a potentially dangerous region.

The primary objective is to develop a lightweight and efficient pedestrian detection pipeline capable of operating close to real time while maintaining satisfactory detection accuracy.

The system is evaluated using standard object-detection metrics such as **Precision, Recall, F1-Score, IoU, mAP and FPS**.

---

# 🎯 Problem Statement

Pedestrians are one of the most vulnerable road users. In real-world driving environments, pedestrians can be difficult to detect because of:

* Small pedestrian sizes
* Partial occlusion
* Crowded environments
* Different lighting conditions
* Motion blur
* Low-resolution camera frames
* Complex backgrounds
* Different pedestrian poses

Traditional image-processing techniques may struggle with these variations.

Therefore, this project aims to develop a **deep-learning-based real-time pedestrian detection system** that can automatically identify pedestrians from video streams and provide visual or safety alerts.

---

# 💡 Proposed Solution

The proposed system processes video frames continuously and performs pedestrian detection using a YOLO-based deep learning model.

The overall pipeline is:

```text
Camera / Video Input
        ↓
Frame Extraction
        ↓
Image Preprocessing
        ↓
YOLO Object Detection
        ↓
Pedestrian Identification
        ↓
Bounding Box Generation
        ↓
Confidence Evaluation
        ↓
Pedestrian Position Analysis
        ↓
Risk / Proximity Analysis
        ↓
Visual / Audio Alert
        ↓
Real-Time Output
```

---

# 🎯 Objectives

The major objectives of the project are:

* Develop a real-time pedestrian detection system.
* Detect pedestrians from live camera input.
* Detect pedestrians from recorded road videos.
* Apply YOLO-based deep learning for object detection.
* Use OpenCV for real-time image and video processing.
* Generate bounding boxes around detected pedestrians.
* Display confidence scores for detected pedestrians.
* Analyze pedestrian position within the camera frame.
* Identify pedestrians located in potentially dangerous regions.
* Generate visual warnings for pedestrian presence.
* Evaluate detection performance using standard metrics.
* Study the effect of environmental conditions on detection performance.
* Develop a research-oriented prototype suitable for ADAS applications.

---

# ⭐ Key Features

### 🚶 Pedestrian Detection

Automatically detects pedestrians appearing in the input image or video.

### 🎥 Real-Time Video Processing

Processes video frames continuously using OpenCV.

### 🧠 Deep Learning Detection

Uses a YOLO-based object detection model for fast inference.

### 📦 Bounding Boxes

Displays bounding boxes around detected pedestrians.

### 📊 Confidence Score

Shows the model's confidence for each detection.

### ⚠️ Safety Warning

Generates a warning when a pedestrian enters a predefined danger zone.

### 📍 Position Analysis

Analyzes the approximate position of detected pedestrians within the frame.

### 🔊 Alert System

The system can be extended to generate audio alerts when a pedestrian is detected at close proximity.

### 📈 Performance Evaluation

Evaluates the model using Precision, Recall, F1-Score, IoU, mAP and FPS.

---

# 🧠 Research Background

Pedestrian detection is a fundamental problem in computer vision and has been extensively studied for applications including **automotive safety, robotics and surveillance**.

The Caltech Pedestrian Dataset was introduced as a challenging benchmark containing pedestrian annotations collected from a vehicle driving through urban traffic. The dataset includes difficult cases such as low-resolution pedestrians and occlusions, making it useful for studying real-world pedestrian detection.

The original Caltech benchmark contains approximately **250,000 frames, 350,000 pedestrian bounding boxes and around 2,300 unique pedestrians**.

This project uses the dataset as a research foundation for developing and evaluating a real-time YOLO-based pedestrian detection pipeline.

---

# 🗂️ Dataset

## Primary Dataset: Caltech Pedestrian Dataset

The **Caltech Pedestrian Dataset** is selected because it was collected from a **vehicle-mounted camera in an urban traffic environment**, making it highly relevant to pedestrian detection for automotive and ADAS applications.

The dataset contains challenging examples involving:

* Pedestrians
* Urban traffic
* Low-resolution pedestrians
* Occluded pedestrians
* Different pedestrian positions
* Vehicle-mounted camera perspectives

The original dataset contains richly annotated video recorded from a moving vehicle.

---

## 🔗 Kaggle Dataset

**Caltech Pedestrian Dataset – Kaggle**

https://www.kaggle.com/datasets/kalvinquackenbush/caltechpedestriandataset

The Kaggle version provides a convenient way to access the dataset for experimentation and model development.

---

## 🔗 Original Dataset

**Caltech Pedestrians – California Institute of Technology**

https://data.caltech.edu/records/f6rph-90m20

The official dataset contains the original Caltech Pedestrian resources and annotations.

---

# 📊 Dataset Characteristics

The Caltech Pedestrian benchmark was collected from a vehicle driving through regular urban traffic.

Important characteristics include:

```text
Approximate Frames       : 250,000
Bounding Boxes            : 350,000
Unique Pedestrians        : ~2,300
Video Resolution          : 640 × 480
Camera                    : Vehicle-mounted
Environment               : Urban traffic
Main Task                 : Pedestrian Detection
```

The dataset also contains temporal correspondence and occlusion information, which makes it useful for research into difficult pedestrian-detection scenarios.

---

# 🧪 Alternative Dataset

For initial model development and quick experiments, the **Penn-Fudan Pedestrian Dataset** can also be used.

Kaggle:

https://www.kaggle.com/datasets/psvishnu/pennfudan-database-for-pedestrian-detection-zip

The Penn-Fudan dataset contains **170 images and 345 labeled pedestrians**, with images collected around the University of Pennsylvania and Fudan University.

However, because the primary objective of this project is **real-time pedestrian detection in road/automotive environments**, the Caltech Pedestrian Dataset is preferred as the main research dataset.

---

# 🛠️ Technologies Used

```text
Programming Language : Python
Computer Vision      : OpenCV
Deep Learning        : TensorFlow / PyTorch
Object Detection     : YOLO
Data Processing      : NumPy, Pandas
Visualization        : Matplotlib
Web Interface        : Streamlit
Development          : VS Code / Jupyter Notebook
Version Control      : Git / GitHub
```

---

# 🧠 Model Architecture

The project uses a YOLO-based object detection architecture.

YOLO follows a single-stage object detection approach where an input image is processed by the neural network to directly predict:

```text
Input Image
     ↓
Feature Extraction
     ↓
Feature Representation
     ↓
Bounding Box Prediction
     ↓
Class Prediction
     ↓
Confidence Score
     ↓
Non-Maximum Suppression
     ↓
Final Pedestrian Detection
```

The model identifies the pedestrian class and returns the corresponding bounding-box coordinates and confidence score.

---

# 🔍 Detection Pipeline

## Step 1 – Input Acquisition

The system accepts:

* Live webcam input
* CCTV/video input
* Recorded road videos
* Individual images

---

## Step 2 – Frame Extraction

OpenCV reads the incoming video stream frame by frame.

```python
cap = cv2.VideoCapture(0)

while True:
    ret, frame = cap.read()

    if not ret:
        break
```

---

## Step 3 – Preprocessing

Each frame is resized and prepared for inference.

Typical preprocessing operations include:

* Resizing
* Normalization
* Color conversion
* Tensor conversion

---

## Step 4 – YOLO Detection

The processed frame is passed to the YOLO model.

The model returns:

```text
Bounding Box
Class
Confidence Score
```

---

## Step 5 – Pedestrian Filtering

Only detections belonging to the pedestrian/person class are considered for the primary task.

```text
Detection
    ↓
Is detected class = Person?
    ↓
YES → Keep Detection
    ↓
NO → Ignore
```

---

## Step 6 – Bounding Box Generation

Bounding boxes are drawn around detected pedestrians.

Example:

```text
+---------------------------+
|                           |
|       ┌─────────┐         |
|       │ PERSON  │         |
|       │ 0.92    │         |
|       └─────────┘         |
|                           |
+---------------------------+
```

---

# ⚠️ Pedestrian Risk Analysis

An optional safety layer can be implemented after pedestrian detection.

The frame can be divided into regions:

```text
+--------------------------------------+
|              SAFE ZONE               |
|                                      |
|                                      |
|          WARNING ZONE                |
|                                      |
|       +------------------+           |
|       |   DANGER ZONE    |           |
|       |                  |           |
|       +------------------+           |
+--------------------------------------+
```

If a pedestrian enters the predefined danger zone, the system can generate a warning.

Example:

```text
Pedestrian detected
        ↓
Calculate bounding-box center
        ↓
Determine pedestrian position
        ↓
Check danger-zone boundaries
        ↓
Inside danger zone?
     /          \
   YES           NO
    ↓             ↓
WARNING        Continue
```

---

# 🔔 Alert Mechanism

The system can generate:

### Visual Alert

```text
⚠️ PEDESTRIAN DETECTED
```

### High-Risk Alert

```text
🚨 WARNING: PEDESTRIAN IN DANGER ZONE
```

### Audio Alert

An optional text-to-speech or audio notification can be implemented.

---

# 📁 Project Structure

```text
Real-Time-Pedestrian-Detection/
│
├── README.md
│
├── requirements.txt
│
├── dataset/
│   ├── images/
│   │   ├── train/
│   │   ├── val/
│   │   └── test/
│   │
│   └── labels/
│       ├── train/
│       ├── val/
│       └── test/
│
├── models/
│   └── pedestrian_model/
│
├── src/
│   ├── app.py
│   ├── detect.py
│   ├── preprocessing.py
│   ├── pedestrian_detection.py
│   ├── risk_analysis.py
│   └── alert_system.py
│
├── notebooks/
│   ├── data_analysis.ipynb
│   ├── preprocessing.ipynb
│   └── model_training.ipynb
│
├── results/
│   ├── detections/
│   ├── graphs/
│   └── metrics/
│
├── videos/
│   ├── input/
│   └── output/
│
└── requirements.txt
```

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone <repository-url>
```

## 2. Navigate to the Project

```bash
cd Real-Time-Pedestrian-Detection
```

## 3. Create Virtual Environment

```bash
python -m venv venv
```

## 4. Activate Virtual Environment

### Windows

```bash
venv\Scripts\activate
```

### Linux/macOS

```bash
source venv/bin/activate
```

---

# 📦 Install Dependencies

```bash
pip install -r requirements.txt
```

Example dependencies:

```text
opencv-python
numpy
pandas
matplotlib
torch
torchvision
ultralytics
streamlit
Pillow
scikit-learn
```

---

# ▶️ Running the Project

## Webcam Detection

```bash
python src/detect.py
```

## Streamlit Application

```bash
streamlit run src/app.py
```

The application can then be accessed through:

```text
http://localhost:8501
```

---

# 📥 Dataset Preparation

After downloading the dataset, organize the data according to the project's training pipeline.

Example:

```text
dataset/
│
├── images/
│   ├── train/
│   ├── val/
│   └── test/
│
└── labels/
    ├── train/
    ├── val/
    └── test/
```

The dataset should not be uploaded directly to GitHub because of its large size.

Add the dataset directory to `.gitignore`:

```text
dataset/
models/
results/
*.pt
*.pth
```

---

# 🏋️ Model Training

The model can be trained using a YOLO-compatible dataset configuration.

Example training workflow:

```text
Dataset
   ↓
Data Cleaning
   ↓
Annotation Conversion
   ↓
Train / Validation / Test Split
   ↓
Data Augmentation
   ↓
YOLO Training
   ↓
Validation
   ↓
Testing
   ↓
Performance Analysis
```

---

# 🔄 Data Preprocessing

The preprocessing stage may include:

* Image resizing
* Pixel normalization
* Annotation verification
* Removal of corrupted images
* Duplicate detection
* Dataset splitting
* Data augmentation

Possible augmentation techniques:

```text
Horizontal Flip
Brightness Adjustment
Contrast Adjustment
Scaling
Cropping
Rotation
Blur
Noise
```

Augmentation should be applied carefully because excessive transformations can create unrealistic road scenes.

---

# 🧪 Train / Validation / Test

The dataset should be divided into independent subsets.

```text
Dataset
   │
   ├── Training Set
   │       ↓
   │    Model Learning
   │
   ├── Validation Set
   │       ↓
   │    Hyperparameter / Model Selection
   │
   └── Test Set
           ↓
       Final Evaluation
```

The test set must remain separate from training to provide an unbiased estimate of model performance.

---

# 📈 Performance Evaluation

The following metrics will be used to evaluate the system.

## Precision

Measures how many predicted pedestrians are actually pedestrians.

```text
Precision = TP / (TP + FP)
```

---

## Recall

Measures how many actual pedestrians were successfully detected.

```text
Recall = TP / (TP + FN)
```

---

## F1-Score

Combines Precision and Recall.

```text
F1 = 2 × (Precision × Recall)
     -------------------------
     (Precision + Recall)
```

---

## Intersection over Union

IoU measures the overlap between the predicted bounding box and the ground-truth bounding box.

```text
IoU = Area of Intersection
      ----------------------
      Area of Union
```

---

## Mean Average Precision

mAP is used as a standard object-detection evaluation metric.

The project can report:

```text
mAP@0.5
mAP@0.5:0.95
```

---

## FPS

Frames Per Second measures real-time processing performance.

```text
FPS = Processed Frames / Time
```

Higher FPS generally indicates faster inference.

---

# 📊 Evaluation Parameters

| Metric         | Purpose                        |
| -------------- | ------------------------------ |
| Precision      | False-positive analysis        |
| Recall         | Missed pedestrian analysis     |
| F1-Score       | Overall classification balance |
| IoU            | Bounding-box accuracy          |
| mAP            | Object detection performance   |
| FPS            | Real-time performance          |
| Inference Time | Detection latency              |

---

# 🔬 Research Methodology

The project follows a systematic research methodology.

```text
Problem Identification
        ↓
Literature Review
        ↓
Dataset Selection
        ↓
Data Collection
        ↓
Data Preprocessing
        ↓
Model Selection
        ↓
Model Training
        ↓
Model Validation
        ↓
Real-Time Implementation
        ↓
Performance Evaluation
        ↓
Error Analysis
        ↓
Optimization
        ↓
Final Evaluation
```

---

# 📚 Research Questions

The project can investigate the following research questions:

### RQ1

How accurately can a YOLO-based model detect pedestrians in real-time road scenes?

### RQ2

How does pedestrian occlusion affect detection performance?

### RQ3

How does image resolution affect pedestrian detection accuracy?

### RQ4

What is the trade-off between detection accuracy and real-time FPS?

### RQ5

How does the model perform under different environmental and traffic conditions?

### RQ6

Can a lightweight YOLO model provide sufficient accuracy while maintaining real-time inference?

---

# 🧪 Experimental Design

The experiments can compare different model configurations.

Example:

```text
Experiment 1
Baseline YOLO Model
        ↓
Measure mAP, Precision, Recall and FPS

Experiment 2
YOLO + Data Augmentation
        ↓
Measure performance improvement

Experiment 3
Different Image Resolution
        ↓
Compare accuracy vs FPS

Experiment 4
Different Confidence Thresholds
        ↓
Analyze false positives and false negatives

Experiment 5
Real-Time Video Testing
        ↓
Measure inference latency and FPS
```

---

# 🔍 Error Analysis

Detection errors will be categorized into:

### False Positive

The system detects a pedestrian when there is no pedestrian.

### False Negative

A real pedestrian is missed by the system.

### Localization Error

The pedestrian is detected but the bounding box is inaccurate.

### Occlusion Error

A partially hidden pedestrian is not correctly detected.

### Small-Object Error

Distant pedestrians are difficult to detect.

---

# 🌦️ Environmental Testing

The system can be evaluated under different conditions:

| Condition           | Expected Challenge    |
| ------------------- | --------------------- |
| Daylight            | Baseline              |
| Low Light           | Reduced visibility    |
| Night               | Low illumination      |
| Crowded Road        | Multiple pedestrians  |
| Occlusion           | Partial visibility    |
| Distant Pedestrians | Small objects         |
| Motion Blur         | Reduced image quality |
| Complex Background  | False detections      |

---

# 🚗 Real-Time ADAS Application

The proposed pedestrian detector can act as one component of an ADAS pipeline.

```text
Camera
   ↓
Pedestrian Detection
   ↓
Pedestrian Position
   ↓
Distance / Proximity Analysis
   ↓
Risk Estimation
   ↓
Warning Generation
```

The system can therefore serve as a foundation for future intelligent vehicle safety systems.

---

# 🖥️ Expected Output

Example output:

```text
-----------------------------------------
     REAL-TIME PEDESTRIAN DETECTION
-----------------------------------------

Pedestrians Detected : 3

Person 1 : Confidence 0.94
Person 2 : Confidence 0.89
Person 3 : Confidence 0.76

FPS : 28.5

Status : SAFE
-----------------------------------------
```

When a pedestrian enters the danger region:

```text
-----------------------------------------
        🚨 SAFETY WARNING 🚨

     PEDESTRIAN DETECTED
       IN DANGER ZONE

          SLOW DOWN
-----------------------------------------
```

---

# 📊 Results

The final project should report experimental results using tables and graphs.

Example:

| Model               | Precision | Recall | F1  | mAP@0.5 | FPS |
| ------------------- | --------- | ------ | --- | ------- | --- |
| YOLO Baseline       | TBD       | TBD    | TBD | TBD     | TBD |
| YOLO + Augmentation | TBD       | TBD    | TBD | TBD     | TBD |
| Optimized Model     | TBD       | TBD    | TBD | TBD     | TBD |

> **Note:** Results should be filled only after actual experiments. No performance values should be fabricated.

---

# 📈 Visualization

The project can generate:

* Detection result images
* Confusion matrix
* Precision-Recall curve
* Training loss graph
* Validation loss graph
* mAP graph
* FPS comparison
* Confidence distribution
* Error analysis charts

---

# ⚠️ Limitations

The proposed system may face limitations such as:

* Low-resolution pedestrians
* Heavy occlusion
* Night-time conditions
* Rain and fog
* Motion blur
* Dense pedestrian crowds
* Small or distant pedestrians
* Camera quality limitations
* Hardware limitations
* False positives caused by complex backgrounds

The Caltech benchmark itself contains challenging low-resolution and frequently occluded pedestrians, making these conditions particularly relevant to evaluation.

---

# 🚀 Future Enhancements

Future versions of the project can include:

* Pedestrian tracking
* Multi-object tracking
* Distance estimation
* Depth estimation
* Pedestrian trajectory prediction
* Pedestrian intention prediction
* Crosswalk detection
* Traffic-sign detection
* Vehicle detection
* Lane detection
* Night-time pedestrian detection
* Thermal-camera detection
* Multi-camera detection
* Edge-AI deployment
* NVIDIA Jetson deployment
* Raspberry Pi deployment
* Mobile deployment
* Driver alert integration
* Automatic emergency braking research

---

# 🔮 Advanced Research Extension

A future research version can combine:

```text
YOLO
  +
OpenCV
  +
Object Tracking
  +
Depth Estimation
  +
Pedestrian Trajectory Prediction
  +
Risk Assessment
  +
Driver Alert
```

This can transform the basic pedestrian detector into a more complete **AI-based pedestrian safety system**.

---

# 🏆 Advantages

* Real-time pedestrian detection
* Deep-learning-based detection
* Automated detection process
* Bounding-box visualization
* Confidence-based predictions
* Potential ADAS application
* Can process live video
* Can process recorded videos
* Supports quantitative evaluation
* Suitable for academic research
* Can be extended to autonomous driving applications

---

# 🌍 Applications

The system can be applied to:

* Advanced Driver Assistance Systems
* Autonomous Vehicles
* Smart Transportation
* Intelligent Traffic Systems
* Road Safety
* CCTV Surveillance
* Pedestrian Monitoring
* Robotics
* Smart Cities
* Automotive Research

---

# 🔐 Safety Disclaimer

This project is an **academic and research prototype**.

It is not a certified automotive safety system and must not be used as the sole mechanism for real-world vehicle control, emergency braking, or autonomous driving.

Real-world deployment would require extensive validation, safety engineering, hardware testing, and compliance with applicable automotive standards.

---

# 📅 Development Roadmap

## Phase 1 – Research & Planning

**Status: Completed ✅**

* [x] Project topic selection
* [x] Problem identification
* [x] Technology selection
* [x] Initial dataset research
* [x] System workflow design

---

## Phase 2 – Dataset Preparation

**Status: In Progress 🔄**

* [ ] Download dataset
* [ ] Analyze dataset
* [ ] Clean data
* [ ] Convert annotations if required
* [ ] Create train/validation/test sets
* [ ] Apply preprocessing
* [ ] Apply suitable augmentation

---

## Phase 3 – Model Development

**Status: Pending ⏳**

* [ ] Select YOLO model
* [ ] Configure dataset
* [ ] Train model
* [ ] Validate model
* [ ] Tune confidence threshold
* [ ] Analyze errors
* [ ] Save best model

---

## Phase 4 – Real-Time Implementation

**Status: Pending ⏳**

* [ ] OpenCV camera integration
* [ ] Real-time inference
* [ ] Bounding-box visualization
* [ ] Confidence display
* [ ] FPS calculation
* [ ] Danger-zone implementation
* [ ] Warning system

---

## Phase 5 – Testing & Evaluation

**Status: Pending ⏳**

* [ ] Test on images
* [ ] Test on recorded videos
* [ ] Test webcam input
* [ ] Calculate Precision
* [ ] Calculate Recall
* [ ] Calculate F1-Score
* [ ] Calculate mAP
* [ ] Calculate IoU
* [ ] Measure FPS
* [ ] Perform error analysis

---

## Phase 6 – Finalization

**Status: Pending ⏳**

* [ ] Optimize model
* [ ] Complete documentation
* [ ] Generate graphs
* [ ] Prepare research results
* [ ] Prepare project demonstration
* [ ] Final GitHub repository
* [ ] Final presentation
* [ ] Research paper/report

---

# 📦 Deliverables

The final project will contain:

```text
✓ Source Code
✓ Trained Model
✓ Dataset Configuration
✓ Preprocessing Pipeline
✓ Real-Time Detection Application
✓ Detection Results
✓ Performance Metrics
✓ Graphs and Visualizations
✓ Research Documentation
✓ Project Report
✓ Research Paper
✓ Final Presentation
```

---

# 📚 References

1. Dollár, P., Wojek, C., Schiele, B., and Perona, P.
   **Pedestrian Detection: A Benchmark.**

2. Caltech Pedestrian Dataset
   https://data.caltech.edu/records/f6rph-90m20

3. Caltech Pedestrian Dataset – Kaggle
   https://www.kaggle.com/datasets/kalvinquackenbush/caltechpedestriandataset

4. Penn-Fudan Pedestrian Dataset – Kaggle
   https://www.kaggle.com/datasets/psvishnu/pennfudan-database-for-pedestrian-detection-zip

5. OpenCV Documentation
   https://docs.opencv.org/

---

# 📜 Dataset Citation

If the Caltech Pedestrian Dataset is used in the final research work, the original dataset and benchmark publication should be properly acknowledged.

```text
Piotr Dollár, Christian Wojek, Bernt Schiele,
and Pietro Perona.

"Pedestrian Detection: A Benchmark."

IEEE Transactions on Pattern Analysis and Machine Intelligence.
```

---

# 📄 License

This project is developed for **academic, educational, and research purposes**.

Dataset usage is subject to the respective dataset's terms and licensing conditions.

---

# 👨‍💻 Team

| Member          | ID             |
| --------------- | -------------- |
| **A. Srinivas** | **2420030349** |
| **M. Pranay**   | **2420030562** |
| **S. Roshan**   | **2420030528** |

---

# ⭐ Project Summary

**Real-Time Pedestrian Detection Using YOLO, OpenCV and Deep Learning** is an AI-based computer vision project designed to detect pedestrians from live and recorded road scenes.

The system combines:

```text
Deep Learning
      +
YOLO
      +
OpenCV
      +
Real-Time Video Processing
      +
Pedestrian Detection
      +
Risk Analysis
      +
Safety Alerts
```

The ultimate goal is to develop a **fast, accurate and research-oriented pedestrian detection system** that can serve as a foundation for future ADAS and intelligent transportation applications.

---

## 🚀 Project Status

**Research & Development Phase 🔄**

> Building an intelligent pedestrian detection pipeline for real-time road-safety applications.
