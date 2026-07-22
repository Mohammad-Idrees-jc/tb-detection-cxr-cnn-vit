# Experiment Log

This document records the chronological evolution of the project.

---

## Experiment 1

Model

CNN Baseline

Framework

TensorFlow / Keras

Objective

Develop a simple CNN baseline for TB classification.

Performance

Training Accuracy

82%

Validation Accuracy

78%

Observations

- Basic feature extraction.
- Established baseline performance.

Status

Completed

---

## Experiment 2

Model

DenseNet121 (CheXNet)

Framework

TensorFlow / Keras

Improvements

- CLAHE preprocessing
- Data augmentation
- Transfer Learning

Performance

Accuracy

80.22%

AUC

0.8763

Observations

- Improved generalization.
- Better feature representation.

Status

Completed

---

## Experiment 3

Model

DenseNet121

Framework

PyTorch

Improvements

- Migration to PyTorch
- Grad-CAM
- Transfer Learning

Performance

Validation Accuracy

76.78%

Validation AUC

0.8543

Observations

- Improved explainability.
- Framework transition completed successfully.

Status

Completed

---

## Experiment 4

Model

Hybrid CNN-Transformer

Backbone

ResNet50

Improvements

- Multi-head Self Attention
- Transformer Encoder
- Grad-CAM

Performance

Accuracy

93.04%

AUC

0.9860

Observations

- Significant improvement.
- Strong global feature learning.

Status

Completed

---

## Experiment 5

Model

ResNet50

Improvements

- CLAHE
- Data augmentation
- Flask Deployment

Performance

Accuracy

92.76%

AUC

0.9856

Deployment

Flask application

Features

- Image Upload
- CLAHE
- Grad-CAM
- Overlay visualization

Status

Completed

---

## Experiment 6 (Final)

Model

Hybrid CNN-Transformer

Backbone

DenseNet121

Major Improvements

- DenseNet121 backbone
- Vision Transformer
- CLAHE preprocessing
- Mixup
- Label smoothing
- Cosine Annealing Warm Restarts
- AdamW
- Gradient clipping
- Transfer learning
- Explainable AI
- Flask deployment

Dataset

2388 Chest X-rays

Training

1670

Validation

359

Testing

359

Performance

Test Accuracy

95.54%

Test AUC

0.9926

Test Loss

0.2322

Classification

Precision

Normal : 0.96

TB : 0.95

Recall

Normal : 0.95

TB : 0.96

F1-score

Normal : 0.96

TB : 0.96

Outputs

- best_model.pth
- pipeline_info.json
- ROC Curve
- Confusion Matrix
- Training History
- CLAHE Preview
- Grad-CAM Visualization

Deployment

Flask web application

Capabilities

- Upload chest X-ray
- Automatic prediction
- CLAHE enhancement
- Grad-CAM heatmap
- Overlay visualization

Conclusion

The final Hybrid CNN-Transformer using a DenseNet121 backbone achieved the best overall performance (95.54% accuracy and 0.9926 AUC), while also providing explainable predictions and a deployable clinical prototype. This version represents the culmination of the research and serves as the foundation for the accompanying undergraduate thesis and Zenodo preprint.

Status

Final Version (v2.0)