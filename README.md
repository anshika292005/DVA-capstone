# 🌾 Farmer Decision Support System: Mandi Price Analysis

### *Identifying the Best Market and Time to Sell for Maximum Returns*

> **Capstone Project** | **Group 4 (Section B)** | **Newton School of Technology**
> *February 2026*

---

## 📖 Project Overview

Indian farmers often face suboptimal price realization due to information asymmetry and price variations across Mandis (markets). This project analyzes **6,000 transactional records** to build a decision support system that moves farmers from intuition-based to **insight-based agriculture**.

* **Core Objective:** Maximize farmer returns by predicting optimal selling windows and locations.


* **Business Question:** *How can we predict optimal selling windows and locations to minimize distress sales?* 


* **Tech Stack:** Google Sheets (Data Cleaning, Feature Engineering, Dashboarding).



---

## 📊 Dataset & Scope

The analysis covers agricultural data from **2018 to 2026**, sourced from Agmarknet (via Kaggle).

| Dimension | Details |
| --- | --- |
| **Coverage** | 8 States, 8 Markets, 8 Commodities 

 |
| **Time Period** | 2018 – 2026 (7 Years) 

 |
| **Volume** | 6,000 Rows |
| **Commodities** | Cotton, Maize, Onion, Potato, Rice, Soybean, Tomato, Wheat 


---

## 🛠 Data Dictionary & Feature Engineering

We engineered **5 Key Performance Indicators (KPIs)** to drive decision-making.

| Column/KPI | Type | Description & Formula | Decision Relevance |
| --- | --- | --- | --- |
| **Modal Price** | Metric | Most frequent traded price (`₹/q`). | <br>*Revenue Proxy* 

 |
| **Price Spread** | Derived | `Max_Price - Min_Price` | <br>*Volatility/Risk Signal* 

 |
| **PPI** | Derived | **Price Position Index:** `(Modal - Min) / (Max - Min)` | <br>*Negotiation Power (0-1 score)* 

 |
| **RMA** | Derived | **Relative Market Advantage:** `Modal - State Avg` | <br>*Location Choice (Premium vs. Avg)* 

 |
| **Profit Opp.** | Flag | Composite Signal: `Top 25% Price + Positive RMA + PPI > 0.6` | <br>*Action Trigger (When to sell)* 



### 🧹 Data Cleaning Log

All cleaning was performed in Google Sheets. Key actions included:

1. **Imputation:** Fixed 150+ missing `Modal_Price` values using mid-range estimation (`(Min+Max)/2`).


2. **Standardization:** Unified 8 variations of state names (e.g., 'maharashtra' vs 'MAHARASHTRA') using `PROPER()` and `TRIM()`.


3. **Date Parsing:** Standardized mixed date formats to `DD-MM-YYYY` for accurate seasonality analysis.


4. 
**Outlier Validation:** Reviewed and corrected prices below ₹10 or above ₹50,000.



---

## 💡 Key Insights

The analysis generated actionable intelligence for farmers and FPOs:

### 1. 🏆 Top Performing Market: Lucknow

* **Lucknow Mandi** consistently commands the highest average modal price (**₹3,109.78/q**), serving as the benchmark for the northern region.



### 2. 📅 Peak Selling Window: May

* **May** is the peak selling month due to pre-monsoon supply tightening.

**Rabi Season** crops consistently command better prices compared to Kharif or Summer harvests.



### 3. 📉 Volatility = Opportunity

* Average market volatility (Spread) is **₹490/q**, indicating significant arbitrage potential.

**Cotton and Soybean** show the highest spreads (₹700–900/q), suggesting high ROI on sorting/grading investments before sale.



### 4. 📍 Geographic Arbitrage

* **Maharashtra, UP, and Rajasthan** hold the highest share of "High-Profit Opportunity" windows (approx 42% each).


* **Recommendation:** Route bulk produce to Maharashtra markets or Lucknow to capture structural price premiums.



---

## 📈 Dashboard Architecture

The Farmer Decision Dashboard is split into two strategic views:

### 🔹 Executive View (Quick Summary)

* **KPI Strip:** Displays Top Market (Lucknow), Peak Month (May), and Avg Volatility (₹490.20) .


* **RMA Analysis:** Visualizes markets with the highest structural price advantage (Mysuru, Jaipur).



### 🔹 Operational View (Deep Dive)

* **Slicers:** Filter by `Commodity`, `Month`, and `Season`.


* **Seasonal Trends:** Grouped bar charts showing price variations across Rabi vs. Kharif seasons.


* **Opportunity Heatmap:** Stacked bar chart highlighting states with the highest frequency of "High Profit" signals.


---

## 👥 Contributors (Group 4)

* **Khushi** (2401010225) - *Project Lead*
* **Abhinav** (2401010017) - *Data Lead*
* **Anshika** (2401010080) - *Dashboard Lead*
* **Kshitiz** (2401010242) - *PPT & Quality Lead*
* **Abhijeet** (2401010014) - *Analysis Lead*
* **Nishant** (2401010302) - *Strategy Lead*

**Mentors:** Satyaki Sir & Ayushi Ma'am.