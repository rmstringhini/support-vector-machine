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

     where:

     - _w_ is the weight vector (determines the orientation of the hyperplane)
     - _b_ is the bias term (shifts the hyperplane)
     - _x_ is the input feature vector
    
  - Among all possible hyperplanes, SVM selects the one that maximizes the margin (distance between the closest points of both classes, known as support vectors).
  - Margin: the distance between the hyperplane and the nearest data points.
  - Support vectors: the data points that lie closest to the hyperplane.

  - For linearly separable data, the constraints for correction classification are:
    $y_i(w^Tx_i+b)\geqslant 1$
  
  - The goal is to maximize the margin, which is equivalent to minimizing:
    $\frac{1}{2}\left | \left | w\right |\right |^2$ 
    
3) Handling non-linearly separable data (kernel trick):
   - When data is not linearly separable (it cannot be separated by a straight line), SVM uses the kernel trick to transform data into a higher-dimensional space, where it becomes separable.
   - Common kernel functions:
      - Linear kernel
      - Polynomial kernel
      - Radial Basis Function (RBF) Kernel

4) Soft margin (handling overlapping data)
   - Usually, a perfect separation is not possible. SVM introduces slack variables &\xi_i& to allow misclassified points while penalizing them:
     $y_i(w^T+b) \geq 1 - \xi_i$

     and the new objective function becomes
     $\frac{1}{2}\left | \left | w\right |\right |^2 + C\sum_{i=1}^{n}\xi_i$

     where:

     - Large _C_: less tolerance for misclassified points.
     - Small _C_: allows more misclassified points (better generalization).

5) Make predictions:
   - Once the model is trained, predictions for a new data point _x_ are made using:
     $f(x) = sign(w^T+b)$

     where:
     - if _f(x) > 0_: classify as +1
     - if _f(x) < 0_: classify as -1


![SVM2](https://github.com/user-attachments/assets/dd402566-a24d-431e-9172-74f5fbec3c47)
