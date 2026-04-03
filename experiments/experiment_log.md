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

Status: In progress