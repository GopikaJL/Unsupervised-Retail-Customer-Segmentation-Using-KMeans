# Unsupervised-Retail-Customer-Segmentation-Using-KMeans
# KMeans-Based Customer Segmentation for Online Retail

## Project Overview

This project aims to segment customers of a UK-based non-store online retail company using unsupervised learning techniques. The company, which sells unique all-occasion gifts primarily to wholesalers, has provided a transactional dataset containing all transactions between 01/12/2010 and 09/12/2011. The objective is to categorize customers to devise targeted marketing strategies.

## Dataset

The dataset used in this project contains the following attributes:
- **InvoiceNo**: Invoice number. A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation.
- **StockCode**: Product (item) code. A 5-digit integral number uniquely assigned to each distinct product.
- **Description**: Product (item) name.
- **Quantity**: The quantities of each product (item) per transaction.
- **InvoiceDate**: Invoice date and time in the format yyyy-mm-dd hh:mm:ss.
- **UnitPrice**: Unit price of the product in GBP (Great Britain Pound).
- **CustomerID**: Customer number. A 5-digit integral number uniquely assigned to each customer.
- **Country**: The name of the country where each customer resides.

Dataset Credits: [UCI Machine Learning Repository - Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)

Citation: Dr. Daqing Chen, Director: Public Analytics group. chend '@' lsbu.ac.uk, School of Engineering, London South Bank University, London SE1 0AA, UK.

## Methodology

The project utilizes the following methodologies and techniques:

### Data Preprocessing

1. **Removing Cancelled Orders**: Transactions with InvoiceNo starting with 'c' were removed to ensure data integrity.
2. **Handling Missing Values**: Any missing CustomerID entries were discarded as they are crucial for customer segmentation.

### RFM Analysis

RFM (Recency, Frequency, Monetary) analysis is used to understand customer behavior:
- **Recency**: How recently a customer made a purchase.
- **Frequency**: How often a customer makes a purchase.
- **Monetary**: How much money a customer has spent.

### K-Means Clustering

K-Means Clustering, an unsupervised learning algorithm, is used to segment customers based on the RFM values:
1. **Determining Optimal Number of Clusters**: The Elbow Method is used to identify the optimal number of clusters.
2. **Clustering Customers**: Customers are grouped into clusters representing different segments (e.g., high-value, mid-value, low-value customers).

### Data Visualization

Visualizations are created to analyze the distribution of customers within each segment and understand their characteristics.

## Installation

To run this project, you need to have Python installed along with the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn

git clone https://github.com/yourusername/CustomerSegmentation.git
cd CustomerSegmentation
jupyter notebook CustomerSegmentation.ipynb

