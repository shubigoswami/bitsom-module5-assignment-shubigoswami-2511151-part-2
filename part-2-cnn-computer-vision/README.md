# CNN-Based Manufacturing Defect Classification

## Project Overview

This project builds a Convolutional Neural Network (CNN) model to classify manufacturing product surface images into four categories:

- Normal
- Scratch
- Dent
- Stain

The objective is to automate defect detection using computer vision techniques for manufacturing quality inspection.

---

# Dataset Description

The dataset contains images divided into four classes:

| Class | Description |
|---|---|
| normal | Product surface without defects |
| scratch | Surface with scratch-like marks |
| dent | Surface with dent-like patterns |
| stain | Surface with stain or discoloration |

Dataset Structure:

images/
- normal/
- scratch/
- dent/
- stain/

labels.csv

---

# Problem Identification

This dataset represents an **Image Classification** problem because:

- Each image belongs to one single class
- The model predicts one label per image
- No object localization or segmentation masks are provided

Other computer vision tasks such as object detection or segmentation are not suitable because the dataset does not contain bounding boxes or pixel-level annotations.

---

# Dataset Exploration

The dataset was analyzed by:

- Counting the number of images in each class
- Visualizing sample images
- Checking image dimensions
- Identifying any class imbalance

The dataset contains four image categories:
- Normal
- Scratch
- Dent
- Stain

---

# Image Preprocessing

The following preprocessing steps were performed:

- Resized all images to 128 × 128
- Normalized pixel values to range [0,1]
- Split dataset into training and validation sets
- Applied data augmentation:
  - Rotation
  - Zoom
  - Horizontal flipping

---

# CNN Model Architecture

The CNN model consists of:

1. Convolution Layers
2. ReLU Activation Function
3. Max Pooling Layers
4. Flatten Layer
5. Dense Fully Connected Layer
6. Dropout Layer
7. Softmax Output Layer

The model was built using TensorFlow/Keras.

---

# Model Training

The model was trained using:

- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Evaluation Metric: Accuracy
- Epochs: 10
- Batch Size: 32

---

# Results

The following outputs were generated:

- Accuracy and Loss Curves
- Confusion Matrix
- Sample Predictions

The CNN model successfully learned defect patterns and achieved good classification performance.

---

# Task 6 : CNN Concept Explanation

## What is Convolution?

Convolution is an operation where small filters scan across an image to detect important visual features such as edges, textures, scratches, dents, and stains.

---

## Why is Pooling Used?

Pooling reduces the size of feature maps while keeping important information. It helps reduce computation and prevents overfitting.

---

## Why is ReLU Commonly Used in CNNs?

ReLU (Rectified Linear Unit) introduces non-linearity into the network and helps the model learn complex image patterns efficiently.

---

## Why are CNNs Better than Regular Feed-Forward Networks for Image Data?

CNNs are specifically designed for image processing. They automatically extract spatial features from images while using fewer parameters than traditional neural networks.

---

# Task 7 : Business Use Case Mapping

## Manufacturing Quality Inspection

Computer vision systems using CNNs can automatically inspect products for defects such as scratches, dents, and stains.

Benefits include:

- Faster inspection
- Reduced manual effort
- Improved quality control
- Lower manufacturing errors
- Increased production efficiency

This type of solution is commonly used in:
- Automotive manufacturing
- Electronics production
- Metal surface inspection
- Industrial automation

---

# Technologies Used

- Python
- TensorFlow/Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# Repository Structure

part-2-cnn-computer-vision/

├── README.md
├── notebook.ipynb
├── requirements.txt
├── sample_predictions/
│   └── prediction_outputs.png
└── results/
    ├── accuracy_loss_curves.png
    └── confusion_matrix.png

---

# Conclusion

This project demonstrates how CNN-based computer vision models can be used for automated manufacturing defect classification. The model successfully identifies different defect categories and shows the practical application of deep learning in industrial quality inspection.