# 🛒 Customer Segmentation — RFM + K-Means Clustering

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.4-orange)
![Pandas](https://img.shields.io/badge/Pandas-2.2-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📌 Description

Customer segmentation model using RFM analysis (Recency, Frequency, Monetary)
combined with K-Means clustering to identify behavioral patterns across
4,338 customers from a UK-based e-commerce retailer.
The goal is to support data-driven marketing and retention strategies.

---

## 🎯 Objectives

- Calculate RFM metrics per customer from raw transactional data
- Apply K-Means clustering to identify 4 distinct customer segments
- Determine the optimal number of clusters using the Elbow Method
- Visualize segments with interactive 3D charts (Plotly)
- Provide actionable business recommendations per segment

---

## 🛠️ Tech Stack

| Tool | Usage |
|---|---|
| Python 3.11 | Core language |
| Pandas, NumPy | Data manipulation |
| Scikit-learn | K-Means, StandardScaler |
| Matplotlib, Seaborn | Static visualizations |
| Plotly | Interactive 3D charts |
| JupyterLab | Exploratory analysis |

---

## 📊 Dataset

[Online Retail — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail)

- 541,909 transactions from a UK-based online retailer (Dec 2010 – Dec 2011)
- Key features: InvoiceNo, Quantity, InvoiceDate, UnitPrice, CustomerID, Country
- After cleaning: 4,338 unique customers

---

## 📁 Repository Structure
customer-segmentation-rfm/
│
├── data/
│   ├── raw/                    # Original dataset (Online Retail.xlsx)
│   └── processed/              # Cleaned and transformed data
│
├── notebooks/
│   └── 01_EDA.ipynb            # Full pipeline: EDA → RFM → Clustering → Viz
│
├── reports/
│   └── figures/
│       ├── elbow_method.png
│       ├── rfm_clusters.png
│       ├── segment_distribution.png
│       ├── rfm_3d_segments.html
│       └── segment_pie.html
│
├── src/                        # Modular scripts (refactored pipeline)
│   ├── data_loader.py
│   ├── preprocessing.py
│   ├── model.py
│   └── evaluate.py
│
├── requirements.txt
├── .gitignore
├── main.py
└── README.md



## 📈 Results

| Segment | Recency (days) | Frequency | Avg Monetary (£) | Customers |
|---|---|---|---|---|
| 🏆 Champions | 7 | 83 | £127,338 | 13 |
| 💎 Loyal Customers | 16 | 22 | £12,709 | 204 |
| 🌱 Potential Loyalists | 44 | 4 | £1,359 | 3,054 |
| ⚠️ At Risk | 248 | 2 | £481 | 1,067 |

> Champions represent only 0.3% of customers but drive the highest revenue per customer.
> The largest group (Potential Loyalists, 70%) has strong reactivation potential.


## 💡 Business Recommendations

| Segment | Strategy |
|---|---|
| 🏆 Champions | VIP rewards, loyalty programs, request testimonials |
| 💎 Loyal Customers | Upsell premium products, increase purchase frequency |
| 🌱 Potential Loyalists | Personalized offers, push notifications, discount for 2nd purchase |
| ⚠️ At Risk | Win-back email campaigns, reactivation discounts |



## 🚀 How to Run
1. Clone the repository
git clone https://github.com/gmespinozar15/customer-segmentation-rfm.git
cd customer-segmentation-rfm
2. Install dependencies
pip install -r requirements.txt
3. Open the notebook
jupyter lab


Then open `notebooks/01_EDA.ipynb` and run all cells.

> **Note:** Download the dataset from [UCI ML Repository](https://archive.ics.uci.edu/dataset/352/online+retail)
> and place it in `data/raw/Online Retail.xlsx` before running.



## 📦 Requirements
pandas==2.2.0
numpy==1.26.0
scikit-learn==1.4.0
matplotlib==3.8.0
seaborn==0.13.0
plotly==5.19.0
jupyterlab==4.1.0
openpyxl==3.1.2

## 👩‍💻 Author

Gabriela Espinoza — Data Scientist | Lima, Peru
[LinkedIn](https://linkedin.com/in/your-profile) · [GitHub](https://github.com/gmespinozar15)

This project is part of a Data Science portfolio. Built for learning and professional development.