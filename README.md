# Stock-Market-Clustering-with-K-Means

#Overview
This project extends the concept of customer segmentation to stock market clustering using the K-Means clustering algorithm. By analyzing stock data based on two important factors, variance and returns, we apply unsupervised learning techniques to identify distinct groups of stocks that share similar behaviors. This project aims to explore how clustering can be leveraged for stock market analysis and how different clustering techniques can help in making informed financial decisions.

#Objective
Stock Market Clustering: Use K-Means clustering to segment stocks based on their volatility (variance) and performance (returns).
Optimizing Clusters: Use the Elbow Method to determine the optimal number of clusters.
Visualizing Data: Visualize the clustering results and explore how variance and returns contribute to forming clusters.
#Key Components
Stock Data: We fetch historical stock data using Yahoo Finance API (via yfinance) for a set of major companies.
K-Means Clustering: We perform K-Means clustering to group stocks based on their variance and returns.
Elbow Method: The optimal number of clusters is determined using the Elbow Method, which helps find the number of clusters that minimizes inertia.
Clustering Results Visualization: We use matplotlib and seaborn to visualize the clusters and their behavior.
Approach
Data Collection: Historical stock prices for 24 companies are collected using yfinance. Data is fetched from Yahoo Finance, with the default interval set to '1-minute' to capture detailed trends.
Data Preprocessing:
Cleaning: Stock data is cleaned and merged into a single DataFrame for easier analysis.
Return Calculation: Daily returns are calculated, and annualized mean returns and variances are derived for each stock.
Standardization: The data (variance and returns) is standardized using the StandardScaler to bring both features to the same scale.
Clustering:
K-Means Algorithm is applied to the standardized data to find natural clusters of stocks.
Elbow Method is used to identify the optimal number of clusters based on inertia (within-cluster sum of squares).
Visualization:
2D Scatter Plot: The clusters are visualized in a 2D scatter plot showing variance on the x-axis and returns on the y-axis.
Elbow Curve: The Elbow Curve is plotted to visualize the optimal number of clusters based on inertia.
Technologies Used
Python: The core programming language for data analysis.

#Libraries:
yfinance: To fetch stock data.
pandas: For data manipulation.
numpy: For numerical operations.
scikit-learn: For clustering and scaling the data.
matplotlib & seaborn: For visualization.

#Requirements
To run this project, you'll need the following Python libraries:

pandas
numpy
matplotlib
seaborn
scikit-learn
yfinance

A scatter plot visualizing the clusters of stocks.
An elbow curve indicating the optimal number of clusters.
Stocks grouped into clusters based on similar returns and variance, which helps in understanding the similarities among stock behaviors.
Challenges and Insights
Variance vs Returns: Determining how variance (volatility) and returns affect the clustering was critical. Stocks with high returns and low variance tend to form one type of cluster, while others with high volatility and lower returns group differently.
Optimal Clusters: Identifying the optimal number of clusters with the Elbow Method was essential for better analysis. Too few clusters failed to capture all distinct behaviors, and too many resulted in overfitting.
Future Improvements
Feature Expansion: Additional features like historical price trends, market capital, or economic factors could be incorporated for more detailed clustering.
Advanced Clustering: Exploring other clustering methods such as DBSCAN or Hierarchical Clustering could provide deeper insights into stock market segmentation.
Time Series Analysis: Incorporating time series data and performing clustering on a temporal basis could provide more dynamic stock groupings.

Contributions
If you'd like to contribute to this project, feel free to fork the repository and submit a pull request with your improvements!
