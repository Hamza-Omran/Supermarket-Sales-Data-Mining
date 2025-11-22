# Supermarket Sales Data Mining and Analytics Project

## Team Members

* Hamza Hussain Omran
* Ahmed Khalifa Abdulraouf
* Moaz Moustafa Abd-Elhamid
* Abdurhman Hesham Ragab
* Kareem Mohamed Samy Aboshady

## Overview

This project performs end-to-end data mining and analytics on supermarket sales data. The workflow includes data preprocessing, exploratory analysis, outlier treatment, correlation study, feature engineering, and clustering techniques to understand customer behavior and sales patterns.

## Dataset Summary

The dataset contains transaction-level records with fields such as invoice ID, branch, city, customer type, gender, product line, unit price, quantity, tax, total, COGS, gross income, payment type, rating, and timestamps.

Key characteristics:

* No missing or duplicate values
* Normal and heavy-tailed distributions across financial variables
* Date and Time merged into a single DateTime column

## Data Preprocessing

* Converted date and time into a unified datetime feature
* Added Hour and Month features for temporal analysis
* Outliers detected using IQR and replaced with median values
* Verified outlier treatment using boxplots

## Exploratory Data Analysis (Summary)

### Correlation

* Strong correlations among Total, COGS, Gross Income, and Tax
* Weak or negligible correlation with Rating and Quantity

### Product Line Insights

* Highest transaction count: Fashion Accessories
* Highest total gross income: Food and Beverages
* Ratings stable across product lines

### Geographic Analysis

* Gross income evenly distributed across branches (A, B, C)
* Each branch shows different peak hours

### Payment and Gender Insights

* E-wallet, Cash, and Credit Card used in similar proportions
* Females spend more in most product lines
* Males spend more in Health and Beauty

### Temporal Patterns

* Peak sales: 18:00–19:00
* Lowest sales: 15:00–18:00
* Specific product lines show hour-specific demand patterns

### Quantity and Distribution

* Product lines show balanced contribution to quantity sold
* Members frequently buy in quantities of 1, 4, or 10

## Clustering Analysis

### K-Medoids

* Applied on Unit Price and Rating
* Optimal clusters: 3
* Identified three pricing segments (low, mid, high)

### Hierarchical Clustering

* Applied on Quantity and Total
* Four clusters identified
* Clear separation based on total spending and purchase quantity

## Key Insights

1. Food and Beverages leads total revenue; Fashion Accessories leads frequency.
2. Branch revenue split is almost equal across all cities.
3. Female customers contribute higher spending overall.
4. Peak shopping occurs in the evening across branches.
5. Price sensitivity segmentation reveals three clear customer groups.
6. Clustering identifies four purchasing behavior segments useful for targeted marketing.

## Recommendations

* Increase stock for high-demand product lines.
* Adjust staffing and promotions for evening peak hours.
* Target pricing and marketing based on identified clusters.
* Maintain all payment methods due to balanced usage.
* Develop city-specific operational strategies based on temporal behavior.

## Tools and Techniques

* Python (pandas, numpy, matplotlib, seaborn)
* Scikit-learn (StandardScaler, clustering algorithms)
* sklearn_extra for K-Medoids
* SciPy hierarchical clustering

## Conclusion

The project provides a complete analytical workflow for supermarket sales, revealing actionable patterns in customer behavior, product performance, spending trends, and temporal demand. The combination of EDA and clustering offers a structured foundation for data-driven retail decision-making.
