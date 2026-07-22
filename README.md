# Hybrid CNN-Transformer for Tuberculosis Detection from Chest X-ray Images

## Overview

Tuberculosis (TB) remains one of the leading infectious diseases worldwide, particularly in low-resource regions where expert radiologists and advanced diagnostic facilities are limited. Chest X-ray (CXR) analysis offers an inexpensive screening method; however, manual interpretation is time-consuming and subject to inter-observer variability.

This project presents a deep learning framework for automated TB detection from chest X-ray images. Throughout this research, multiple architectures were investigated, beginning with a baseline CNN and progressively evolving into an optimized Hybrid CNN-Transformer architecture incorporating transfer learning, image enhancement, explainable AI (Grad-CAM), and a Flask-based deployment system.

The objective is to develop a reliable, interpretable, and deployable AI-assisted diagnostic system.

---

# Repository Evolution

This repository documents the complete research journey.

Version 1
- CNN Baseline (TensorFlow/Keras)

Version 2
- CNN + CLAHE
- Data Augmentation
- DenseNet121 (CheXNet)

Version 3
- PyTorch implementation
- DenseNet121
- Grad-CAM visualization

Version 4
- Hybrid CNN-Transformer
- ResNet50 backbone
- Multi-head Self Attention
- Transfer Learning

Version 5
- ResNet50
- CLAHE preprocessing
- Flask deployment
- Explainable AI

Version 6 (Final)
- Hybrid CNN-Transformer
- DenseNet121 backbone
- Vision Transformer encoder
- CLAHE preprocessing
- Data Augmentation
- Mixup augmentation
- Cosine Annealing Warm Restarts
- Label Smoothing
- AdamW optimizer
- Gradient Clipping
- Explainable AI (Grad-CAM)
- Flask Web Application

---

# Dataset

Combined public datasets:

- Shenzhen
- Montgomery County
- TBX11K

Total Images

- Total : 2388
- TB : 1194
- Normal : 1194

Data Split

- Train : 1670
- Validation : 359
- Test : 359

---

# Proposed Architecture

Final architecture consists of:

Input Chest X-ray

↓

CLAHE Enhancement

↓

Data Augmentation

↓

DenseNet121 Backbone (Transfer Learning)

↓

Patch Embedding

↓

Transformer Encoder (4 Multi-Head Attention Blocks)

↓

Classification Head

↓

TB / Normal Prediction

↓

Grad-CAM Explainability

---

# Final Hyperparameters

Image Size : 320 × 320

Batch Size : 16

Embedding Dimension : 768

Transformer Blocks : 4

Attention Heads : 8

MLP Dimension : 2048

Dropout : 0.20

Epochs : 60

Optimizer : AdamW

Learning Rate : 5e-5

Weight Decay : 5e-5

Scheduler : CosineAnnealingWarmRestarts

Mixup : Enabled

Label Smoothing : 0.05

Gradient Clipping : Enabled

Random Seed : 42

---

# Final Results

Test Accuracy

95.54%

Test AUC

0.9926

Test Loss

0.2322

Classification Performance

Precision

Normal : 0.96

TB : 0.95

Recall

Normal : 0.95

TB : 0.96

F1-score

Normal : 0.96

TB : 0.96

---

# Performance Comparison

| Version | Model | Accuracy | AUC |
|----------|-------------------------------|---------|--------|
| V1 | CNN Baseline | 78% (Validation) | - |
| V2 | DenseNet121 + CLAHE | 80.22% | 0.8763 |
| V3 | DenseNet121 (PyTorch) | 76.78% | 0.8543 |
| V4 | Hybrid CNN-Transformer (ResNet50) | 93.04% | 0.9860 |
| V5 | ResNet50 + CLAHE | 92.76% | 0.9856 |
| **V6** | **Hybrid DenseNet121 + Transformer** | **95.54%** | **0.9926** |

---

# Explainable AI

Grad-CAM is integrated into the final system.

The web application displays:

- Original Chest X-ray

- CLAHE Enhanced Image

- Grad-CAM Heatmap

- Overlayed Heatmap

This improves model interpretability and helps clinicians understand prediction regions.

---

# Flask Deployment

A Flask web application was developed for real-world deployment.

Features

- Upload Chest X-ray

- Automatic TB prediction

- Prediction confidence

- CLAHE visualization

- Grad-CAM visualization

- Overlay visualization

---

# Repository Structure

```
TB_Detection_Project/

│

├── notebooks/

├── deployment/

├── experiments/

├── models/

├── results/

├── paper/

├── thesis/

├── README.md

├── requirements.txt

└── LICENSE
```

---

# Research Outputs

This project produced:

✔ Undergraduate Final Year Thesis

✔ Research Preprint (Zenodo)

✔ Flask-based AI Diagnostic System

✔ Hybrid CNN-Transformer Architecture

---

# Future Work

- External clinical validation

- Domain adaptation

- Model uncertainty estimation

- Lightweight deployment for edge devices

- Multi-class chest disease classification

---

# Citation

If you use this work, please cite the accompanying preprint available on Zenodo.

(CITATION.cff included in repository)

---

# Author

Mohammad Idrees

Bachelor of Computer Science

Final Year Project

Hybrid CNN-Transformer for Tuberculosis Detection from Chest X-ray Images