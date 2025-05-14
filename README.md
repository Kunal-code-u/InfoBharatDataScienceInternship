# 🛒 Online Retail Customer Segmentation & Behavior Analysis

## 📌 Project Overview

This project was completed as part of my internship task to analyze real-world customer transaction data. The dataset is sourced from an online retail store and contains transactional and customer-related information. The main goal was to extract business insights, segment customers, estimate customer lifetime value (CLV), and optionally predict future purchase behavior.

---

## 📁 Dataset

- **Source**: [UCI Machine Learning Repository - Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)
- **Size**: ~500K transactions
- **Columns**: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

---

## 📊 Task Breakdown

### 1. 🔧 Data Cleaning
- Removed missing CustomerIDs and duplicates
- Filtered invalid rows (Quantity ≤ 0, Price ≤ 0)
- Converted `InvoiceDate` to datetime and extracted month, day, year, hour

### 2. 🔄 Data Transformation
- Added new features: `TotalPrice`, `InvoiceMonth`, `Weekday`, `Hour`
- Aggregated customer-level data for analysis

### 3. 📈 Exploratory Data Analysis (EDA)
- Summary statistics of customer behavior
- Most popular products by frequency & revenue
- Monthly sales trends and peak sales hours
- Pie chart of country-wise customers (if applicable)
- Correlation matrix for numeric fields

### 4. 🧠 Customer Segmentation (K-Means)
- Applied RFM (Recency, Frequency, Monetary) analysis
- Performed K-Means clustering to identify 4 distinct customer groups
- Identified top-value and at-risk customer segments

### 5. 📦 Customer Lifetime Value (CLV)
- Estimated CLV using simple RFM metrics
- Labeled customers with RFM scores (e.g., 444 = best)
- Recommended retention and reactivation strategies

### 6. 🔮 Predictive Modeling (Optional)
- Built binary classification models to predict likelihood of a repeat purchase
- Used Logistic Regression, Random Forest, and XGBoost
- Random Forest performed best based on F1-score

---

## 🖼️ Visualizations

- Histograms of customer spending
- Bar charts for most popular products
- Line plots showing sales trends over time
- Pie charts for customer geography
- Scatter plots for customer clusters
- Confusion matrix for model performance

---

## 📌 Key Business Insights

- **Top Products**: Small decorative items like "WHITE HANGING HEART T-LIGHT HOLDER" and gift items.
- **Best Customers**: Cluster 0 (loyal and high-spending).
- **Sales Peak**: November and early December (holiday season).
- **Retention Tip**: Use RFM to identify customers at risk and personalize offers.

---

## 🧰 Tech Stack

- **Python**
- **Jupyter Notebook**
- **Pandas, NumPy**
- **Matplotlib, Seaborn**
- **Scikit-learn**
- **XGBoost (optional)**

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/your-username/online-retail-analysis.git

# 2. Navigate into the folder
cd online-retail-analysis

# 3. Open Jupyter Notebook and run the `.ipynb` file
jupyter notebook
