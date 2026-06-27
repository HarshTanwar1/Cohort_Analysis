<div align="center">

# 📊 Customer Cohort & Segmentation Analysis

Turning raw e-commerce transactions into actionable customer-retention strategy

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)

</div>

<br>

## 🎯 Overview

An end-to-end data analytics project that transforms **~500K raw e-commerce transactions** into a clear picture of _who the most valuable customers are_ and _how well the business retains them over time_.

Using **Cohort Analysis**, **RFM Analysis**, and **K-Means Clustering**, the project answers three business-critical questions:

> 🔹 **How well do we retain customers month over month?**<br>
> 🔹 **Which customers are the most valuable to us right now?**<br>
> 🔹 **Can we automatically group customers into actionable segments?**

<br>

## 🚀 Key Highlights

- ✅ Built a **monthly retention matrix** that reveals how customer engagement decays over a customer's lifetime.
- ✅ Ranked customers into **RFM segments** to distinguish loyal, high-value buyers from at-risk and lapsed ones.
- ✅ Used **unsupervised ML** to automatically segment the customer base into **3 distinct groups**, enabling targeted marketing strategies.
- ✅ Produced insights the business can act on — _which customers to focus on, and what offers will foster loyalty._

<br>

## 🛠️ Tech Stack

| Layer                | Technologies        |
| -------------------- | ------------------- |
| **Language**         | Python 3            |
| **Environment**      | Jupyter Notebook    |
| **Data Wrangling**   | pandas, NumPy       |
| **Visualization**    | Matplotlib, Seaborn |
| **Machine Learning** | scikit-learn        |

<br>

## 🔍 Features & Methodology

The notebook walks through a complete analytics pipeline, from raw data to business insight:

### 1️⃣ Data Cleaning

Removes missing values, duplicate records, and invalid transactions (negative quantities, zero prices) to ensure reliable downstream analysis.

### 2️⃣ Descriptive Statistics

Summary statistics, variance, and standard deviation analysis to understand how `Quantity`, `UnitPrice`, and `CustomerID` are distributed.

### 3️⃣ Cohort Analysis

Groups customers into monthly cohorts by their **first purchase month**, computes a **cohort index** (months since first purchase), and visualizes **month-over-month retention rates** in a heatmap.

### 4️⃣ RFM Analysis

Scores every customer on **Recency**, **Frequency**, and **Monetary** value, then bins them into quartiles to surface the best (`444`) and worst (`111`) customer segments.

### 5️⃣ K-Means Clustering

Log-transforms and normalizes the RFM data, uses the **Elbow Method** to find the optimal number of clusters (**K = 3**), and segments customers — visualizing the relative importance of each RFM attribute per cluster.

<br>

## 📂 Dataset

| Attribute     | Description                                                                |
| ------------- | -------------------------------------------------------------------------- |
| `InvoiceNo`   | Unique 6-digit transaction number (a leading `c` indicates a cancellation) |
| `StockCode`   | Unique 5-digit product code                                                |
| `Description` | Product name                                                               |
| `Quantity`    | Quantity of each product per transaction                                   |
| `InvoiceDate` | Date and time the transaction was generated                                |
| `UnitPrice`   | Product price per unit (in sterling)                                       |
| `CustomerID`  | Unique 5-digit customer number                                             |
| `Country`     | Country where the customer resides                                         |

<br>

## ⚙️ Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/HarshTanwar1/Cohort_Analysis.git
cd Cohort_Analysis

# 2. (Recommended) Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# 4. Launch the notebook
jupyter notebook Cohort_Analysis.ipynb
```

<br>

## 📚 What I Learned

- **Cohort analysis** as a technique for measuring retention over time, and constructing cohort/retention matrices with pandas `groupby`, `transform`, and `pivot`.
- **RFM segmentation** — quantifying customer value across recency, frequency, and monetary dimensions using `pd.qcut`.
- **Unsupervised ML** with K-Means — including _why_ skewed data must be log-transformed and standardized before clustering, and how to choose K with the elbow method.
- **Data cleaning discipline** as the foundation of trustworthy analysis.
- **Data storytelling** — translating statistical output into business-relevant decisions.

<br>

## 🔮 Future Improvements

- 🧩 Refactor the notebook into reusable modules/functions or a Python package.
- 🏷️ Profile and label clusters with business-friendly names (_Loyal_, _At-Risk_, _Churned_) tied to concrete marketing actions.
- 📊 Add interactive dashboards (Plotly / Streamlit / Dash) for dynamic exploration.
- 🔬 Experiment with alternative clustering algorithms (DBSCAN, hierarchical) and validate quality with the silhouette score.
- 🎚️ Handle outliers more rigorously beyond filtering negatives and zeros.

<br>

---

<div align="center">

⭐ _If you found this project helpful or interesting, consider giving it a star!_ ⭐

</div>
