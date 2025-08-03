# 🧭 Regional Sales Analysis (Python + Power BI Project)

This comprehensive analytics project explores over **64,000 rows of sales data** across the United States from 2014 to 2018. It involves full-cycle analysis: from **data extraction, cleaning, and merging of 5 distinct tables**, to **insight generation in Python via Google Colab**, and **executive dashboard storytelling in Power BI**.

---

## 🧩 Problem Statement & Objective

**Problem Statement**  
Acme Co needed to assess four years of regional sales performance to understand revenue and profit drivers, detect seasonal and geographic trends, and evaluate underperformance against budgeted expectations.

**Objective**  
The goal was to deliver a dual-layered analytics product—technical EDA in Python and executive-ready visuals in Power BI—to highlight:
- Performance discrepancies across geographies
- High- vs. low-performing products and customers
- Budget adherence and forecasting trends
- Profit margin and cost structure inefficiencies

---

## 🔍 Dataset Overview

| Sheet / Table      | Description                                        |
|--------------------|----------------------------------------------------|
| Sales Orders       | Transaction-level sales data (main fact table)     |
| Customers          | Customer location, state, and channel              |
| Products           | Product SKUs, category, unit price, cost           |
| Regions            | Mapping states into larger US regions              |
| Budgets            | 2017 forecasted sales by state                     |

**Total Volume**: ~64,000 rows  
**Merge Complexity**: Required aligning customer IDs, product IDs, and state keys across five tables to construct an integrated analytical base.

---

## 🧹 Data Cleaning & Wrangling

Performed entirely in **Google Colab**, the data wrangling involved:

- Handling null values and standardizing date/time formats
- Converting financial figures from string/object to float
- Creating derived columns like `profit`, `margin (%)`, `unit revenue`, and `customer tier`
- Standardizing column naming conventions
- Validating integrity after multi-table joins with `.merge()` across key relationships
- Aggregating, grouping, and filtering to prepare for visual storytelling

---

## 🧠 Python EDA (Google Colab): Key Visuals & Insights

Over 15 visualizations were developed to explore trends and segment insights:

| Visualization | Key Insights |
|---------------|--------------|
| **Choropleth Map: Revenue by State** | CA, TX, IL led in revenue, but high cost-to-revenue ratios lowered margin |
| **Profit vs. Revenue by State** | Some low-revenue states had higher profit efficiency (e.g., MA, NJ) |
| **Monthly Revenue Line Chart** | Q4 surges yearly; Feb and Aug consistently underperform |
| **Product-Level Performance** | Certain SKUs (like Product B and C) had high sales but thin margins |
| **Customer Profitability Bubble Chart** | High-volume clients didn’t always yield high profit—detected margin erosion |
| **Top vs. Bottom Customers** | Bottom 10 customers consistently incurred losses—candidate for price restructuring |
| **Budget vs. Actual State Bar Chart** | Budget misses in FL, NC, and MI triggered follow-up opportunity flags |
| **Regional Margin Map** | Northeast showed highest margin %, South had widest margin variability |

> Tools: `Pandas`, `Seaborn`, `Plotly`, `Matplotlib`  
> Environment: **Google Colab** (not Jupyter Notebook)
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

## 📊 Power BI Dashboard: Executive Visual Layer

After cleaning and exporting the dataset from Python, the data was loaded into Power BI to create an executive-ready dashboard with 3 interactive tabs:

### 1️⃣ Executive Overview
- KPIs: Total Revenue, Profit, Margin %, Total Orders
- Monthly trend line for revenue and profit
- Map visualization of revenue and margin by state

### 2️⃣ Product & Channel Performance
- Bar chart: Profit per product and per channel
- KPI cards: Best-selling product, channel with highest margin
- Segmentation by unit price and cost structures

### 3️⃣ Geographic & Customer Insights
- Map of customer-level revenue contribution
- Customer tiers based on total sales
- Margin analysis by customer and state

> All visuals are interactive, filterable by region, year, channel, and customer tier  
> DAX measures were created to calculate profit, unit margin, and conditional formatting

> 📁 `.pbix` file and screenshots included in `dashboards/`
<img width="1387" height="777" alt="Executive Overview" src="https://github.com/user-attachments/assets/01c11e64-6157-4c0a-8759-4ae12e10feac" />
<img width="1387" height="777" alt="Product   Channel Performance" src="https://github.com/user-attachments/assets/73b58778-76e4-4d19-be4d-e7fd0b52ff9b" />
<img width="1387" height="782" alt="Geographics   Customer Insights Top 5" src="https://github.com/user-attachments/assets/b3fb3fd5-37fb-4135-be3b-50ee62812aa7" />
<img width="1386" height="776" alt="Geographic   Customer Insights Bottom 5" src="https://github.com/user-attachments/assets/53e14969-1e39-4dd2-9131-f34f06f23a1d" />
<img width="1391" height="778" alt="Filter Page" src="https://github.com/user-attachments/assets/9b7d0604-ce0a-4ca1-a3d5-74a3957b67ea" />

---

## 🎯 Strategic Outcomes

- **Targetable High-Margin Regions Identified**: Northeastern states showed highest profit % with moderate revenue—opportunity to scale
- **Customer Segmentation Enabled**: Tiers defined for profitability, driving account prioritization strategies
- **Channel Optimization Detected**: Volume ≠ profit — Channel C had highest unit profit despite lower overall revenue
- **Budget Gap Regions Flagged**: NC, MI, and FL fell short of budget projections—triggering review of pipeline and execution
- **Executive Dashboard Delivered**: Fully functional and polished Power BI dashboard aligned to business stakeholder needs

---

## 🧠 Recruiter & Hiring Manager Takeaway

This project simulates a real-world BI analyst workflow:

- Extracting and merging large datasets (64,000+ rows across 5 tables)
- Deep analysis using Python in Google Colab
- Delivering executive visuals in Power BI
- Bridging business KPIs with technical storytelling

Perfect for roles involving **Sales Analytics, Business Intelligence, Data Analysis**, and **Operations Strategy**.








