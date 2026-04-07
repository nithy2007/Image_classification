# Fashion-MNIST Image Classification

## Introduction
This project focuses on the multi-class classification of the **Fashion-MNIST dataset**, which consists of 28x28 grayscale images of various clothing items. Each image is represented as a 784-dimensional feature vector, presenting a high-dimensional classification challenge.

## Objective
The primary goal is to predict the correct category (e.g., apparel, footwear, bag) for unseen images using both supervised and unsupervised learning techniques.

## Dataset Overview
* **Data Source**: Fashion-MNIST
* **Training Set**: 60,000 samples
* **Test Set**: 10,000 samples
* **Labels**: 10 classes (balanced with 6,000 training samples and 1,000 test samples per class)
* **Features**: 784 pixel values (0–255)

## Methodology

### 1. Data Preprocessing
* **Standardization**: Features were standardized to a mean of 0 and standard deviation of 1 to improve the performance of distance-based algorithms.
* **Dimensionality Reduction**: Principal Component Analysis (PCA) was applied to handle high dimensionality and improve computational efficiency.
* **Downsampling**: For specific computational needs, a balanced subset of 3,000 training samples (300 per class) was utilized.

### 2. Models Implemented
The project compares several machine learning models:
* **Supervised Learning**:
    * K-Nearest Neighbors (KNN)
    * Random Forest
    * Support Vector Machines (SVM) with RBF kernel
    * XGBoost (Gradient Boosting)
* **Unsupervised Learning**:
    * KMeans Clustering
    * Hierarchical Clustering

## Results and Findings
* **Best Performers**: **XGBoost** and **SVM (RBF)** achieved the highest overall performance with approximately **85% accuracy**.
* **Baseline Models**: Random Forest followed closely at ~83%, while KNN performed well for obvious categories with ~80% accuracy.
* **Unsupervised Results**: KMeans and Hierarchical clustering performed poorly for direct classification, as natural clusters often contained a mix of different clothing classes.
* **Class Specifics**:
    * **High Performance**: Bags and Ankle boots achieved F1-scores > 0.90.
    * **Challenging Classes**: "Shirts" proved to be the most difficult to classify (F1-scores 0.53–0.62) due to visual overlap with Pullovers and Coats.

## Libraries Used
* `pandas` 
* `scikit-learn`
* `xgboost` 
* `matplotlib` / `seaborn`

Overall, this project provides a comprehensive comparison of unsupervised and supervised learning techniques for image classification and demonstrates the challenges of classifying visually similar categories using traditional machine learning models.
