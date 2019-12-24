## K-Nearest Neighbors (KNN) Model

In pattern recognition, the k-nearest neighbors algorithm (k-NN) is a non-parametric method used for classification and regression. In both cases, the input consists of the k closest training examples in the feature space. The output depends on whether k-NN is used for classification or regression:

In k-NN classification, the output is a class membership. An object is classified by a plurality vote of its neighbors, with the object being assigned to the class most common among its k nearest neighbors (k is a positive integer, typically small). If k = 1, then the object is simply assigned to the class of that single nearest neighbor.
In k-NN regression, the output is the property value for the object. This value is the average of the values of k nearest neighbors.
k-NN is a type of instance-based learning, or lazy learning, where the function is only approximated locally and all computation is deferred until classification.

Both for classification and regression, a useful technique can be to assign weights to the contributions of the neighbors, so that the nearer neighbors contribute more to the average than the more distant ones. For example, a common weighting scheme consists in giving each neighbor a weight of 1/d, where d is the distance to the neighbor.

The neighbors are taken from a set of objects for which the class (for k-NN classification) or the object property value (for k-NN regression) is known. This can be thought of as the training set for the algorithm, though no explicit training step is required.

A peculiarity of the k-NN algorithm is that it is sensitive to the local structure of the data.

Case study: An automobile company wants to predict through a campaign whether a person will purchase a new SUV launched at a very reasonable price based on that person's Age and Salary, based on the results, the company will target those who fall under the category of purchasing the SUV. The outcome would be '0' means the person will NOT purchase the SUV, and '1' if that person will purchase the SUV. Use the K-Nearest Neighbors (KNN) model and predict the outcome of the case study. 

Please find the dataset attached!

![alt text](https://github.com/prtk1306/MachineLearning/blob/master/ML%20Logo.PNG "Machine Learning")

Citation: https://www.udemy.com/, https://en.wikipedia.org/