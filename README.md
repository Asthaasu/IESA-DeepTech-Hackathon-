# IESA–NXP DeepTech Hackathon  
## Edge-AI-Based Defect Classification System for Semiconductor Images

### Overview
This project is developed as part of the **IESA–NXP DeepTech Hackathon 2026**.  
The objective is to design an **Edge-AI-powered system** capable of detecting and classifying defects in semiconductor wafer and die images in real time, while operating under **low-power edge constraints**.

The solution focuses on balancing **accuracy, latency, and computational efficiency**, reflecting real-world semiconductor manufacturing environments.

---

### Problem Statement
Modern semiconductor fabrication generates massive volumes of microscopic inspection images. Traditional cloud-based or manual inspection systems suffer from high latency, bandwidth limitations, and poor scalability.

This project aims to:
- Automatically detect defects in semiconductor wafer/die images
- Classify defects into predefined categories using AI/ML techniques
- Run efficiently on low-power edge devices without cloud dependency

---

### Defect Classes
The system targets a minimum of **8 classes**, including:

- Clean (No defect)
- Opens
- Bridges
- CMP 
- Oxide Defect Thickness
- Incomplete Etch
- Pattern Collapse
- Other

Images are processed in **grayscale (single-channel)** format to optimize edge deployment.

---

### Dataset
- Images - 1048
- Balanced class distribution
- Sources: Public datasets and curated samples
- Image type: Semiconductor wafer and die inspection images

---

### Methodology
1. **Data Collection & Preprocessing**
   - Image resizing and normalization
   - Grayscale conversion
   - Dataset balancing and augmentation

2. **Model Development**
   - Framework: TensorFlow / PyTorch
   - Language: Python
   - Approach: Custom CNN / Transfer Learning
   - Optimization for model size and inference speed

3. **Evaluation**
   - Accuracy
   - Precision
   - Recall
   - Confusion Matrix
   - Tested on both user-selected and hackathon-provided datasets

4. **Edge Deployment (Software Only)**
   - Model exported to **ONNX format**
   - Ported using **NXP eIQ AI Development Environment**
   - Target platform: **NXP i.MX RT series**
   - No physical hardware used (as per hackathon scope)

---

### Deliverables
- Curated dataset (.zip)
- Trained ML model (ONNX format)
- Evaluation metrics and confusion matrices
- Prediction results on hackathon test images
- NXP eIQ model stack output
- Complete source code
- Documentation of methodology and future scope

---

### Tech Stack
- **Programming Language:** Python  
- **ML Frameworks:** TensorFlow / PyTorch  
- **Model Format:** ONNX  
- **Edge AI Toolkit:** NXP eIQ  
- **Domain:** Semiconductor Manufacturing, Edge AI

---

### Project Status
🚧 **Work in Progress**  
Model training, optimization, and edge deployment are currently under development.

---

### Team
- **Asthaasu** – Project Lead & Developer

---

### References
- NXP eIQ AI Development Environment  
- IESA–NXP DeepTech Hackathon 2026 Problem Statement

---

### Acknowledgements
This project is developed as part of the **IESA–NXP DeepTech Hackathon**, aiming to explore practical applications of Edge AI in semiconductor manufacturing.
