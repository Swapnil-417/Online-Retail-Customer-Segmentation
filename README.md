# Online-Retail-Customer-Segmentation
In this project, our task is to identify major customer segments on a transactional data set which contains all the transactions for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

## Why Segment Customers?
Customer Segmentation is the process of dividing customers into homogeneous and distinct groups. It helps a company to develop an effective strategy for targeting its customers. This has a direct impact on the entire product development cycle, the budget management practices, and the plan for delivering targeted promotional content to customers. 

Customer segmentation can also help a company to understand how its customers are alike, what is important to them, and what is not.

## Steps Involved

Initially, we explored and cleaned the data. Then carried out Exploratory Data analysis to get some insights from the dataset. During this analysis we performed preprocessing, filtering, processing for clustering that can be checked in the below notebook in detail.


## RFM Analysis

RFM stands for Recency, Frequency, and Monetary. RFM analysis is a marketing technique in analyzing customer behavior such as how recently a customer has purchased, how often the customer purchases, and how much the customer spends. The advantage is that the customers’ behavior can be captured by using a relatively small number of features. The RFM variables are appropriate for capturing the specifics of the customer's purchase behavior.

After getting the RFM values, creating quartiles on each of the metrics and assigned the required order. Divided each metric into 4 cuts. For example, the recency metric, the highest value, 4, is assigned to the customers with the least recency value (since they are the most recent customers). For the frequency and monetary metric, the highest value, 4, is assigned to the customers with the top 25% frequency and monetary values, respectively.

## RFM based Clustering models

First we used K-means clustering and built multiple clusters to find the optimal number of clusters using elbow method and silhouette method. From both methods we got k=2 as the optimal number of clusters. 

Next, We used an Agglomerative Hierarchical Clustering algorithm but before that drew the dendrogram to help us decide the number of clusters. We got 2 clusters from dendrogram and then applied hierarchical clustering on our RFM data using clusters k=2. 

Next, we built DBSCAN clustering without any parameter optimization. Later we used K-nearest neighbors to tune the hyperparameter and again ran the DBSCAN model. Here we got 3 clusters, 0 and 1 are the two different clusters, and -1 is the noise.

## Conclusion

We have performed RFM analysis on the online retail dataset and then used Recency, Frequency and Monetary values to form clusters using K-means clustering, Hierarchical clustering and DBSCAN algorithms. K-means clustering and Hierarchical clustering segmented the customers very well using 2 clusters. We got two customer segments that were to be formed on this online retail dataset as a wholesale customer segment and average customer segment.


