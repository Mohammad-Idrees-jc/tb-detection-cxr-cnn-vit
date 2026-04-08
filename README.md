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

| Model 			|  Accuracy  |   AUC   |  Key Feature  |
|-----------------------	|------------|---------|---------------|
| CNN Baseline  		| ~78% (val) | -       | Basic CNN |
| DenseNet121 (TF)	 	| 80.22%     | 0.8763 | CLAHE + Transfer Learning |
| DenseNet121 (PyTorch) 	| 76.78% (val)| 0.8543 | Grad-CAM |
| Hybrid CNN-Transformer 	| **93.04%** | **0.9860** | Attention + Global Features |

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

## 🚀 Key Findings
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