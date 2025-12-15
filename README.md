# Image_classification
In this project, we analyze the Fashion-MNIST dataset, which consists of grayscale images of clothing/footwear/bag. The primary objective is to perform multi-class classification to predict the correct apparel category for unseen images.
Each image is represented as a 28 × 28 pixel grid, resulting in a high-dimensional feature space of 784 pixel values per observation.
In addition to supervised learning, we also explore unsupervised learning techniques to understand the intrinsic structure of the data and assess whether natural groupings align with the true class labels.

Given the high dimensionality of the data, several pre-processing steps are applied, including feature scaling and dimensionality reduction using Principal Component Analysis (PCA). These steps are essential to improve computational efficiency and model performance, particularly for distance-based and margin-based algorithms.

For unsupervised learning, clustering methods such as K-Means and Hierarchical Clustering are applied to the training data. Cluster quality is evaluated using metrics such as the silhouette score, and the relationship between clusters and true class labels is examined to determine whether clustering can meaningfully separate apparel categories.

For supervised learning, multiple multi-class classification models are implemented and compared, including K-Nearest Neighbors (KNN), Random Forest, Support Vector Machines (SVM), and Gradient Boosting (XGBoost). Model performance is evaluated using classification accuracy and detailed class-wise metrics such as precision, recall, and F1-score. The comparative analysis highlights the strengths and limitations of each approach when applied to high-dimensional image data represented by raw pixel features.

Overall, this project provides a comprehensive comparison of unsupervised and supervised learning techniques for image classification and demonstrates the challenges of classifying visually similar categories using traditional machine learning models.
