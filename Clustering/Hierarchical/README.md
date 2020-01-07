## Hierarchical Clustering

Hierarchical clustering is another unsupervised learning algorithm that is used to group together the unlabeled data points having similar characteristics. Hierarchical clustering algorithms falls into following two categories.

**Agglomerative hierarchical algorithms** − In agglomerative hierarchical algorithms, each data point is treated as a single cluster and then successively merge or agglomerate (bottom-up approach) the pairs of clusters. The hierarchy of the clusters is represented as a dendrogram or tree structure.

**Divisive hierarchical algorithms** − On the other hand, in divisive hierarchical algorithms, all the data points are treated as one big cluster and the process of clustering involves dividing (Top-down approach) the one big cluster into various small clusters.

**Steps to Perform Agglomerative Hierarchical Clustering**

We are going to explain the most used and important Hierarchical clustering i.e. agglomerative. The steps to perform the same is as follows −

Step 1 − Treat each data point as single cluster. Hence, we will be having, say K clusters at start. The number of data points will also be K at start.

Step 2 − Now, in this step we need to form a big cluster by joining two closet datapoints. This will result in total of K-1 clusters.

Step 3 − Now, to form more clusters we need to join two closet clusters. This will result in total of K-2 clusters.

Step 4 − Now, to form one big cluster repeat the above three steps until K would become 0 i.e. no more data points left to join.

Step 5 − At last, after making one single big cluster, dendrograms will be used to divide into multiple clusters depending upon the problem.

**Role of Dendrograms in Agglomerative Hierarchical Clustering**

As we discussed in the last step, the role of dendrogram starts once the big cluster is formed. Dendrogram will be used to split the clusters into multiple cluster of related data points depending upon our problem.


**Case study:** The marketing team for some Mall wants to predict the type of their customers based on their salary (k$) and spending score (1-100) to target them for their upcoming product launch/sale events to get maximum profit. Use the Hierarchical clustering algorithm and find the optimum clusters using the Dendrogram method.

Please find the dataset attached!

![alt text](https://github.com/prtk1306/MachineLearning/blob/master/ML%20Logo.PNG "Machine Learning")

Citation: https://www.udemy.com/, https://www.tutorialspoint.com/