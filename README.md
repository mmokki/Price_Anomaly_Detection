# Price Anomaly Detection
The project used the two features (Standard Deviation and Kurtosis) extracted from price points distribution of each product in each store to detect the products with price anomalies in its sales history.

Since the price rarely changes in retail industry, the assumption is the products having price points distribution with high Kurtosis and high standard deviation simutaneously are more likely have anomalies in its sales history.

Two approaches has been applied:
- Using quantile as threshold
- Clustering: Kmeans, Meanshift and DBSCAN

It turns out DBSCAN is the best methods to apply in this case.
