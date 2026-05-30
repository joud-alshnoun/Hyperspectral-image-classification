# Hyperspectral-image-classification
# Hyperspectral Crop Disease Classification using Deep Learning

## Project Overview

This project was developed as part of the Deep Learning course (Spring 2026).

The objective is to classify hyperspectral crop images into three categories:
* Healthy
* Rust
* Other Diseases
  
The project focuses on processing high-dimensional hyperspectral imagery and applying deep learning techniques to accurately identify crop health conditions.

## Dataset

The dataset consists of hyperspectral images containing 125 spectral bands per image.
Each image represents a crop sample belonging to one of the following classes:
1. Healthy
2. Rust
3. Other

Due to the high dimensionality of hyperspectral data, dimensionality reduction techniques were applied before training the deep learning model.

## Methodology

### 1. Data Preprocessing

The preprocessing pipeline includes:

* Loading hyperspectral images
* Normalizing pixel values
* Handling missing or corrupted samples
* Converting images into tensors
* Creating training and testing datasets

### 2. Dimensionality Reduction

Principal Component Analysis (PCA) was applied to:

* Reduce computational complexity
* Remove redundant information
* Reduce overfitting
* Speed up model training

The original 125 spectral bands were transformed into a reduced set of principal components while preserving most of the useful information.

### 3. Deep Learning Model

The project utilizes a modified deep learning architecture based on EfficientNet-B3/Fusion Network to process hyperspectral data.

The model architecture consists of:

Hyperspectral Image
→ Preprocessing
→ PCA
→ Feature Extraction Network
→ Fully Connected Layer
→ Class Prediction

## Training Configuration

 Parameter:
 Optimizer: Adam               
 Loss Function: Cross Entropy Loss 
 Batch Size: 32                 
 Epochs: 50                 
 GPU : NVIDIA T4          

## Evaluation Metrics

Model performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Macro F1-Score
* Confusion Matrix

## Results

Final Evaluation Results:

 Metric:
 Accuracy: 74%   
 Macro F1 Score : 0.739 

Classification Report:

| Class   | Precision | Recall | F1-Score |
| ------- | --------- | ------ | -------- |
| Healthy | 0.67      | 0.57   | 0.62     |
| Rust    | 0.71      | 0.82   | 0.76     |
| Other   | 0.85      | 0.82   | 0.84     |

The model achieved its best performance on the "Other" class while maintaining competitive results on Rust disease detection.

## Running the Project

On Colab or Open the notebook:

jupyter notebook DeepLearning_Final_proj.ipynb 

Run all cells sequentially to:

1. Load the dataset
2. Apply PCA
3. Train the model
4. Evaluate performance
5. Generate metrics and visualizations

## Future Improvements

Possible future enhancements include:

* Using 5-fold cross-validation
* Applying advanced data augmentation techniques
* Exploring Vision Transformers (ViT)
* Incorporating multimodal remote sensing data
* Improving class balancing strategies

## Team Members

* Joud Al-Shnoun
* Heba Awwad
* Raneem Sabha

## Course Information

Course: Deep Learning
Semester: Spring 2026
University of Jordan

## Acknowledgments

This project was completed as part of the Deep Learning course project and focuses on applying modern deep learning techniques to hyperspectral crop disease classification.
