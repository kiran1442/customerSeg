# Customer Segmentation using RFM Analysis and K-Means Clustering

## 📌 Project Overview

What is Customer Segmentation?
Customer segmentation is the process of dividing customers into groups based on shared characteristics or behaviors. This allows companies to tailor marketing efforts to each segment, leading to improved customer satisfaction, loyalty, and profitability.

This project focuses on segmenting customers using RFM (Recency, Frequency, Monetary) analysis and K-Means Clustering on a transactional dataset to segment customers into cohorts for personalized marketing strategies. It includes data preprocessing, transformation, clustering, and visualization.

---

## 📁 Dataset Description

Attribute	Description:

- InvoiceNo:	Unique invoice number; 'C' prefix indicates cancellations
- StockCode:	Unique product/item code
- Description: Product/item name
- Quantity:	Number of items purchased per transaction
- InvoiceDate:	Date and time of the transaction
- UnitPrice:	Price per unit in GBP
- CustomerID:	Unique identifier for each customer
- Country:	Country of residence of the customer

---

## 📊 Project Workflow

1. Data Loading & Exploration:
- Load dataset from Google Drive (Excel format).
- Inspect data types, missing values, and overall structure.

2. Data Cleaning:
- Drop records with missing CustomerID.
- Remove duplicate rows.
- Exclude negative quantity rows (mostly cancellations).
- Filter out transactions with non-positive unit prices.

3. Data Visualization:
- Analyze top 10 countries by number of transactions.
- Analyze monthly transaction volume.
- Compute and plot MonetaryValue, Frequency, and Recency per customer.

4. Feature Engineering (RFM):
- Recency: Days since last purchase from reference date (Dec 10, 2011).
- Frequency: Number of purchases per customer.
- Monetary: Total spending per customer.

5. Preprocessing:
- Apply logarithmic transformation to remove skewness in data.
- Visualize transformed data distributions.

6. RFM Clustering:
- 3D scatter plot to visualize RFM space.

7. Clustering with K-Means:
- Use Elbow Method and Silhouette Score to determine optimal cluster count.
- Perform K-Means clustering with K=4.
- Assign cluster labels to customers.
- Compute and interpret mean RFM values for each cluster.

---

## Requirements

- Python 3.7+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- plotly (optional for 3D visualization)

---

## Results

- Customers were successfully segmented into 4 distinct groups using K-Means.

- These segments can help the business tailor their marketing strategies to different customer behaviors:

    - High spenders with recent activity

    - Frequent buyers

    - Inactive or churned users

    - Low-frequency, low-monetary customers

---

## 📌 Conclusion
This project demonstrates how RFM analysis combined with K-Means clustering can effectively identify and separate customer segments for targeted marketing. Such segmentation allows companies to better allocate resources, improve customer retention, and increase profitability.

---
