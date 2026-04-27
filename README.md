# TB Detection from Chest X-rays using Deep Learning

## 📌 Overview
This project focuses on automated detection of Tuberculosis (TB) from Chest X-ray (CXR) images
using deep learning techniques. The work evolves from baseline CNN models to advanced hybrid architectures
combining convolutional neural networks and transformer-based attention mechanisms.

---

## 🧠 Methodology Evolution

### Version 1: CNN Baseline
- Simple CNN architecture
- Achieved moderate performance

### Version 2: CNN + DenseNet121 (CheXNet)
- CLAHE preprocessing
- Data augmentation
- Transfer learning with DenseNet121

### Version 3: PyTorch DenseNet121 + Grad-CAM
- Framework transition (TensorFlow → PyTorch)
- Explainability using Grad-CAM

### Version 4: Hybrid CNN-Transformer (Proposed Model)
- ResNet50 backbone (feature extraction)
- Multi-head self-attention transformer blocks
- Grad-CAM visualization

---

## 📊 Results Comparison

| Model | Accuracy | AUC | Key Feature |
|------|---------|-----|------------|
| CNN Baseline | ~78% (val) | - | Basic CNN |
| DenseNet121 (TF) | 80.22% | 0.8763 | CLAHE + Transfer Learning |
| DenseNet121 (PyTorch) | 76.78% (val) | 0.8543 | Grad-CAM |
| Hybrid CNN-Transformer | 93.04% | 0.9860 | Attention + Global Features |
| ResNet50 + CLAHE (Final) | **92.76%** | **0.9856** | Deployment + Explainability |

---

## 🧪 Dataset
- Total Images: 2388
- Train: 1670
- Validation: 359
- Test: 359

---

## 🔍 Key Features
- Transfer Learning (DenseNet121, ResNet50)
- Image enhancement using CLAHE
- Data augmentation
- Grad-CAM for explainability
- Hybrid CNN + Transformer architecture

---
## 🌐 Deployment (Flask Web Application)

A web-based interface was developed using Flask to demonstrate real-world usability of the trained model.

### Features:
- Upload chest X-ray image
- Automated TB prediction
- Visual explanations for trust and interpretability

### Output Visualizations:
- Original X-ray image
- CLAHE enhanced image
- Grad-CAM heatmap
- Overlayed Grad-CAM on original image

### Purpose:
This deployment demonstrates how AI models can assist clinicians by providing both predictions and visual explanations, 
increasing trust and transparency in medical AI systems.

## 🚀 Key Findings
- ResNet50 + CLAHE achieves near state-of-the-art performance with simpler architecture and better deployability
- Hybrid CNN-Transformer significantly outperforms CNN-based models
- Attention mechanisms improve global feature understanding
- Grad-CAM improves interpretability and trust in predictions

---

## 📈 Future Work
- Fine-tuning transformer architecture
- Cross-dataset validation (Shenzhen, Montgomery, TBX11K)
- Model optimization for deployment
- Clinical validation and robustness testing

---

## 🧠 Research Direction
This project aims to contribute towards AI-assisted medical diagnosis systems and serves as a foundation for research publication and real-world deployment.