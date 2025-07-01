# Image Classification using Convolutional Neural Networks (CNN)

This repository demonstrates an image classification project using Convolutional Neural Networks (CNNs) with TensorFlow and Keras. The project explores how varying the number of filters and kernel sizes in convolutional layers affects classification performance, as detailed in the included laboratory report.

## Project Overview

- **Goal:** Classify images using a CNN and analyze the impact of different convolutional configurations.
- **Dataset:** Loaded using Keras' `ImageDataGenerator`, with real-time augmentation and normalization.
- **Tech Stack:** Python, TensorFlow, Keras, NumPy, Matplotlib, scikit-learn.

## Approach

1. **Data Preparation:**  
   Images are loaded and augmented in real time for training and validation using `ImageDataGenerator`.
2. **Model Building:**  
   Multiple Sequential CNN architectures are constructed, each with different numbers of filters and kernel sizes.
3. **Training & Evaluation:**  
   Each model is trained and evaluated using accuracy, precision, recall, F1-score, and confusion matrix.
4. **Experimentation:**  
   Four different CNN configurations are tested to analyze the impact of architecture choices on model performance.
5. **Analysis:**  
   The laboratory report (included as a PDF) details each experiment, the observed metrics, and conclusions regarding the most effective configurations.

## Experiments Conducted

- **Baseline:** 16-32-64 filters, 3x3 kernels
- **Increased filters and kernel size:** 32-64-128 filters, 5x5 and 3x3 kernels
- **Larger kernels:** 16-32-64 filters, all 5x5 kernels
- **High filters, small kernels:** 32-64-128 filters, all 3x3 kernels

Findings show that a balanced configuration (16–32–64 filters, 3×3 kernels) gives the best trade-off between recall and specificity, while overly large filters/kernels may lead to overfitting and poor specificity.

## How to Use

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/image-classification-cnn.git
cd image-classification-cnn
```

### 2. Install dependencies
All required libraries are listed in requirements.txt:
```bash
pip install -r requirements.txt
```

### 3. Prepare the dataset
- Place your image dataset in the correct folder structure (see notebook for details).
- The code uses Keras ImageDataGenerator with flow_from_directory, so images should be organized in subfolders by class.

### 4.  Run the notebook
```bash
jupyter notebook ImageClassification.ipynb
```
Follow the cells to experiment with different CNN architectures and view evaluation metrics.

