# 🗑️ TrashBot — AI-Based Framework for Automated Waste Segregation

> Bachelor's Thesis · Fatima Jinnah Women University, Rawalpindi · July 2023  
> Supervised by Dr. Aamir Arsalan & Dr. Saria Safdar

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![TensorFlow Lite](https://img.shields.io/badge/TensorFlow%20Lite-FF6F00?style=flat&logo=tensorflow&logoColor=white)](https://tensorflow.org/lite)
[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)](https://flutter.dev)
[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi%204-A22846?style=flat&logo=raspberrypi&logoColor=white)](https://raspberrypi.org)
![Accuracy](https://img.shields.io/badge/Classification%20Accuracy-87%25-brightgreen?style=flat)

---

## Overview

TrashBot is an end-to-end AI framework for automated household and commercial waste segregation. The system combines a CNN-based image classification model deployed on a Raspberry Pi 4 with a cross-platform Flutter mobile application, forming a complete smart bin ecosystem that eliminates the need for manual waste sorting.

Manual waste segregation is hazardous, time-consuming, and error-prone. TrashBot addresses this by automating the classification and physical segregation of waste in real time, while providing users with waste analytics and environmental awareness features through a companion app.

---

## System Architecture

```
Camera Input (Raspberry Pi 4)
        │
        ▼
CNN Image Classifier (TensorFlow Lite)
        │
        ▼
Waste Category Prediction
        │
        ├─── Physical Bin Sorting (Hardware)
        │
        └─── Flutter App (Android / iOS / Desktop)
                    │
                    ├─── Daily & Monthly Waste Reports
                    ├─── Bin Collection Scheduling
                    └─── Environmental News Feed
```

---

## Model Performance

The CNN model was trained to classify waste into **7 categories**: battery, cardboard, glass, metal, paper, plastic, and general trash.

| Metric | Value |
|--------|-------|
| Overall Accuracy | **87%** |
| Training Epochs | 50 |
| Deployment Format | TensorFlow Lite (`.tflite`) |
| Hardware Target | Raspberry Pi 4 |

The model was trained over 50 epochs, with training accuracy converging to ~90% and test accuracy stabilising at ~87%, as shown in the accuracy curve below.

Per-class performance (from confusion matrix):

| Category | Correctly Classified |
|----------|---------------------|
| Paper | 546 |
| Glass | 480 |
| Metal | 405 |
| Battery | 385 |
| Cardboard | 367 |
| Plastic | 340 |

---

## Features

**Smart Bin (Hardware)**
- Real-time waste image capture and classification via Raspberry Pi 4
- Automated physical segregation into category-specific compartments
- Bin-full notification sent to the companion app

**Mobile Application (Flutter)**
- Cross-platform: Android, iOS, Linux, macOS, Windows
- Bin scheduling — book a waste collection slot
- Daily and monthly waste reports for usage analytics
- Environmental news feed to promote waste-aware behaviour
- User registration, login, and personalised settings

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| ML Model | CNN (Convolutional Neural Network) |
| Edge Deployment | TensorFlow Lite |
| Mobile App | Flutter (Dart) |
| Hardware | Raspberry Pi 4 |
| Training Environment | Python, Jupyter Notebook |

---

## Repository Structure

```
TRASHBOT.io/
├── WasteClassification.ipynb   # Model training and evaluation notebook
├── wasteclassification_final.py # Core classification script
├── model.tflite                 # Trained TFLite model for edge deployment
├── ABSTRACT.txt                 # Project abstract
└── pubspec.yaml                 # Flutter app dependencies
```

---

## Getting Started

### Prerequisites
- Python 3.8+
- TensorFlow / TensorFlow Lite
- Flutter SDK
- Raspberry Pi 4 with camera module

### Run the classifier

```bash
pip install tensorflow numpy pillow
python wasteclassification_final.py
```

### Open the training notebook

```bash
jupyter notebook WasteClassification.ipynb
```

### Build the Flutter app

```bash
flutter pub get
flutter run
```

---

## Results

The TrashBot system achieved **87% classification accuracy** across 7 waste categories using a CNN with object detection, trained on a custom waste image dataset. The model was successfully compressed to TFLite format and deployed on a Raspberry Pi 4 for real-time inference, demonstrating a complete edge-AI pipeline from model training to embedded deployment.

---

## Authors

- Hala Ali Khan — [GitHub](https://github.com/HalaKhan00) · [LinkedIn](https://www.linkedin.com/in/hala-ali-khan/)
- Mahrukh Ali Khan
- Arshiya Saleem

**Supervisors:** Dr. Aamir Arsalan · Dr. Saria Safdar  
**Institution:** Department of Software Engineering, Fatima Jinnah Women University, Rawalpindi
