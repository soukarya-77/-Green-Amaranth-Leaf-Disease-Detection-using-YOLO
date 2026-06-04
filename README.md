# 🌿 Green Amaranth Leaf Disease Detection using YOLO

## 📌 Overview

This project presents a deep learning-based solution for detecting diseases in Green Amaranth leaves using the YOLO (You Only Look Once) object detection framework. The system identifies diseased and healthy leaves in real time, helping farmers, vendors, and agricultural inspectors take early preventive measures.

This work is one of the first attempts to apply object detection techniques to Green Amaranth leaf disease identification.

---

## 🎯 Objectives

* Collect Green Amaranth leaf images from real-world environments.
* Extract image frames from videos using OpenCV.
* Annotate diseased and healthy leaves using Roboflow.
* Train YOLOv8m and YOLOv9m models.
* Compare model performance using detection metrics.
* Build a baseline system for real-time disease detection.

---

## 🚀 Features

* Real-time leaf disease detection.
* Custom dataset generation from video frames.
* Two-class object detection:

  * Diseased Leaf
  * Healthy Leaf
* Data augmentation for improved robustness.
* Performance comparison between YOLOv8m and YOLOv9m.
* Suitable for precision agriculture applications.

---

## 🛠️ Technologies Used

* Python
* OpenCV
* Roboflow
* YOLOv8m
* YOLOv9m
* Ultralytics Framework
* Deep Learning

---

## 📂 Dataset Creation

### Data Collection

* Videos collected from gardens across:

  * West Bengal
  * Assam
  * Sikkim

### Frame Extraction

* Extracted frames every 10 ms (100 FPS).
* Approximately 1600+ frames generated.

### Annotation

* Platform: Roboflow
* Bounding boxes drawn around visible leaves.

### Classes

| Class ID | Label       |
| -------- | ----------- |
| 0        | Disease     |
| 1        | Not Disease |

---

## 🔄 Data Augmentation

The following augmentation techniques were applied:

* Rotation (-10° to +10°)
* Grayscale Conversion (10% images)
* Brightness Adjustment (±20)
* Gaussian Blur
* Random Transformations

These augmentations improve model generalization and reduce overfitting.

---

## 🧠 Model Architecture

### YOLOv8m

* Input Size: 640 × 640
* Parameters: 25.9M
* FLOPs: 78.9B

### YOLOv9m

* Input Size: 640 × 640
* Parameters: 20.1M
* FLOPs: 76.8B

---

## ⚙️ Training Configuration

| Parameter              | Value            |
| ---------------------- | ---------------- |
| Train/Validation Split | 80/20            |
| Epochs                 | 5                |
| Optimizer              | SGD              |
| Framework              | Ultralytics      |
| GPU                    | NVIDIA RTX A4000 |
| RAM                    | 128 GB           |
| CPU                    | Intel Core i7    |

---

## 📊 Results

### YOLOv8m

| Metric       | Value |
| ------------ | ----- |
| Precision    | 0.487 |
| Recall       | 0.477 |
| mAP@0.5      | 0.422 |
| mAP@0.5:0.95 | 0.177 |
| F1 Score     | 0.48  |

### YOLOv9m

| Metric       | Value |
| ------------ | ----- |
| Precision    | 0.461 |
| Recall       | 0.432 |
| mAP@0.5      | 0.346 |
| mAP@0.5:0.95 | 0.150 |

---

## 🏆 Key Findings

* YOLOv8m outperformed YOLOv9m.
* YOLOv8m achieved:

  * 21.7% higher mAP@0.5
  * 18.1% higher mAP@0.5:0.95
* Faster convergence and lower loss values.
* Better localization and classification performance.

---

## 📈 Evaluation Metrics

* Precision
* Recall
* F1 Score
* mAP@0.5
* mAP@0.5:0.95
* Classification Loss
* Bounding Box Loss
* Distribution Focal Loss (DFL)

---

## 🌍 Applications

* Smart Agriculture
* Precision Farming
* Crop Health Monitoring
* Disease Surveillance
* Food Safety Management
* Agricultural Research

---

## 🔮 Future Work

* Increase dataset size.
* Include more disease categories.
* Train with 100+ epochs.
* Hyperparameter optimization.
* Deploy on smartphones.
* Deploy on edge devices.
* Build a farmer-friendly mobile application.

---

## 📄 Publication

**Utilizing YOLO Framework for Green Amaranth Leaf Disease Detection**

Presented at:
**5th IEEE International Conference on Artificial Intelligence and Signal Processing (AISP 2025)**

---

