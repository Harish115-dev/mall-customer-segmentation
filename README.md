# Mall Customer Segmentation using K-Means Clustering

A machine learning project that segments mall customers into distinct groups based on their annual income and spending behavior, using unsupervised K-Means clustering.

## Overview

This project analyzes customer data to identify meaningful segments that can guide targeted marketing strategies. By clustering customers based on **Annual Income** and **Spending Score**, the model reveals five distinct customer profiles, ranging from high-value frequent spenders to budget-conscious shoppers.

## Dataset

The dataset (`Mall_Customers.csv`) contains 200 customer records with the following fields:

| Column | Description |
|--------|-------------|
| CustomerID | Unique identifier |
| Gender | Customer gender |
| Age | Customer age |
| Annual Income (k$) | Yearly income in thousands of dollars |
| Spending Score (1-100) | Score assigned based on customer spending behavior |

## Project Workflow

1. **Data Exploration** — checked for missing values, examined distributions of Age, Income, and Spending Score
2. **Feature Scaling** — standardized features using `StandardScaler` for fair distance-based clustering
3. **Optimal Cluster Selection** — used the Elbow Method (WCSS) to determine the ideal number of clusters
4. **K-Means Clustering** — segmented customers into 5 groups using Annual Income and Spending Score
5. **Visualization** — plotted clusters with centroids to interpret each segment
6. **Business Insights** — translated clusters into actionable customer segments

## Key Findings

Five customer segments were identified:

- **High Income, High Spending** — premium target customers, ideal for loyalty programs
- **High Income, Low Spending** — untapped potential, candidates for re-engagement campaigns
- **Low Income, High Spending** — value-driven shoppers, respond well to discounts and bundles
- **Low Income, Low Spending** — lower marketing priority
- **Average Income, Average Spending** — the largest, general-purpose segment

## Tech Stack

- Python
- pandas, numpy — data handling
- matplotlib — visualization
- scikit-learn — `StandardScaler`, `KMeans`, `silhouette_score`

## How to Run

```bash
git clone https://github.com/Harish115-dev/mall-customer-segmentation.git
cd mall-customer-segmentation
jupyter notebook customer_segmentation.ipynb
```

## Requirements
```
pandas
numpy
matplotlib
scikit-learn
```

## Project Structure

```
.
├── Mall_Customers.csv          # Dataset
├── customer_segmentation.ipynb # Main analysis notebook
├── README.md
└── requirements.txt
```

## Future Improvements

- Experiment with other clustering algorithms (DBSCAN, Hierarchical Clustering) for comparison
- Incorporate additional features (e.g., purchase frequency, product categories) if available
- Deploy as an interactive dashboard for business stakeholders to explore segments
