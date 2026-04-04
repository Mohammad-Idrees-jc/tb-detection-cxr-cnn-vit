Experiment 1: CNN Baseline
--------------------------
Description: Initial CNN model for TB detection from chest X-ray images.
Status: completed

Experiment 2: CNN + CLAHE + DenseNet121 (CheXNet)
-------------------------------------------------
Model: Pretrained DenseNet121 (CheXNet)
Preprocessing:
- CLAHE (Contrast Limited Adaptive Histogram Equalization)
- Data augmentation

Observations:
- Improved feature extraction
- Better generalization expected

Status: completed

Experiment 3: PyTorch DenseNet121 with Grad-CAM
----------------------------------------------
Framework: PyTorch
Model: Pretrained DenseNet121 (torchxrayvision)
Weights: densenet121-res224-all

Preprocessing:
- Image normalization
- Data augmentation
- CLAHE (Contrast Limited Adaptive Histogram Equalization)

Techniques:
- Transfer learning
- Grad-CAM for explainability

Observations:
- Improved interpretability through Grad-CAM visualization
- Better feature localization on lung regions

Status: In progress