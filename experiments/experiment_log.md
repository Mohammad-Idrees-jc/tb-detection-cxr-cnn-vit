Experiment 1: CNN Baseline
--------------------------
Description: Initial CNN model for TB detection from chest X-ray images.

Performance:
- Train Accuracy: 82%
- Validation Accuracy: 78%

Observations:
- Basic feature extraction
- Limited generalization capability

Status: Completed

--------------------------------------------------

Experiment 2: CNN + CLAHE + DenseNet121 (CheXNet)
-------------------------------------------------
Model: Pretrained DenseNet121 (CheXNet)

Preprocessing:
- CLAHE (Contrast Limited Adaptive Histogram Equalization)
- Data augmentation

Performance:
- Test Accuracy: 80.22%
- Test AUC: 0.8763
- Precision: 0.8428
- Recall: 0.7444

Observations:
- Improved feature extraction
- Better generalization compared to baseline
- Slight class imbalance effect observed

Status: Completed

--------------------------------------------------

Experiment 3: PyTorch DenseNet121 with Grad-CAM
----------------------------------------------
Framework: PyTorch
Model: Pretrained DenseNet121 (torchxrayvision)
Weights: densenet121-res224-all

Preprocessing:
- Image normalization
- Data augmentation
- CLAHE

Techniques:
- Transfer learning
- Grad-CAM for explainability

Performance:
- Training Accuracy: 80.42%
- Validation Accuracy: 76.78%
- Validation AUC: 0.8543
- Sensitivity: 0.7758

Observations:
- Improved interpretability with Grad-CAM
- Stable but moderate performance
- Slight drop compared to TensorFlow DenseNet version

Status: Completed

--------------------------------------------------

Experiment 4: Hybrid CNN-Transformer (ResNet50 + Multi-Head Attention)
----------------------------------------------------------------------
Architecture: Hybrid CNN-Transformer
Backbone: ResNet50 (Transfer Learning)
Transformer Blocks: 4
Embedding Dimension: 768
Attention Heads: 8

Preprocessing:
- Data augmentation
- Image normalization

Techniques:
- Transfer learning (ResNet50)
- Multi-head self-attention (Transformer)
- Grad-CAM visualization

Dataset:
- Total Images: 2388
- Train: 1670
- Validation: 359
- Test: 359

Performance:
- Best Validation AUC: 0.9949
- Test Accuracy: 0.9304
- Test AUC: 0.9860
- Test Loss: 0.1696

Observations:
- Significant improvement in classification performance
- Transformer enhances global feature understanding
- Excellent AUC indicates strong separability
- Grad-CAM shows better localization of infected regions

Conclusion:
- Hybrid CNN-Transformer outperforms all previous models
- Best candidate for final deployment and research publication

Status: Completed