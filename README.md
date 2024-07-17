# Customer Segmentation using K-means Clustering

## Overview

This project aims to segment customers based on their annual income and spending score using the K-means clustering algorithm. The analysis provides insights into different customer groups, which can help tailor marketing strategies effectively.

## Data Description

The dataset used for this analysis is `Mall_Customers.csv`, which contains the following columns:

- **CustomerID**: Unique identifier for each customer
- **Gender**: Gender of the customer
- **Age**: Age of the customer
- **Annual Income (k$)**: Annual income of the customer in thousand dollars
- **Spending Score (1-100)**: Score assigned by the mall based on customer behavior and spending nature

## Data Preprocessing

1. **Data Loading**: The dataset was loaded using pandas.
2. **Data Inspection**: The first few and last few rows of the dataset were displayed to understand its structure. The dataset has 200 entries and 5 columns with no missing values.
3. **Data Encoding**: The categorical column 'Gender' was converted into numerical values using Label Encoding.

## Exploratory Data Analysis

Various plots were generated to understand the distribution and relationship of the data:
- **Age Distribution**: Histogram showing the distribution of customer ages.
- **Annual Income Distribution**: Histogram displaying the distribution of annual income.
- **Spending Score Distribution**: Histogram showing the distribution of spending scores.
- **Age vs Annual Income**: Scatter plot to observe the relationship between age and annual income.
- **Annual Income vs Spending Score**: Scatter plot to see the relationship between annual income and spending score.
- **Annual Income by Gender**: Box plot to compare annual income across genders.
- **Spending Score by Gender**: Box plot to compare spending scores across genders.

## Clustering

### Feature Selection and Standardization

Features selected for clustering were 'Annual Income (k$)' and 'Spending Score (1-100)'. The data was standardized using StandardScaler to ensure that each feature contributes equally to the distance calculations.

### Optimal Number of Clusters

The Elbow Method was used to determine the optimal number of clusters by plotting the Within-Cluster Sum of Squares (WCSS) for different numbers of clusters.

### Applying K-means

K-means clustering was applied with the optimal number of clusters (5 clusters). The resulting clusters were added to the dataset for further analysis.

### Visualization

The clusters were visualized using a scatter plot, with different colors representing different clusters. This helped in understanding the customer segments better.

## Clustering Evaluation Metrics

Several evaluation metrics were used to assess the quality of the clustering:
- **Inertia (WCSS)**: Measures how tightly the clusters are formed. Lower values indicate more tightly clustered data points.
- **Silhouette Score**: Measures how similar an object is to its own cluster compared to other clusters. It ranges from -1 to 1, where a higher value indicates better-defined clusters.

### Results

- **Inertia (WCSS)**: 65.56840815571681
- **Silhouette Score**: 0.5546571631111091

## Conclusion

The K-means clustering algorithm effectively categorized customers into distinct groups based on their annual income and spending score. The evaluation metrics confirmed the robustness and reliability of the clustering. This analysis provides valuable insights into customer segments, enabling more targeted and effective marketing strategies.
