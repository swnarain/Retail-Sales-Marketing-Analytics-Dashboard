# Sales & Marketing Performance Dashboard (Power BI)

**End-to-End Data Analytics Project | UK Retail Industry (Simulated Business Case)**
**Role:** Sole Data Analyst (End-to-End Ownership)
**Tools:** Power BI, DAX, Excel, Data Modelling

<img width="1562" height="1042" alt="image" src="https://github.com/user-attachments/assets/d2208512-71d6-44b0-a51d-c478bfeece3e" />

---

## Business Context

A mid-sized UK retail company operating across multiple regions and product categories is experiencing steady revenue growth but lacks **visibility into what is actually driving performance**.

Sales and marketing data exist in silos, limiting leadership’s ability to:

* Understand revenue drivers
* Evaluate marketing efficiency
* Identify high-performing regions
* Make data-driven investment decisions

As a result, strategic decisions around **budget allocation, product focus, and growth strategy** are not fully optimised.

---

## Problem Statement

The business requires a **centralised, data-driven solution** to answer key commercial questions:

* Are we growing sustainably over time?
* Which products and categories drive the most revenue?
* Which regions deliver the highest return on investment?
* Are marketing channels operating efficiently?

Without these insights, the company risks:

* Misallocating marketing spend
* Over-dependence on a narrow product base
* Missing scalable growth opportunities

---

## Project Objective

To design and deliver an **interactive Power BI dashboard** that:

* Tracks core commercial KPIs
* Identifies revenue drivers and underperforming segments
* Evaluates marketing performance using Customer Acquisition Cost (CAC)
* Enables self-service analysis for non-technical stakeholders

---

## My Approach (What I Did)

### 1. Translating Business Needs into Metrics

Defined core KPIs aligned with business goals:

* Total Sales
* Average Order Value (AOV)
* Total Quantity Sold
* Customer Acquisition Cost (CAC)

---

### 2. Data Validation & Preparation

Ensured data reliability before analysis:

* Verified **Total Sales = Price × Quantity**
* Cleaned missing and inconsistent values
* Standardised categorical fields (region, category, channel)

---

### 3. Data Modelling

Designed a **star schema** to optimise performance:

* Fact table: Orders
* Dimension tables: Date, Product, Region, Marketing

Created a dedicated **Date table** to enable:

* Monthly trends
* Year-over-year comparisons

---

### 4. DAX Development

```DAX
Total Sales = SUM(Orders[TotalSales])

Total Quantity = SUM(Orders[QuantitySold])

AOV = DIVIDE([Total Sales], DISTINCTCOUNT(Orders[OrderID]))

CAC = DIVIDE([Total Marketing Spend], [Customers Acquired])
```

Additional logic:

* Product ranking (Top performers)
* Channel and regional breakdowns
* Dynamic filtering across visuals

---

### 5. Dashboard Design

Built with a **business-first approach**:

* KPI cards for quick executive insight
* Clear visual hierarchy (overview → detail)
* Interactive slicers (Date, Region, Category, Product)

Designed for **intuitive use by non-technical stakeholders**.

---

## Dashboard Overview

<img width="1562" height="1042" alt="image" src="https://github.com/user-attachments/assets/d2208512-71d6-44b0-a51d-c478bfeece3e" />






## Key Insights

---

### 1. Growth & Seasonality

<p align="center">
  <img src="https://github.com/user-attachments/assets/626bf6e2-5160-49eb-b1cd-35fb77e27fa1" width="48%" style="border:1px solid #ccc;" />
  <img src="https://github.com/user-attachments/assets/781b15e5-5275-4cce-bf00-9b7cb08a72b8" width="48%" style="border:1px solid #ccc;" />
</p>


* Revenue growth:

  * 2022: £280K
  * 2023: £293K
  * 2024: £304K

* Peak months: January, August

* Low months: September–October

**Insight:**
The business is growing steadily but exhibits strong seasonality, indicating an opportunity to stabilise demand during low periods.

---

### 2. Product & Category Performance

<p align="left">
  <img src="https://github.com/user-attachments/assets/8793cf69-0269-42ad-bf91-a2eb2e99796c" width="48%" style="border:1px solid #ccc;" />
</p>


* Electronics: **57% of total revenue**
* Sports & Outdoors: 21%
* Kitchen: 13%
* Fashion & Apparel: **8.3% (declining trend)**

**Insight:**
Revenue is highly concentrated in Electronics, creating **dependency risk**, while Fashion is underperforming and losing relevance.

---

### 3. Regional Performance & Efficiency

<p align="left">
  <img src="https://github.com/user-attachments/assets/c7b49862-9868-4d3a-bf13-56018f4378c5" width="48%" style="border:1px solid #ccc; border-radius:6px;" />
</p>


Top regions:

* Yorkshire & Humber: £245K
* North West England: £241K

CAC analysis:

* Lowest CAC: Yorkshire
* Highest CAC: Greater London

**Insight:**
Certain regions deliver higher revenue at lower acquisition cost, making them ideal for **scalable growth investment**.

---

### 4. Marketing Performance

![Marketing Performance](images/marketing-performance.png)

Revenue contribution:

* Instagram: 27.9%
* Google Ads: 26.3%
* Facebook: 24.6%
* TikTok: 21.3%

**Insight:**
TikTok generates comparatively lower returns relative to its spend, indicating inefficiencies in targeting, creative execution, or audience alignment.

---

## Business Impact (Value Delivered)

This project goes beyond visualisation by delivering **actionable business value**:

* Identified **high-performing products (Electronics)** as primary revenue drivers
* Highlighted **low-CAC regions** for cost-efficient scaling
* Exposed **inefficient marketing spend**, enabling reallocation of budget
* Revealed **underperforming categories**, informing product strategy decisions

📊 **Outcome:**
If implemented, these insights could:

* Improve **marketing ROI**
* Increase **revenue through targeted investment**
* Reduce **wasted spend on low-performing channels**

---

## Strategic Recommendations

### 1. Scale High-Performing Products

* Focus on Laptops, Smartphones, Bicycles
* Introduce product bundles to increase AOV
* Target high-value customer segments

---

### 2. Address Underperforming Categories

* Reposition Fashion & Apparel
* Use visually driven campaigns (Instagram, TikTok)
* Introduce targeted promotions during low-demand periods

---

### 3. Optimise Marketing Spend

* Increase investment in high-ROI channels (Instagram, Google Ads)
* Rework TikTok strategy (creative testing, influencers)
* Use Facebook for remarketing and retention

---

### 4. Regional Strategy

* Scale investment in low-CAC regions (e.g. Yorkshire)
* Focus on high-margin products in high-cost regions

---

### 5. Continuous Optimisation

* Monthly performance reviews
* A/B testing campaigns
* Ongoing KPI monitoring

---

## Challenges & Limitations

* Simulated dataset lacks real-world complexity (e.g. competition, pricing changes)
* Limited customer-level data (no LTV or retention metrics)
* Simplified marketing attribution (no multi-touch tracking)
* Assumes clean and complete data

**Impact:**
Insights are directionally strong but would require deeper validation in a real-world environment.

---

## 🔍 Future Improvements

* Customer segmentation & lifetime value analysis
* Marketing attribution modelling
* Predictive forecasting
* Promotion and pricing optimisation

---

## 🛠 Skills Demonstrated

* Data Cleaning & Validation
* Data Modelling (Star Schema)
* DAX Calculations
* Data Visualisation (Power BI)
* Business Analysis & Insight Generation
* Stakeholder-Focused Communication

---

## Repository Structure

```
Sales-Marketing-Analytics-Dashboard/
│
├── README.md
├── Sales_Marketing_Dashboard.pbix
├── Sales_Marketing.xlsx
└── images/
```

---

## About Me

I am a data analyst focused on translating data into **clear, actionable business insights**.

Currently seeking opportunities in:

* Data Analytics
* Business Intelligence
* Marketing / Commercial Analytics

---
