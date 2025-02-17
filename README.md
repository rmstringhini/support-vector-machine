The SVM (Support Vector Machine) is a supervised machine learning algorithm used for both classification and regression tasks. The SVM model aims to find the best decision boundary (also called a hyperplane) that separates classes in the dataset while maximizing the margin between the two closest data points of different classes. These closest data points are called support vectors.

If the data is linearly separable, SVM finds a straight-line hyperplane (2D) or a flat plane (in higher dimensions) that maximizes the distance (margin) between the classes.
If data is non-linearly separable, SVM uses the kernel trick to map data to a higher-dimensional space where it can become linearly separable.

How SVM works:

1) Input data:
   - Obtain the feature vectors of each data point and their corresponding labels.
  
2) Find the best hyperplane:
   - A hyperplane is a decision boundary that separates classes.
   - The equation of the hyperplane in 2D is:
     $w^T + b = 0$


