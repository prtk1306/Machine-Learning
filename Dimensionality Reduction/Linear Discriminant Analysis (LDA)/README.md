## Linear Discriminant Analysis (LDA)

Linear Discriminant Analysis (LDA) is most commonly used as dimensionality reduction technique in the pre-processing step for pattern-classification and machine learning applications. The goal is to project a dataset onto a lower-dimensional space with good class-separability in order avoid overfitting (“curse of dimensionality”) and also reduce computational costs.

The general LDA approach is very similar to a Principal Component Analysis (for more information about the PCA, see the previous article Implementing a Principal Component Analysis (PCA) in Python step by step), but in addition to finding the component axes that maximize the variance of our data (PCA), we are additionally interested in the axes that maximize the separation between multiple classes (LDA).

So, in a nutshell, often the goal of an LDA is to project a feature space (a dataset n-dimensional samples) onto a smaller subspace k (where k≤n−1) while maintaining the class-discriminatory information.
In general, dimensionality reduction does not only help reducing computational costs for a given classification task, but it can also be helpful to avoid overfitting by minimizing the error in parameter estimation (“curse of dimensionality”).

Listed below are the 5 general steps for performing a linear discriminant analysis; we will explore them in more detail in the following sections.

Compute the d-dimensional mean vectors for the different classes from the dataset.
Compute the scatter matrices (in-between-class and within-class scatter matrix).
Compute the eigenvectors and corresponding eigenvalues for the scatter matrices.
Sort the eigenvectors by decreasing eigenvalues and choose k eigenvectors with the largest eigenvalues to form a d×k dimensional matrix W (where every column represents an eigenvector).
Use this d×k eigenvector matrix to transform the samples onto the new subspace. This can be summarized by the matrix multiplication: Y=X×W (where X is a n×d-dimensional matrix representing the n samples, and y are the transformed n×k-dimensional samples in the new subspace).

**Case study:** To analyze Wine dataset and fetch the best 2 independent/predictor variables which are highly correlated with the dependent variable and classify the 3 types of Wine, so to recommend the same to the Wine lovers. Use Linear Discriminant Analysis model to solve this case study and finally calculate the accuracy of the model. 

Please find the dataset attached!

![alt text](https://github.com/prtk1306/MachineLearning/blob/master/ML%20Logo.PNG "Machine Learning")

Citation: https://www.udemy.com/, https://sebastianraschka.com/