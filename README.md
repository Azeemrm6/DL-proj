# DL-proj
Deep Learning 2025 spring semester project

This project builds baseline and enhanced multimodal deep learning models for chest X-ray disease classification. By combining DenseNet-121 for image encoding and BioClinicalBERT for text encoding with cross-attention fusion, the goal is to improve classification accuracy by leveraging both visual and textual clinical information.


## 2. Setup
- Python version: 3.8+
- Install required packages:



# Chest X-ray Multimodal Disease Classification

##  Project Overview
This project focuses on automated disease classification from chest X-ray images, enhanced by combining radiology report texts using deep learning.  
We developed and compared two models:
- A **Baseline Model** (image-only classifier using DenseNet-121).
- An **Enhanced Multimodal Model** that fuses image features (DenseNet-121) and text features (BioClinicalBERT) through Cross-Attention Fusion.

Our goal is to demonstrate that leveraging both image and textual modalities improves disease classification performance compared to using images alone.

---

## Model Architectures

- **Baseline Model**:
  - DenseNet-121 backbone pretrained on ImageNet.
  - Fully connected classification head with dropout layers.
  - Image-only input.

- **Enhanced Multimodal Model**:
  - DenseNet-121 for X-ray image encoding.
  - BioClinicalBERT for radiology text encoding.
  - Cross-Attention Fusion mechanism for combining image and text features.
  - Fully connected classification head with dropout.
  - Text and image inputs.

## Training Details
Optimizer: Adam / AdamW

Scheduler: ReduceLROnPlateau
Loss Functions:
  Cross-Entropy Loss (Baseline)
  Focal Loss (Enhanced model, to handle class imbalance)
Data Augmentation:
   Random Resized Crop, Affine Transform, Horizontal Flip, Color Jittering
Class Balancing:
   Weighted Random Sampler and Class Weights


## Evaluation Metrics
Accuracy
Precision, Recall, F1-Score
ROC AUC Score (per class)
Confusion Matrix
Monte Carlo Dropout Uncertainty Estimation (Enhanced Model)



## Highlights

Multimodal fusion of chest X-ray and text reports using Cross-Attention.
Class imbalance handled with Focal Loss and weighted sampling.
Mixup data augmentation improves robustness.
Monte Carlo Dropout to measure model uncertainty at test time.

![Screenshot (30)](https://github.com/user-attachments/assets/d2349014-3ee7-4eaf-a388-f5a5774a66e0)


The above images shows how the enhanced model performs better than the baseline model
