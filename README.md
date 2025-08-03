# 🧭 Regional Sales Analysis (Python + Power BI Project)

This end-to-end project analyzes five years of B2B sales data across the U.S. to uncover regional revenue drivers, product profitability, customer segmentation, and performance gaps relative to budgeted expectations. The analysis integrates **Python for exploratory analytics and data storytelling**, and **Power BI for executive-level visualization**.

---

## 📊 Project Overview

📁 **Data Source**: Multi-sheet Excel workbook (Orders, Customers, Products, Regions, Budgets)  
⏱️ **Period Covered**: 2014–2018  
🗺️ **Scope**: United States – All 50 states  
🎯 **Business Goal**: Equip leadership with insights to optimize territory performance, channel strategy, and customer targeting

---

## 🧠 Business Questions Answered

- Which states, regions, and channels generate the most revenue and profit?
- How are our top-performing products and customers distributed geographically?
- Which customer segments contribute the most vs. least profit?
- How do actual sales compare to 2017 budget expectations?
- Where can we improve cost efficiency or increase margins?

---

## 🛠️ Tools & Technologies

| Category        | Tools Used                                     |
|----------------|-------------------------------------------------|
| Data Handling   | Python (Pandas, NumPy), Excel                  |
| Visualization   | Matplotlib, Seaborn, Plotly, Power BI          |
| Mapping         | Plotly Choropleth, Power BI Filled Maps        |
| Dashboarding    | Power BI with bookmarks and interactivity      |
| Reporting       | Jupyter Notebook (Google Colab), GitHub, LinkedIn |

---

## 🧾 Dataset Breakdown

| Sheet Name          | Description                                 |
|---------------------|---------------------------------------------|
| Sales Orders        | ~3,000 rows of order-level transactional data |
| Customers           | Customer ID, Region, and State alignment     |
| Products            | Product categories, unit prices, and costs   |
| Regions / State Map | Regional grouping and state matching         |
| Budgets             | 2017 State-level budget vs. actual data      |

---

## 🔍 Python EDA Highlights (15+ Visuals)

Python was used to:
- **Clean, transform, and merge** 5 different sheets
- **Create new metrics**: `profit`, `margin %`, `revenue per unit`, `customer tiering`
- **Analyze sales trends**: monthly, seasonal, regional
- **Compare budget vs. actuals**

### 📌 Key Visuals

| 📊 Visualization | 💡 Insight |
|------------------|------------|
| **Choropleth Map: Sales by State** | CA, TX, IL dominate revenue ($200M+), but not always margin leaders |
| **Dual Bar: Top vs. Bottom Customers** | 10 customers generated 40% of revenue; bottom tier often unprofitable |
| **Bubble Chart: Customer Profitability** | Revealed hidden inefficiencies — high volume but low-margin clients |
| **Line Chart: Monthly Revenue Trends** | Consistent Q4 spikes; Feb and Aug underperform |
| **Heatmap: Product vs. Region** | Uneven product penetration across states; some SKUs are regionally dominant |

> **Total Visuals**: 15  
> **Charting Libraries**: Matplotlib, Seaborn, Plotly Express
<img width="1472" height="875" alt="Monthly Sales Revenue Trend Analysis" src="https://github.com/user-attachments/assets/81de8522-f413-4c7f-aa0b-5a1cbc3b28b0" />
<img width="1402" height="747" alt="Total Monthly Sales Revenue Trend Analysis (All Years)" src="https://github.com/user-attachments/assets/aa1a0284-9c08-41b0-9e32-907c1b193bc7" />
<img width="1398" height="845" alt="Top 10 Products by Revenue" src="https://github.com/user-attachments/assets/6b3ab2a0-f80b-43a7-9857-73a85defabe9" />
<img width="1408" height="830" alt="Bottom 10 Products by Revenue" src="https://github.com/user-attachments/assets/064fed16-7ff4-42c5-8a1a-9749908007a1" />
<img width="1485" height="807" alt="Top 10 Produts by Average Profit Margin (USD)" src="https://github.com/user-attachments/assets/76a80f98-6c61-4ff8-9118-dde3e4253882" />
<img width="922" height="727" alt="Total Sales by Channel" src="https://github.com/user-attachments/assets/1ffba545-22ed-4ffa-acc7-983e85f447c8" />
<img width="1480" height="606" alt="Distribution of Average Order Value" src="https://github.com/user-attachments/assets/1b986886-3e3f-4f55-bcf6-0e0fb5e46fb5" />
<img width="1021" height="520" alt="Profit Margin % vs Unit Price" src="https://github.com/user-attachments/assets/d8985c81-c330-4402-ad2f-c0b16636c9ca" />
<img width="1368" height="792" alt="Unit Price Distribution - Top 10 Products by Revenue" src="https://github.com/user-attachments/assets/ebf2517a-bd73-4f27-ae86-d4a847e23c5a" />
<img width="1451" height="525" alt="Total Sales by US Region" src="https://github.com/user-attachments/assets/ca4ac574-8437-4ba7-a4a3-1bbee43dcade" />
<img width="1451" height="677" alt="Total Sales by State" src="https://github.com/user-attachments/assets/e81fb312-285a-4bc7-9cdc-e716a3b9c7f4" />
<img width="1456" height="613" alt="Top 10 States by Revenue   Order Count" src="https://github.com/user-attachments/assets/ebdf8f88-b79d-43af-82a6-4ca8cb06f0a2" />
<img width="1065" height="537" alt="Average Profit Margin by Channel" src="https://github.com/user-attachments/assets/07f014b1-2ae5-48c1-a0a8-94f0a1f27e21" />
<img width="1446" height="607" alt="Top   Bottom 10 Customers by Revenue" src="https://github.com/user-attachments/assets/673b95b1-df69-489b-8a92-f79817a583e5" />
<img width="1487" height="686" alt="Customer Segmentation Revenue vs Profit Margin" src="https://github.com/user-attachments/assets/7927cf3c-cfd6-476b-8303-15364fae88e4" />
<img width="742" height="537" alt="Correlation Matrix" src="https://github.com/user-attachments/assets/4ea1161c-9d10-4588-a879-22bea737e66d" />

---

## 📊 Power BI Dashboard (Executive Layer)

Power BI transformed the cleaned dataset into a **multi-tab interactive dashboard**, optimized for stakeholder presentation.

### Tabs Included:
- **Executive Overview**: KPI cards, YoY trends, revenue map
- **Product & Channel Performance**: Top-selling SKUs, margin bands, channel efficiency
- **Geographic & Customer Insights**: Regional breakdown, customer tiers, sales by state

### Features Used:
- DAX Measures & Calculated Columns
- Bookmarks and Navigation Buttons
- Filters for Region, Year, Product Category
- KPI Cards, Line Graphs, Bar Charts, Maps

> 📁 `.pbix` file and screenshots included in `dashboards/`
<img width="1387" height="777" alt="Executive Overview" src="https://github.com/user-attachments/assets/01c11e64-6157-4c0a-8759-4ae12e10feac" />
<img width="1387" height="777" alt="Product   Channel Performance" src="https://github.com/user-attachments/assets/73b58778-76e4-4d19-be4d-e7fd0b52ff9b" />
<img width="1386" height="782" alt="Geographics   Customer Insights Top 5" src="https://github.com/user-attachments/assets/835de0bb-4a61-4b6f-9748-883a111af7ef" />
<img width="1386" height="776" alt="Geographic   Customer Insights Bottom 5" src="https://github.com/user-attachments/assets/53e14969-1e39-4dd2-9131-f34f06f23a1d" />
<img width="1391" height="778" alt="Filter Page" src="https://github.com/user-attachments/assets/9b7d0604-ce0a-4ca1-a3d5-74a3957b67ea" />

---

## 📈 Strategic Insights

✅ **Geographic Focus**: Concentrated revenue in California, Texas, and Illinois — but margin efficiency was highest in select Northeast states  
✅ **Customer Profitability**: A small fraction of customers contributed outsized profit — perfect for targeted retention  
✅ **Channel Analysis**: Certain channels had high volume but lower margin — opportunity for pricing review  
✅ **Product Gaps**: Strong regional skew toward specific SKUs — signals unmet demand in low-penetration areas  
✅ **Budget Performance**: Several high-opportunity states underperformed vs. 2017 budget — worth strategic review













