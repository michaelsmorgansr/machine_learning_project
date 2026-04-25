# 🧠 Customer Segmentation with K‑Means Clustering

Welcome to my data science project using a **Mall Customers** dataset.  
In this project, I apply **unsupervised machine learning** to segment customers based on **income and spending behavior**, then interpret the resulting clusters using demographic information.

---

## 📌 Project Overview

This project walks through a complete **unsupervised learning workflow**:

- Data loading and inspection
- Data cleaning and preprocessing
- Feature scaling using Z‑score normalization
- Determining optimal number of clusters using the **Elbow Method**
- Customer segmentation using **K‑Means clustering**
- Visualizing customer groups
- Interpreting and naming clusters
- Demographic analysis by cluster (age and gender)

**Goal:**  
Identify meaningful customer segments that can inform business and marketing strategy.

---

## 🛠️ Skills Demonstrated

- Data cleaning and preprocessing with **Pandas**
- Numerical computing with **NumPy**
- Feature scaling with **scikit‑learn**
- Unsupervised learning (K‑Means clustering)
- Model selection using the **Elbow Method**
- Data visualization with **Matplotlib**
- Cluster interpretation and labeling
- Demographic aggregation and analysis
- Reproducible, GitHub‑ready project structure

---

## 📂 Dataset

The dataset used in this project is a mall customer dataset containing demographic and behavioral information.

**Input file:**  
`mallcustomers.csv`

Each row represents a single customer.

### Key Features Include:
- **CustomerID** – Unique customer identifier (removed before modeling)
- **Gender** – Male / Female
- **Age** – Customer age
- **Income** – Annual income (provided as strings with commas and “USD”)
- **SpendingScore** – Spending score (1–100)

> Income values are cleaned and converted to numeric format before analysis.

---

## 🔍 How the Model Works

### 1. Preprocessing
- Removed formatting from income values (commas and “USD”)
- Converted income to integer values
- Dropped `CustomerID` since it does not provide clustering value
- Standardized `Income` and `SpendingScore` using **StandardScaler**

---

### 2. Choosing the Number of Clusters
- K‑Means models were trained for `k = 1` through `k = 10`
- The **Elbow Method** was used to evaluate within‑cluster sum of squares
- The elbow point indicated **k = 6** as an appropriate choice

---

### 3. Final Clustering
- K‑Means clustering applied with `k = 6`
- Cluster assignments added back to the original dataset
- Customer groups visualized using **Income vs Spending Score**

---

### 4. Cluster Interpretation
- Cluster centers transformed back to original units
- Clusters labeled based on relative income and spending levels:
  - Low / Mid / High Income
  - Low / Mid / High Spending

Example cluster labels:
- **Low Income / Low Spend (Low Engagement)**
- **Low Income / High Spend (Enthusiastic Budget Shoppers)**
- **High Income / Low Spend (Value‑Conscious Customers)**
- **High Income / High Spend (Premium Customers)**

---

### 5. Demographic Analysis
For each cluster, the following metrics are calculated:
- Customer count
- Mean age
- Male and female counts
- Gender percentage distribution

This step translates abstract clusters into understandable customer profiles.

---

## ▶️ How to Run the Project

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/customer-segmentation.git
cd customer-segmentation
