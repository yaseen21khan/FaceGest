# FaceGest: A Comprehensive Facial Gesture Dataset for Human-Computer Interaction

![FaceGest Banner](asset/facegest.png)

## Overview
**FaceGest** is a novel dataset designed for advancing research in **facial gesture recognition** for **Human-Computer Interaction (HCI)**. It includes a diverse collection of facial expressions, micro-expressions, and head movements captured in various lighting conditions and backgrounds, enabling robust model training and evaluation.

## Key Features
- **Diverse Expressions:** Includes a wide range of facial gestures (smiles, frowns, eyebrow raises, head nods, etc.).
- **High-Quality Annotations:** Carefully labeled with timestamps and expression categories.
- **Multi-Modal Data:** Contains RGB videos, depth maps, and landmark annotations.
- **Realistic Scenarios:** Captured in different lighting conditions and perspectives.

## Dataset Access
To request access to the dataset, please fill out the following form:

[Request FaceGest Dataset](https://example.com/request-form)

Once your request is approved, you will receive download instructions via email.

## Dataset Structure
The dataset is organized as follows:
```
FaceGest/
├── videos/              # Raw video recordings
├── images/              # Extracted keyframes
├── annotations/         # Facial landmarks and expression labels
├── depth/               # Depth maps (if available)
├── metadata/            # Subject details and conditions
└── README.md            # Project documentation
```

## Usage
### 1. Install Dependencies
Ensure you have the required libraries installed:
```bash
pip install opencv-python numpy pandas mediapipe
```
```bash
pip install tensorflow opencv-python numpy
```
### 2. Loading FaceGest using face-gest library
```bash
pip install face-gest-loader
```
### 2. Load and Visualize Samples
```python
import cv2
import numpy as np

# Load a sample video
video_path = 'videos/sample.mp4'
cap = cv2.VideoCapture(video_path)

while cap.isOpened():
    ret, frame = cap.read()
    if not ret:
        break
    cv2.imshow('FaceGest Sample', frame)
    if cv2.waitKey(25) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

## Benchmark Results
We evaluated FaceGest using the following models:

| Model        | Accuracy (%) | Precision (%) | Recall (%) |
|-------------|------------|--------------|------------|
| **Mediapipe**  | XX.XX      | XX.XX        | XX.XX      |
| **InceptionV4**| XX.XX      | XX.XX        | XX.XX      |
| **SqueezeNet** | XX.XX      | XX.XX        | XX.XX      |


## Applications
- **Human-Computer Interaction (HCI)**
- **Emotion Recognition**
- **Gesture-Based UI/UX Design**
- **Assistive Technologies**
- **Affective Computing**

## Citation
If you use **FaceGest** in your research, please cite:
```
@inproceedings{YourName2025FaceGest,
  author    = {Your Name and Collaborators},
  title     = {FaceGest: A Comprehensive Facial Gesture Dataset for Human-Computer Interaction},
  booktitle = {conference},
  year      = {2025}
}
```

