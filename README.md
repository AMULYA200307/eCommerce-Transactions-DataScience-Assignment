# Data Science Assignment: eCommerce Transactions Dataset

## Overview

This project focuses on analyzing and deriving insights from an eCommerce Transactions dataset consisting of three files: `Customers.csv`, `Products.csv`, and `Transactions.csv`. The primary objectives are to perform exploratory data analysis (EDA), build predictive models, and derive actionable business insights. The project involves the following key tasks:

- **Task 1**: Exploratory Data Analysis (EDA) and Business Insights
- **Task 2**: Lookalike Model
- **Task 3**: Customer Segmentation / Clustering

## Files Description

1. **Customers.csv**:
    - **CustomerID**: Unique identifier for each customer.
    - **CustomerName**: Name of the customer.
    - **Region**: Continent where the customer resides.
    - **SignupDate**: Date when the customer signed up.

2. **Products.csv**:
    - **ProductID**: Unique identifier for each product.
    - **ProductName**: Name of the product.
    - **Category**: Product category.
    - **Price**: Product price in USD.

3. **Transactions.csv**:
    - **TransactionID**: Unique identifier for each transaction.
    - **CustomerID**: ID of the customer who made the transaction.
    - **ProductID**: ID of the product sold.
    - **TransactionDate**: Date of the transaction.
    - **Quantity**: Quantity of the product purchased.
    - **TotalValue**: Total value of the transaction.
    - **Price**: Price of the product sold.

## Assignment Tasks and Deliverables

### Task 1: Exploratory Data Analysis (EDA) and Business Insights
- **Objective**: Perform exploratory data analysis on the provided dataset and derive at least 5 business insights.
- **Deliverables**:
    - A Jupyter Notebook/Python script containing the EDA code.
    - A PDF report with the business insights (maximum 500 words).
    - Insights include trends in customer behavior, popular products, etc.

### Task 2: Lookalike Model
- **Objective**: Build a Lookalike Model that recommends 3 similar customers based on their profile and transaction history.
- **Deliverables**:
    - A `Lookalike.csv` file containing the map: `Map<cust_id, List<cust_id, score>`.
    - A Jupyter Notebook/Python script explaining model development.
    - Evaluation based on model accuracy, logic, and the quality of recommendations and similarity scores.

### Task 3: Customer Segmentation / Clustering
- **Objective**: Perform customer segmentation using clustering techniques and visualize the clusters.
- **Deliverables**:
    - A report on the clustering results, including the number of clusters formed and clustering metrics (DB Index).
    - A Jupyter Notebook/Python script containing clustering code.
    - Evaluation based on clustering logic, metrics, and visual representation of clusters.

## Clustering Methods Used

We used the following clustering algorithms to segment customers:
- **K-Means Clustering**: A centroid-based clustering algorithm.
- **Agglomerative Clustering**: A hierarchical clustering method.
- **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**: A density-based clustering algorithm.

### Performance Metrics:
- **DB Index**: A metric used to evaluate the quality of clusters based on their cohesion and separation.
- **Silhouette Score**: A measure of how similar an object is to its own cluster compared to other clusters.

## Experiment Results

We experimented with different numbers of clusters (2 to 10) for K-Means and Agglomerative Clustering. DBSCAN was evaluated with varying values of `eps` and `min_samples`.

### K-Means Clustering

| Number of Clusters | DB Index | Silhouette Score |
|--------------------|----------|------------------|
| 2                  | 1.3356   | 0.2884           |
| 3                  | 1.2480   | 0.2809           |
| 4                  | 1.1660   | 0.3253           |
| 5                  | 1.0226   | 0.3696           |
| 6                  | 1.0260   | 0.3587           |
| 7                  | 1.0114   | 0.3493           |
| 8                  | 0.9399   | 0.3795           |
| 9                  | 0.8987   | 0.3931           |
| 10                 | 0.9146   | 0.3900           |

### Agglomerative Clustering

| Number of Clusters | DB Index | Silhouette Score |
|--------------------|----------|------------------|
| 2                  | 1.3948   | 0.2780           |
| 3                  | 1.2374   | 0.3004           |
| 4                  | 1.0140   | 0.3363           |
| 5                  | 1.0566   | 0.3648           |
| 6                  | 0.9620   | 0.3630           |
| 7                  | 0.9300   | 0.3646           |
| 8                  | 0.9470   | 0.3720           |
| 9                  | 0.9296   | 0.3773           |
| 10                 | 0.8902   | 0.3820           |

### DBSCAN Clustering

| eps | min_samples | DB Index | Silhouette Score |
|-----|-------------|----------|------------------|
| 0.3 | 5           | 1.4679   | -0.1844          |
| 0.5 | 5           | 1.4718   | -0.2100          |
| 0.7 | 5           | 1.5393   | 0.1658           |
| 0.7 | 10          | 1.5992   | -0.0638          |

## Installation and Setup

1. Clone this repository to your local machine:

   ```
   git clone [https://github.com/AMULYA200307/eCommerce-Transactions-DataScience-Assignment]
   ```

2. Install the necessary libraries:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the Jupyter Notebooks and execute the cells to perform the analysis and clustering.

## File Structure

```
eCommerce-Transactions-Analysis/
├── Amulya_Gangula_EDA.ipynb
├── Amulya_Gangula_EDA.pdf
├── Amulya_Gangula_Lookalike.ipynb
├── Amulya_Gangula_Lookalike.csv
├── Amulya_Gangula_Clustering.ipynb
├── Amulya_Gangula_Clustering.pdf
└── requirements.txt
```

## Conclusion

This project presents a comprehensive analysis of an eCommerce Transactions dataset. It covers:
- Exploratory Data Analysis (EDA) and actionable business insights.
- Development of a Lookalike Model for customer recommendation based on transaction history.
- Customer segmentation using various clustering algorithms.

The results provide valuable insights that can be used for targeted marketing strategies and customer profiling.
