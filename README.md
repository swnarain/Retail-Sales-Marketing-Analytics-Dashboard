# Sales & Marketing Performance Dashboard (Power BI)


**End-to-End Data Analytics Project | UK Retail Industry (Simulated Business Case)**

**Tools:** Power BI, DAX, Excel, Data Modelling

<img width="1562" height="1042" alt="image" src="https://github.com/user-attachments/assets/d2208512-71d6-44b0-a51d-c478bfeece3e" />

---

# Table of Contents
1. [Business Context](#business-context)  
2. [Problem Statement](#problem-statement)  
3. [Project Objective](#project-objective)  
4. [Business Requirements & KPI Framework](#business-requirements--kpi-framework)  
5. [My Approach](#my-approach)  
6. [Dashboard Overview](#dashboard-overview)  
7. [Key Insights](#key-insights)  
8. [Strategic Recommendations](#strategic-recommendations)  
9. [Business Impact](#business-impact-value-delivered)  
10. [Challenges & Limitations](#challenges--limitations)  
11. [Future Improvements](#-future-improvements)  
12. [Skills Demonstrated](#-skills-demonstrated)  
13. [Repository Structure](#repository-structure)  
14. [About Me](#about-me)

---

# Business Context

A mid-sized UK retail company operating across multiple regions and product categories is experiencing steady revenue growth but lacks **visibility into what is actually driving performance**.

Sales and marketing data exist in silos, limiting leadership’s ability to:

* Understand revenue drivers
* Evaluate marketing efficiency
* Identify high-performing regions
* Make data-driven investment decisions

As a result, strategic decisions around **budget allocation, product focus, and growth strategy** are not fully optimised.

---

# Problem Statement

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

# Project Objective

**Business Requirements & KPI Framework**

To ensure the solution directly addressed business needs, I translated stakeholder questions into a structured set of analytical requirements and measurable KPIs.

<table>
  <thead style="background-color:#1E90FF; color:white;">
    <tr>
      <th>#</th>
      <th>Business Requirement</th>
      <th>Requirement Description</th>
      <th>Business Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Overall Revenue Performance</td>
      <td>Calculate total revenue across all transactions</td>
      <td>Provides a clear view of overall financial performance and tracks progress against growth targets</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Customer Spend Behaviour (AOV)</td>
      <td>Calculate Average Order Value (AOV)</td>
      <td>Helps understand purchasing behaviour and identify opportunities to increase basket size</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Sales Volume Tracking</td>
      <td>Measure total quantity sold</td>
      <td>Supports demand analysis and operational planning</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Marketing Efficiency (CAC)</td>
      <td>Calculate Customer Acquisition Cost (CAC)</td>
      <td>Evaluates effectiveness of marketing spend and supports budget optimisation</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Time-Based Performance Analysis</td>
      <td>Analyse monthly and yearly sales trends</td>
      <td>Identifies seasonality patterns and supports strategic planning</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Product & Category Performance</td>
      <td>Analyse revenue by product category</td>
      <td>Identifies high-performing categories and informs inventory and marketing strategy</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Regional Performance</td>
      <td>Compare sales across regions</td>
      <td>Highlights regional strengths and growth opportunities</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Top Product Analysis</td>
      <td>Identify top-performing products by revenue</td>
      <td>Supports product prioritisation and promotional strategy</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Regional Marketing Efficiency</td>
      <td>Compare CAC across regions</td>
      <td>Identifies where acquisition is most cost-effective</td>
    </tr>
    <tr>
      <td>10</td>
      <td>Marketing Channel Effectiveness</td>
      <td>Analyse revenue contribution by channel</td>
      <td>Enables optimisation of marketing mix</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Interactive Analysis</td>
      <td>Enable filtering by date, region, category, and product</td>
      <td>Allows stakeholders to explore insights independently</td>
    </tr>
  </tbody>
</table>


# My Approach



**1. Translating Requirements into KPIs**

Based on the defined business requirements, I translated key questions into measurable KPIs that reflect both commercial performance and marketing efficiency:

- **Total Sales** – to track overall revenue performance  
- **Average Order Value (AOV)** – to understand customer purchasing behaviour and basket size  
- **Total Quantity Sold** – to measure sales volume and demand trends  
- **Customer Acquisition Cost (CAC)** – to evaluate the efficiency of marketing spend  

These KPIs formed the foundation of the dashboard and ensured that all analysis remained aligned with business objectives.



**2. Data Validation & Preparation**

Ensured data reliability before analysis:

* Verified **Total Sales = Price × Quantity**
* Cleaned missing and inconsistent values
* Standardised categorical fields (region, category, channel)
  


**3. Data Modelling**

- Designed a **star schema** to optimise performance:

* Fact table: Orders
  
* Dimension tables: Date, Product, Region, Marketing

- Created a dedicated **Date table** to enable:

* Monthly trends
  
* Year-over-year comparisons
  


**4. DAX Development**

```DAX
Total Sales = SUM(Orders[TotalSales])

Total Quantity = SUM(Orders[QuantitySold])

AOV = DIVIDE([Total Sales], DISTINCTCOUNT(Orders[OrderID]))

CAC = DIVIDE([Total Marketing Spend], [Customers Acquired])
```


**Additional logic:**

* Product ranking (Top performers)
* Channel and regional breakdowns
* Dynamic filtering across visuals


**5. Dashboard Design**


Built with a **business-first approach**:

* KPI cards for quick executive insight
* Clear visual hierarchy (overview → detail)
* Interactive slicers (Date, Region, Category, Product)

Designed for **intuitive use by non-technical stakeholders**.



# Dashboard Overview

<img width="1562" height="1042" alt="image" src="https://github.com/user-attachments/assets/d2208512-71d6-44b0-a51d-c478bfeece3e" />




# Key Insights

---

## 1. Sales Growth & Seasonality

<p align="center">
  <img src="https://github.com/user-attachments/assets/626bf6e2-5160-49eb-b1cd-35fb77e27fa1" width="48%" style="border:1px solid #ccc;" />
  <img src="https://github.com/user-attachments/assets/781b15e5-5275-4cce-bf00-9b7cb08a72b8" width="48%" style="border:1px solid #ccc;" />
</p>


Sales increased steadily over the three-year period, rising from **£280K in 2022** to **£304K in 2024**, demonstrating consistent year-on-year growth.

Monthly trends reveal strong seasonality:

* **Peak sales in January and August**, likely driven by promotional campaigns or seasonal demand
* **Lower sales in September and October**, indicating off-peak periods
* Recovery in **November and December**, suggesting increased holiday season demand

**Business Insight:**

While the company is achieving steady revenue growth, seasonal fluctuations indicate opportunities to improve sales performance during weaker months through targeted promotions and demand-generation campaigns.



### 2. Product Category Concentration

<p align="left">
  <img src="https://github.com/user-attachments/assets/8793cf69-0269-42ad-bf91-a2eb2e99796c" width="48%" style="border:1px solid #ccc;" />
</p>


**Electronics generates 57% of total revenue (£505K)**, significantly outperforming all other categories. In contrast, **Fashion & Apparel contributes only 8.3% (£73K)** and continues to underperform.

**Business Insight:**

The business is highly dependent on Electronics for revenue growth. While this category drives performance, over-reliance creates concentration risk. Meanwhile, the weak performance of Fashion & Apparel suggests poor product positioning or limited market demand.



### 3. Regional Sales Performance

<p align="left">
  <img src="https://github.com/user-attachments/assets/c7b49862-9868-4d3a-bf13-56018f4378c5" width="48%" style="border:1px solid #ccc; border-radius:6px;" />
</p>

**Yorkshire and the Humber (£245K)** and **North West England (£241K)** are the strongest-performing regions.

Electronics leads across all regions, with particularly strong performance in:

* North West England (£153K)
* Yorkshire and the Humber (£135K)

**Business Insight:**

Regional performance indicates strong revenue opportunities in specific markets, particularly where Electronics performs well. These regions present scalable growth opportunities and should be prioritised in regional sales planning.



### 4. Product Revenue Drivers

<p align="left">
  <img src="https://github.com/user-attachments/assets/aeeaa1f1-d0cc-4f7e-9cf2-cb5c0d1e7d65" width="48%" style="border:1px solid #ccc; border-radius:6px;" />
</p>


The highest revenue-generating products are:

* **Laptops (£224K)**
* **Smartphones (£145K)**
* **Bicycles (£95K)**

These products account for a significant share of overall sales.

**Business Insight:**

Revenue is concentrated among a small number of top-performing products. These items are key commercial drivers and should be prioritised for inventory availability, promotional campaigns, and cross-selling opportunities.



### 5. Customer Acquisition Cost (CAC) Efficiency

<p align="left">
  <img src="https://github.com/user-attachments/assets/9b9f8b0c-2ae5-40b4-aea0-328811f2eb62" width="48%" style="border:1px solid #ccc; border-radius:6px;" />
</p>


Customer acquisition costs vary significantly by region:

* **Highest CAC:** Greater London (£12.2), North West England (£11.9)
* **Lowest CAC:** Yorkshire and the Humber

**Business Insight:**

Yorkshire delivers stronger cost efficiency in acquiring customers, making it an attractive region for scaling acquisition efforts. Higher CAC in London suggests stronger competition or lower marketing efficiency.



### 6. Marketing Channel Performance

<p align="left">
  <img src="https://github.com/user-attachments/assets/e7738e9b-9b8a-46dd-ac19-becb778b8ee5" width="48%" style="border:1px solid #ccc; border-radius:6px;" />
</p>


The highest-performing marketing channels are:

* **Instagram: 27.9% of revenue**
* **Google Ads: 26.3%**
* **Facebook: 24.6%**
* **TikTok: 21.3%**

Instagram and Google Ads together contribute over half of total revenue.

**Business Insight:**

Instagram and Google Ads deliver the strongest revenue contribution and represent the most effective channels for growth. TikTok contributes meaningfully but underperforms relative to the leading channels, indicating room for optimisation.



### 7. Underperforming Category Trend

<p align="left">
  <img src="https://github.com/user-attachments/assets/3f58fc0a-73fe-4013-badf-264efa95f168" width="48%" style="border:1px solid #ccc; border-radius:6px;" />
</p>


Fashion & Apparel sales declined from:

* **£27.4K in 2022**
* **£26.5K in 2023**
* **£19K in 2024**

**Business Insight:**

The continued decline in Fashion & Apparel suggests that the category is losing market traction. Without intervention, this segment may continue to reduce overall portfolio profitability.

---

## Strategic Recommendations

### 1. Scale High-Performing Products

Increase investment in high-revenue products such as **Laptops, Smartphones, and Bicycles** by:

* Expanding stock availability
* Running targeted promotions
* Bundling complementary items to increase Average Order Value

**Expected Impact:**

Higher revenue growth through improved product focus and increased basket value.



### 2. Reposition Underperforming Categories

Improve Fashion & Apparel performance by:

* Refreshing the product mix
* Running category-specific promotions
* Using influencer and visual-first campaigns to increase engagement

**Expected Impact:**

Revitalising this category could improve category balance and reduce over-reliance on Electronics.



### 3. Optimise Marketing Channel Investment

Allocate a greater share of spend to **Instagram and Google Ads**, where performance is strongest, while improving TikTok through:

* Platform-specific creative content
* Influencer partnerships
* Better audience targeting

**Expected Impact:**

Higher marketing ROI and improved channel efficiency.



### 4. Focus Growth in Low-CAC Regions

Increase marketing investment in **Yorkshire and the Humber**, where customer acquisition costs are lower and sales performance is strong.

For high-CAC regions such as London:

* Prioritise higher-margin products
* Focus on customer retention strategies

**Expected Impact:**

More efficient growth through better regional budget allocation.



### 5. Address Seasonal Revenue Gaps

Launch targeted campaigns during low-performing months (September–October), such as:

* Promotional discounts
* Seasonal product bundles
* Demand generation campaigns

**Expected Impact:**

Reduced seasonality risk and more consistent monthly revenue.



## Business Impact (Value Delivered)

This project goes beyond visualisation by delivering **actionable business value**:

* Identified **high-performing products (Electronics)** as primary revenue drivers
* Highlighted **low-CAC regions** for cost-efficient scaling
* Exposed **inefficient marketing spend**, enabling reallocation of budget
* Revealed **underperforming categories**, informing product strategy decisions

**Outcome:**

If implemented, these insights could:

* Improve **marketing ROI**
* Increase **revenue through targeted investment**
* Reduce **wasted spend on low-performing channels**



## Challenges & Limitations

* Simulated dataset lacks real-world complexity (e.g. competition, pricing changes)
* Limited customer-level data (no LTV or retention metrics)
* Simplified marketing attribution (no multi-touch tracking)
* Assumes clean and complete data

**Impact:**

Insights are directionally strong but would require deeper validation in a real-world environment.



## Future Improvements

* Customer segmentation & lifetime value analysis
* Marketing attribution modelling
* Predictive forecasting
* Promotion and pricing optimisation



## Skills Demonstrated

* Data Cleaning & Validation
* Data Modelling (Star Schema)
* DAX Calculations
* Data Visualisation (Power BI)
* Business Analysis & Insight Generation
* Stakeholder-Focused Communication



## Repository Structure

```
Retail-Sales-Marketing-Analytics-Dashboard/
│
├── README.md
├── Sales_Marketing_Dashboard.pbix
├── Sales_Marketing.xlsx
```

---

## About Me

As a data analyst I translate data into **clear, actionable business insights**.

Currently seeking opportunities in:

* Data Analytics
* Business Intelligence
* Marketing / Commercial Analytics

---
