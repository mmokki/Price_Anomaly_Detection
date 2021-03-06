# Price Anomaly Detection
This is a personal project.

### Goal
The goal of this project is to detect price anomalies at product level, that is to identify products containing price anomalies in its sales history.


### Analysis
This project explored several classification methods using features extracted from price distribution of each product in each store to flag abnormal products.

Feature Engineering:
- [Standard Deviation](https://en.wikipedia.org/wiki/Standard_deviation)
- [Kurtosis](https://en.wikipedia.org/wiki/Kurtosis)

In the retail industry, having consistent pricing most of the time and having a few different infrequent price points can hint at the distribution being anomalous. 

Kurtosis measures the sharpness and STD measures the spread of the price distribution. Thus, products having price distribution with high Kurtosis and high standard deviation simutaneously are more likely to have anomalies in its sales history. Because high kurtosis indicates there is a frequently used normal price, and high STD indicates there are few infrequent prices lies far away in the tails of the distribution which are highly possible to be price anomalies.

After extracting the two features, four classification methods were utilized:
- Using quantile as threshold for the two features independently
- Kmeans clustering
- Meanshift clustering
- DBSCAN clustering


### Result
According to the result plots, DBSCAN turns out to be the best method in this case. 

I further validated the method using flagged sales dataset to get evaluation metrics like accuracy and precision. However, the validation part can not be publicly shared due to confidential reasons.


### Referrance
[The 5 Clustering Algorithms Data Scientists Need to Know](https://towardsdatascience.com/the-5-clustering-algorithms-data-scientists-need-to-know-a36d136ef68)
