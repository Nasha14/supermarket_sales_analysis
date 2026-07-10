# 🛒 Supermarket Sales Analysis

An end-to-end data analytics portfolio project analysing supermarket sales data 
across 3 branches (January - March 2019).

## 📌 Problem Statement
How can a supermarket chain understand what drives customer satisfaction and revenue 
performance across its branches, product lines, and customer segments — and use those 
insights to optimise staffing, inventory, and marketing strategies?

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| Python (Google Colab) | Data cleaning, feature engineering, EDA, ML |
| Pandas | Data manipulation and analysis |
| Matplotlib & Seaborn | Data visualisation |
| Scikit-learn | Machine learning models |
| Power BI | Interactive dashboard |
| GitHub | Version control and project sharing |

## 📁 Project Structure

supermarket-sales-analysis/
├── README.md
├── .gitignore
├── LICENSE
├── supermarket_sales_analysis.ipynb
└── supermarket_sales_cleaned.csv

## 📊 Dataset Overview

| Field | Detail |
|---|---|
| Source | Kaggle Supermarket Sales Dataset |
| Transactions | 1,000 rows |
| Period | January – March 2019 |
| Branches | A, B and C across 3 cities |
| Product Lines | 6 categories |
| Target Variables | Revenue (Total) and Customer Rating |

Raw dataset available on Kaggle:
https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales

## 🔍 Key EDA Findings

| Theme | Finding |
|---|---|
| Branch Performance 
| Branch C leads on both revenue ($119.6K) and average rating (7.1) 

| Top Product Line 
| Food & Beverages — highest revenue ($56K) AND highest rating 

| Untapped Revenue
| Health & Beauty is 2nd highest rated but last in revenue ($49K) |

| Peak Trading 
| Saturdays at 7pm generate the highest revenue 
| Monthly Trend | January strongest ($116K); February dips ($97K); March recovers ($109K) 

| Top Customer Segment
| Female Members are the highest value customer segment 

| Payment Methods 
| All three methods nearly equal — no dominant preference |

| Key Insight
| Customer rating has near-zero correlation with all financial variables

## 📈 Power BI Dashboard

An interactive 5-page Power BI dashboard was built from the cleaned dataset with 
synced slicers for Branch, Gender, Customer Type and Payment Method across all pages.

| Page | Focus |
|---|---|
| 1 | Executive Summary — KPIs, revenue trend, branch and product line overview |
| 2 | Branch Performance — revenue, rating and transactions by branch |
| 3 | Product Line Analysis — revenue, quantity, rating and scatter plot |
| 4 | Customer Behaviour — gender, customer type, payment and time patterns |
| 5 | Rating Analysis — distribution, time of day, day of week and segment breakdown |

### Executive Summary
![Executive Summary](images/01_executive_summary.png)

### Branch Performance
![Branch Performance](images/02_branch_performance.png)

### Product Line Analysis
![Product Line Analysis](images/03_product_line_analysis.png)

### Customer Behaviour
![Customer Behaviour](images/04_customer_behaviour.png)

### Rating Analysis
![Rating Analysis](images/05_rating_analysis.png)


> ## 🤖 Machine Learning

Three ML techniques were applied covering supervised and unsupervised learning.

| Model | Type | Result | Key Finding |
|---|---|---|---|
| Logistic Regression 
| Classification 56% accuracy Barely above random chance 

| Random Forest 
| Classification 47% accuracy Below random chance 

| Linear Regression 
| Regression R2 -0.03  No predictive power 

| Random Forest 
| Regression  R2 -0.09  No predictive power 

| Gradient Boosting 
| Regression  R2 -0.12  No predictive power 

| KMeans Clustering 
| Unsupervised Silhouette 0.24  2 customer segments identified 

### ML Conclusion
Customer type and rating could not be predicted from transaction data alone. 
This is not a data quality issue but a dataset limitation — membership status 
and satisfaction are driven by factors not captured in transactional records 
such as staff behaviour, wait time, and store environment.

The clustering model identified 2 distinct customer segments:

| Segment | Size | Avg Transaction | Avg Quantity | Avg Rating |
|---|---|---|---|---|
| High Value Customers | 348 (34.8%) | $609.29 | 7.87 items | 6.90 |
| Regular Customers | 652 (65.2%) | $170.14 | 4.25 items | 7.01 |

> Key Insight: High value customers spend 3.5x more but report virtually 
> identical satisfaction scores to regular customers.

## 💡 Business Recommendations

| # | Recommendation | Rationale |
|---|---|---|
| 1 | Collect customer experience data | Add staff rating and wait time surveys at POS to enable future satisfaction modelling |
| 2 | Retain high value customers | Cluster 0 spends 3.5x more — prioritise through exclusive loyalty rewards |
| 3 | Promote Health & Beauty | 2nd highest rated but last in revenue — targeted promotions could convert satisfaction to sales |
| 4 | Maximise Saturday 7pm window | Peak revenue hour and day — ensure maximum staffing and full product availability |
| 5 | Investigate February dip | Revenue fell 16% from January — track full year to confirm if seasonal |
| 6 | Review membership programme | Members and Normal customers shop identically — membership benefits need redesigning |
| 7 | Expand data collection period | 3 months insufficient for seasonal ML modelling — 12-24 months needed |
| 8 | Investigate Branch B satisfaction | Lowest average rating (6.8) with no dominant product category |

## ▶️ How to Run the Notebook

1. Download `supermarket_sales_cleaned.csv` from this repository
2. Upload it to Google Colab or your local Jupyter environment
3. Open `supermarket_sales_analysis.ipynb`
4. Run all cells in order

### Required Libraries
```python
pip install pandas numpy matplotlib seaborn scikit-learn
```

## 📋 Project Phases

- [x] Data Cleaning & Feature Engineering
- [x] Exploratory Data Analysis
- [x] Power BI Dashboard
- [x] Machine Learning
- [ ] Dashboard Screenshots (coming soon)

## 👤 Author
  Nuuraishah Binte Noor Mohamed
- GitHub: Nasha14 https://github.com/Nasha14
- LinkedIn: https://www.linkedin.com/in/nuuraishah-noor-mohamed-6001b981/

## 📄 License

This project is licensed under the MIT License — see the LICENSE file for details.
