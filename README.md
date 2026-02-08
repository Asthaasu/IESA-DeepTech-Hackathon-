# IESA–NXP DeepTech Hackathon 2026  
## Edge-AI-Based Defect Classification System for Semiconductor Images

---

## 📌 Overview
This project is developed as part of the **IESA–NXP DeepTech Hackathon 2026**.  
The goal is to build a **real-time Edge-AI system** capable of detecting and classifying **semiconductor wafer and die defects** under **low-power edge constraints**, while maintaining high accuracy and low latency.

The solution demonstrates how **on-device AI inference** can significantly improve inspection speed and quality in modern semiconductor manufacturing.

---

## 🧠 Problem Statement
Semiconductor fabrication involves hundreds of tightly controlled steps, where even microscopic defects can lead to device failure. Traditional inspection systems rely on centralized servers or manual review, which suffer from:

- High latency
- Bandwidth bottlenecks
- Poor scalability
- High infrastructure cost

This project addresses these challenges by deploying a **lightweight AI model directly on edge hardware**, enabling **fast, reliable, and scalable defect classification**.

---

## 🗂 Dataset

### Classes (8)
The dataset is organized into the following defect categories:

- **Clean**
- **Bridge**
- **Open**
- **CMP**
- **Incomplete Etch**
- **Pattern Collapse**
- **Oxide Defect Thickness**
- **Other**

---

### Dataset Details
- **Total images:** 1120  
- **Classes:** 8  
- **Images per class:** ~140 (balanced)  
- **Image type:** Grayscale  
- **Resolution:** 224 × 224  

Sample defect images are included in the repository for reference.

---

## 🏗 Model Architecture

- **Base Model:** MobileNetV2 (ImageNet pretrained)
- **Custom Classification Head**
- **Trainable Parameters:** ~175K
- Designed for **low memory footprint** and **high inference speed**, making it suitable for edge deployment.

---

## 🏋️ Training Details

- **Framework:** TensorFlow 2.x
- **Optimizer:** Adam (learning rate = 0.001)
- **Loss Function:** Sparse Categorical Crossentropy
- **Data Augmentation:**
  - Horizontal & vertical flip
  - Rotation
  - Zoom
  - Brightness adjustment
  - Contrast adjustment
- **Training Time:** ~2 hours on MacBook M2

---

## 📊 Results

| Metric | Value |
|------|------|
| **Test Accuracy** | **91.88%** |
| **Precision** | 91.97% |
| **Recall** | 91.85% |
| **F1-Score** | 91.80% |

The model shows strong generalization across all defect classes.

---

## ⚡ Edge Deployment

- **Target Hardware:** NXP i.MX RT1170
- **Model Format:** TensorFlow Lite (INT8 quantized)
- **Model Size:** **0.22 MB**
- **Inference Speed:** **560 FPS**
- **Latency:** **~1.79 ms per inference**

The quantized model meets real-time inspection requirements while maintaining high accuracy.

---

## 🚧 Challenges Faced & Solutions

### 1. Dataset Variability
- **Challenge:** Class imbalance and defect variability  
- **Solution:** Heavy data augmentation and strict class balancing

### 2. Edge Constraints
- **Challenge:** Model size and inference speed limitations  
- **Solution:** MobileNetV2 backbone + INT8 quantization

---

## 🧪 Project Status
✅ Model trained and evaluated  
✅ Edge-optimized model generated  
🚧 Further testing and documentation in progress

---

## 🔗 References
- NXP eIQ AI Development Environment  
- IESA–NXP DeepTech Hackathon 2026 Problem Statement

---

## 🙏 Acknowledgements
This project was developed as part of the **IESA–NXP DeepTech Hackathon 2026**, focusing on practical applications of **Edge AI in semiconductor manufacturing**.


📁 Folder structure:
