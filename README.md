# Customer Segmentation Analysis

## Overview

This project focuses on customer segmentation using unsupervised machine learning techniques such as KMeans and hierarchical clustering. The goal is to identify distinct groups of customers based on their behavior and characteristics, enabling more targeted marketing strategies and better customer understanding.

## Dataset

The dataset consists of customer behavior data including:

- Minutes watched: The amount of time a customer spends engaging with content.
- Customer Lifetime Value (CLV): A prediction of the net profit attributed to the entire future relationship with a customer.
- Region: The geographical area the customer belongs to.
- Channel: The medium through which the customer was acquired, such as social media platforms or referrals.

### Data Preprocessing

Data preprocessing was performed to ensure that the dataset was clean and suitable for analysis:

1. Missing Values: Missing values were filled with zeroes to maintain the integrity of the dataset.
2. Dummy Variables: Categorical variables, such as region and acquisition channel, were converted into dummy variables for analysis.
3. Standardization: To bring all features to the same scale, standardization was performed using StandardScaler. This ensures that features with larger scales do not dominate the clustering algorithm.

## Exploratory Data Analysis (EDA)

### Correlation Analysis

A correlation heatmap was generated to examine the relationships between variables. This step helps in understanding how features interact with each other, particularly identifying strong correlations or potential multicollinearity.

### Scatter Plot

A scatter plot of Minutes Watched against CLV was used to visualize the raw data. This provides an initial understanding of how customers differ in these two critical dimensions.

## Clustering Techniques

### Hierarchical Clustering

Hierarchical clustering was applied using the Ward method, which minimizes the variance within each cluster. The dendrogram produced helped to visualize the hierarchical structure and determine a suitable number of clusters.

### KMeans Clustering

KMeans clustering was chosen due to its simplicity and effectiveness. To determine the optimal number of clusters, the Elbow Method was used. This method involves plotting the Within-Cluster Sum of Squares (WCSS) for various cluster counts and selecting the point where adding more clusters provides diminishing returns.

The final model was built with 8 clusters, providing distinct customer segments.

## Results

Each cluster was profiled based on the mean values of the features. The key segments identified include:

- Instagram Explorers: Customers primarily engaged through Instagram.
- LinkedIn Networkers: Customers who are active on LinkedIn and tend to have high engagement.
- Friends' Influence: Customers who were referred by friends.
- Google-YouTube Mix: Customers engaged through a combination of Google and YouTube.
- Anglo-Saxon Multi-Channel: Customers from Anglo-Saxon regions using multiple acquisition channels.
- European Multi-Channel: European customers with multi-channel engagement.
- Twitter Devotees: Highly engaged customers from Twitter.
- Facebook Followers: Customers primarily acquired through Facebook.

### Segment Analysis

For each segment, key characteristics such as Customer Lifetime Value, Minutes Watched, and Region were analyzed. Additionally, the proportion of total customers in each segment was calculated to understand their relative importance.

## Visualization

Several plots were created to visualize the segmentation:

- Correlation Heatmap: Displayed the correlation between all features.
- Scatter Plot: Showed the distribution of customers based on Minutes Watched and CLV.
- Elbow Method: Visualized the optimal number of clusters for KMeans.
- Dendrogram: Presented the hierarchical structure of the clustering.
- KMeans Scatter Plot: Colored the customers based on their cluster assignment, providing a visual interpretation of the segmentation.

## Conclusion
This project successfully segments customers into meaningful groups based on their behavior and engagement with the platform. These insights can be leveraged for targeted marketing and improving customer satisfaction. By understanding the unique characteristics of each segment, businesses can tailor their strategies to maximize customer retention and profitability.

## Future Work

- Further Feature Engineering: Additional features such as customer demographics could provide even deeper insights.
- Advanced Clustering Techniques: Exploring other clustering methods like DBSCAN or Gaussian Mixture Models for comparison.
- Predictive Modeling: Use these clusters as a target variable for predictive modeling in customer retention or conversion prediction.

## Tools and Technologies

- Python: Used for data processing, analysis, and modeling.
- Pandas: For handling the dataset and performing data manipulation.
- Scikit-learn: For clustering algorithms and scaling.
- Matplotlib/Seaborn: For visualizing the data and results.
- Scipy: For hierarchical clustering.

This project highlights the power of customer segmentation in understanding and addressing customer needs, which is critical for any data-driven business strategy.
