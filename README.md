# 📊 Vendor Performance & Inventory Sales Analysis

A data analytics project analyzing sales, inventory, and vendor performance for retail and wholesale businesses using **Python**, **Power BI**, and **Tableau**.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Tech Stack](#tech-stack)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Key Findings](#key-findings)
- [Dashboards](#dashboards)
- [System Requirements](#system-requirements)
- [How to Run](#how-to-run)
- [Future Scope](#future-scope)
- [Conclusions](#conclusions)
- [References](#references)

---

## 🧾 Project Overview

This project focuses on analyzing inventory and sales data to identify factors affecting profitability and operational efficiency. Through data analysis techniques such as summary statistics, correlation analysis, and vendor performance evaluation, the project uncovers insights related to:

- Product performance
- Vendor dependency
- Pricing strategies
- Inventory management

**Key Business Metrics:**

| Metric | Value |
|---|---|
| Total Sales | $441.41M |
| Total Purchase | $307.34M |
| Gross Profit | $134.07M |
| Profit Margin | 38.72% |
| Unsold Capital | $2.71M |

---

## ❗ Problem Statement

Retail and wholesale companies often face challenges in:
- Managing inventory and pricing products correctly
- Maintaining profitable vendor relationships
- Identifying underperforming brands without data-driven tools
- Avoiding over-dependence on a few vendors (supply chain risk)
- Optimizing purchasing strategies and maintaining balanced vendor relationships

---

## 🎯 Objectives

1. Analyze sales and inventory data to understand overall business performance
2. Identify underperforming brands that may require promotional or pricing adjustments
3. Determine the top vendors contributing to total sales and gross profit
4. Analyze the impact of bulk purchasing on unit costs and profitability
5. Evaluate inventory turnover to reduce holding costs and improve stock management
6. Compare profit margins between high-performing and low-performing vendors
7. Provide data-driven recommendations to improve profitability and operational efficiency

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Data processing & analysis |
| Pandas, NumPy | Data manipulation |
| Matplotlib, Seaborn | Data visualization |
| Power BI | Interactive dashboard |
| Tableau | Interactive dashboard |
| Jupyter Notebook | Development environment |
| Excel / CSV | Data source |

---

## 📂 Dataset

- **Source:** [Dataset Link](https://topmate.io/ayushi_mishra/1557424)
- **Records:** 10,692 rows
- **Format:** CSV / Excel

### Data Dictionary

| Field | Type | Description |
|---|---|---|
| VendorNumber | Integer | Unique ID for each vendor |
| VendorName | String | Vendor name |
| Brand | String | Brand name of the product |
| Description | String | Product description |
| PurchasePrice | Float | Price at which product was purchased |
| ActualPrice | Float | Selling price of the product |
| TotalPurchaseQuantity | Integer | Total quantity purchased |
| TotalSalesQuantity | Integer | Total quantity sold |
| TotalPurchaseDollars | Float | Total purchase spend |
| TotalSalesDollars | Float | Total sales revenue |
| GrossProfit | Float | Sales revenue minus purchase cost |
| ProfitMargin | Float | Profit percentage on total sales |
| FreightCost | Float | Shipping/transportation cost |
| StockTurnover | Float | Rate at which inventory is sold and replaced |

---

## 📁 Project Structure

```
vendor-performance-analysis/
│
├── data/
│   └── inventory_sales_data.csv       # Raw dataset
│
├── notebooks/
│   └── analysis.ipynb                 # EDA & research questions
│
├── dashboards/
│   ├── PowerBI_Dashboard.pbix         # Power BI dashboard file
│   └── Tableau_Dashboard.twbx         # Tableau dashboard file
│
├── outputs/
│   ├── summary_statistics.png
│   ├── correlation_heatmap.png
│   ├── vendor_contribution_chart.png
│   └── profit_margin_comparison.png
│
├── report/
│   └── FINAL_REPORT.pdf               # Full project report
│
└── README.md
```

---

## 🔍 Key Findings

### 1. Brands for Promotional Adjustments
- **198 brands** have low sales but high profit margins (>65%)
- These brands can benefit from targeted marketing and price optimization

### 2. Vendor Concentration Risk
- The **top 10 vendors** contribute **65.69%** of total purchases
- Remaining vendors contribute only 34.31%
- This concentration creates supply chain vulnerability

### 3. Bulk Purchasing Impact

| Order Size | Unit Purchase Price |
|---|---|
| Small | $39.07 |
| Medium | $15.49 |
| Large | $10.78 |

- Large orders receive up to **72% lower unit cost**

### 4. Slow-Moving Inventory
- **$2.71M** in unsold inventory capital identified
- Vendors like Alisa Carr Beverages (stock turnover: 0.615) and Highland Wine Merchants (0.708) flagged for low turnover

### 5. Profit Margin: Top vs Low Vendors

| Vendor Group | Mean Profit Margin (95% CI) |
|---|---|
| Top Vendors | 31.17% (30.74% – 31.61%) |
| Low Vendors | 41.55% (40.48% – 42.62%) |

- Low-performing vendors maintain **higher margins** but struggle with sales volume

### 6. Correlation Insights
- Total Purchase Quantity vs Total Sales Quantity: **strong correlation (0.999)** — efficient turnover
- Profit Margin vs Total Sales Price: **negative correlation (-0.179)** — pricing pressure
- Stock Turnover vs Gross Profit: **weak negative correlation** — faster turnover ≠ higher profit

---

## 📊 Dashboards

### Power BI Dashboard
![Power BI Dashboard](dashboards/powerbi_screenshot.png)

### Tableau Dashboard
![Tableau Dashboard](dashboards/tableau_screenshot.png)

Both dashboards include:
- KPI cards: Total Sales, Total Purchase, Gross Profit, Profit Margin, Unsold Capital
- Purchase Contribution % (donut chart)
- Top Vendors by Sales (bar chart)
- Top Brands by Sales (bar chart)
- Low Performing Vendors (bar chart)
- Low Performing Brands (scatter plot)

---

## 💻 System Requirements

### Software
- Python 3.8+
- Jupyter Notebook / VS Code / Anaconda
- Power BI Desktop
- Tableau Desktop / Tableau Public
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`

### Hardware
- Processor: Intel Core i3 or higher
- RAM: Minimum 4 GB (8 GB recommended)
- Storage: 500 GB HDD/SSD
- Display: 1366×768 or higher

---

## ▶️ How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/vendor-performance-analysis.git
cd vendor-performance-analysis
```

### 2. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Run the Notebook
```bash
jupyter notebook notebooks/analysis.ipynb
```

### 4. View Dashboards
- Open `dashboards/PowerBI_Dashboard.pbix` in **Power BI Desktop**
- Open `dashboards/Tableau_Dashboard.twbx` in **Tableau Desktop** or **Tableau Public**

---

## 🚀 Future Scope

1. **Real-Time Data Integration** — Connect to live sales/inventory systems
2. **ML Demand Forecasting** — Predict future demand using machine learning
3. **Automated Inventory Optimization** — Smart reorder recommendations
4. **Vendor Risk Monitoring** — Assess reliability, delivery, and pricing consistency
5. **Advanced BI Dashboards** — Interactive exploration with drill-downs
6. **ERP Integration** — Connect with enterprise systems for automated data flow
7. **Mobile/Web App** — Access reports from anywhere
8. **Automated Alerts** — Notify managers of low stock or declining vendor performance
9. **Predictive Profitability** — Forecast margins based on pricing and demand changes

---

## ✅ Conclusions

This project demonstrates how data-driven analysis supports strategic decision-making in:
- Inventory management
- Vendor evaluation
- Pricing strategies

The insights generated enable organizations to identify underperforming vendors, optimize purchasing, reduce inventory inefficiencies, and strengthen profitable vendor relationships — ultimately achieving sustainable growth.

---

## 📚 References

- Han, J., Kamber, M., & Pei, J. (2012). *Data Mining: Concepts and Techniques.* Morgan Kaufmann.
- Provost, F., & Fawcett, T. (2013). *Data Science for Business.* O'Reilly Media.
- Kimball, R., & Ross, M. (2013). *The Data Warehouse Toolkit.* Wiley Publications.
- Dataset: [https://topmate.io/ayushi_mishra/1557424](https://topmate.io/ayushi_mishra/1557424)

---

## 👤 Author

> Made with ❤️ as part of a Data Analytics Project  
> Feel free to ⭐ this repo if you found it helpful!
