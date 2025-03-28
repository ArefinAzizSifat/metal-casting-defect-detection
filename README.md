# metal-casting-defect-detection
A CNN-based image classification project to detect defective metal castings using TensorFlow and Keras.
# 🏭 Metal Casting Defect Detection Using CNN

## 📌 Project Overview

This project focuses on detecting defective metal castings using a **Convolutional Neural Network (CNN)** built with **TensorFlow** and **Keras**. The model classifies whether a metal part is **defective (`def_front`)** or **non-defective (`ok_front`)** based on 2D grayscale images.

✅ The goal: **Automate quality control** in manufacturing processes using deep learning.

---

## 🧠 Model Architecture

The CNN model was built from scratch with the following structure:

- `Conv2D(32, 3x3)` + ReLU  
- `MaxPooling2D(2x2)`
- `Conv2D(64, 3x3)` + ReLU  
- `MaxPooling2D(2x2)`
- `Flatten`
- `Dense(128)` + ReLU
- `Dropout(0.6)` – for regularization
- `Dense(1)` + Sigmoid (binary classification)

**Loss Function**: `Binary Crossentropy`  
**Optimizer**: `Adam`  
**Evaluation Metric**: `Accuracy`

---

## 🗂️ Dataset Info

- **Source**: [Kaggle – Casting Product Image Data for Quality Inspection](https://www.kaggle.com/datasets/ravirajsinh45/real-life-industrial-dataset-of-casting-product)
- **Images**: Grayscale, size `300x300`
- **Categories**:
  - `ok_front/` — Non-defective parts  
  - `def_front/` — Defective parts  
- **Preprocessing**:
  - Resized to `128x128`
  - Normalized (pixel values scaled to 0–1)
  - Data Augmentation (rotation, shifting, zoom, flip)

---

## 🛠️ How to Run

> You can run this project using **Google Colab**.

### 🔹 1. Clone the Repository
```bash
git clone https://github.com/yourusername/metal-casting-defect-detection.git
