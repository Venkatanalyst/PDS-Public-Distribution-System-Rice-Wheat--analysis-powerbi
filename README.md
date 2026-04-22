# 📊 Public Distribution System (PDS) Performance

## 🔍 Project Overview

This project analyzes the **Public Distribution System (PDS)** dataset to evaluate the efficiency of grain allocation, distribution, and wastage across states and districts in India.

The workflow includes **data cleaning, transformation, and visualization** using **Microsoft Excel, Power Query, and Power BI**.

An interactive dashboard is developed to provide stakeholders with a **Single Source of Truth**, enabling data-driven decision-making for improving food distribution systems.

---

## 🎯 Objectives

1. **End-to-End visibility** 
   Track the lifecycle of food grains from initial allocation to final distribution.

2. **Gap analysis** 
   Quantify and localize wastage (the delta between allocation and distribution).

3. **Regional benchmarking** 
   Compare state and district performance using a standardized efficiency index.

4. **Historical trends (2017–2021)**
   Analyse historical patterns (2017–2021) to identify seasonal supply chain pressures.

5. **Data-driven accountability system** 
   Rank states based on a custom efficiency Index to drive systemic improvements.

6. **Distribution efficiency** 
   Compare allocated vs actual distributed quantities to identify underperforming States

---

## ❗ Problem Statement

Managing food supply for a large population involves significant logistical challenges. The PDS system often faces:

* Grain leakage
* Distribution delays
* Lack of centralized analytical visibility

This project converts raw transactional data into **actionable insights** to identify whether issues are **localized or systemic**.

---

## 📂 Data Source

* **Dataset:** PDS District-Wise Monthly Wheat and Rice Data
* **Source:** [https://indiadataportal.com/p/public-distribution-system-pds](https://indiadataportal.com/p/public-distribution-system-pds)
* **Domain:** Supply Chain
* **Timeline:** 2017 – 2021

---

## 🧾 Attribute Details

| Attribute          | Type      | Description                                    | Usage                             |
| ------------------ | --------- | ---------------------------------------------- | --------------------------------- |
| State & Code       | Dimension | Unique state identifier for mapping            | Used in map visuals & filters     |
| Total Wastage      | Measure   | Difference between allocation and distribution | Identifies leakage & inefficiency |
| Month Name         | Dimension | Used for seasonal analysis                     | Enables monthly trend charts      |
| Average Efficiency | Measure   | Normalized performance metric                  | Compares regions fairly           |
| Category           | Dimension | Rice/Wheat filter                              | Slicer for commodity selection    |
| Allocated Quantity | Fact      | Total assigned grain                           | Baseline for performance analysis |
| Current YTD        | Fact      | Year-to-date distribution                      | Tracks annual progress            |
| Performance Status | Dimension | High / Medium / Low classification             | Highlights performance tiers      |

---

## 🛠️ Tools & Technologies

### Microsoft Excel

* Data cleaning
* Handling missing values
* Initial preprocessing

### Power BI

* Data modeling
* Dashboard creation
* Interactive visualizations

### Power Query

* Data transformation (ETL)
* Removing duplicates
* Data formatting

### DAX

* KPI calculations
* Efficiency & ranking logic
* Time intelligence measures

---

## 🧹 Data Preprocessing Steps

* **Data Cleaning**
  Removed null values and corrected inconsistent naming conventions for states and districts.

* **Type Conversion**
  Standardized numeric columns to decimal formats for precise calculation and ensured date columns followed a uniform DD-MM-YYYY format.

* **Column Splitting/Merging**
  Parsed "Location & ID" strings into distinct columns for cleaner filtering.

* **Formatting**
  Applied consistent naming across all headers for better readability within the Power BI field pane.

* **Date Engineering**
  Generated a comprehensive Calendar Table to support DAX time-intelligence functions.

---

## 🔗 Data Modeling

* **Fact Tables:**

  * Public Distribution System
  * Rice Performance
  * Wheat Performance

* **Dimension Tables:**

  * Calendar Table
  * Lookup tables

* **Relationships:**

  * One-to-Many (1:*) relationships for efficient filtering

---

## 🧮 DAX Calculations

### Calculated Columns

* **Category**
  Segments data based on grain types for rapid slicer interaction.
* **Performance Tiers**
  A logical column classifying districts into High, Medium, or Low performance based on distribution percentages.
* **Shortfall Indicator**
  A flag to highlight districts where distribution fell below 90% of the allocation.
* **Grain Category**
  Simplifies the selection between Wheat and Rice for end-users

### Measures

* **Total Allocation**
  Establishes the baseline target. the total quantity of food grains the government intended to provide for a specific period or region.

* **Total Distribution**
   Measures the actual execution. This is the most critical figure for determining the success of the supply chain.

* **Total Wastage**
  Quantifies "Leakage." In a PDS context, this identifies grain that was allocated but never reached the end consumer, signalling potential logistical issues, storage loss, or data reporting gaps.

* **Efficiency (%)**
  Normalizes performance. It allows us to compare a small district with a large state fairly. An $85\%$ efficiency in a small district is objectively comparable to $85\%$ in a large state, even if the volumes differ

* **State Rank**
  Gamifies performance. It automatically assigns a numerical rank to each state. If a user filters by "Wheat," the rank recalculates to show who the top wheat distributors are.

* **Average Efficiency**
  Provides a "Health Check" for a region. It calculates the mean performance across all sub-entities, helping to identify if a state's high volume is driven by just one good district or if performance is consistent across the board**.**

* **YTD Distribution**
  Tracks progress against annual goals. As the year progresses, this measure climbs, allowing officials to see if they are on track to meet their yearly distribution quotas.

* **Running Total (Monthly)**
  Visualizes the  distribution over the months, making it easy to spot which months have the highest activity.

---

## 📈 Dashboard & Visualizations

* **Treemap**
  Monthly performance distribution
* **Funnel Chart**
  State ranking
* **Area Chart**
  Trend analysis
* **Matrix Table**
  District-level details
* **Donut & Bar Charts**
  Wastage analysis
* **KPI Cards**
  Key metrics overview

  ## 📷 Dashboard Preview

<img width="606" height="335" alt="Overview" src="https://github.com/user-attachments/assets/cc8ea13c-b830-4e7e-9b4c-b13bc5e99754" />

---

<img width="603" height="333" alt="Performance" src="https://github.com/user-attachments/assets/e0d2e96b-a88e-4487-afe1-44d20bad0dcb" />

---

<img width="605" height="333" alt="Distribution" src="https://github.com/user-attachments/assets/ca25ddc8-1d67-4b53-87d5-ff12de6fa49a" />

---

## 💡 Key Insights

### Performance Insights

* High-performing districts achieve **>95% efficiency**
* Low-performing districts fall below **70% efficiency**
* Active centers perform significantly better than inactive ones

### Distribution Trends

* Southern/Eastern regions prefer **Rice**
* Northern regions prefer **Wheat**
* Top districts contribute **40%+ of total distribution**

### Wastage Analysis

* Gaps >10% indicate critical issues
* Rural areas face logistical challenges
* Zero distribution over time indicates **high spoilage risk**

---

## 📌 Conclusion

This project transforms raw PDS data into a **powerful analytical solution**.

It enables:

* Improved supply chain efficiency
* Reduced wastage
* Better policy decision-making

Ultimately, it ensures that **essential food resources reach the intended beneficiaries effectively and transparently**.

---


## 🚀 Author

**V.Venkatesh**
Data Analyst | Power BI Developer

🌐 GitHub: [Venkatanalyst](https://github.com/Venkatanalyst/)

💼 LinkedIn: [Venkatesh Venugopal](https://www.linkedin.com/in/venkatesh-v-dataanalyst/)

📧 Email: Calepsundar08@gmail.com

If you found this project useful or have feedback, feel free to reach out!

📚 Tags
#PowerBI #DataAnalysis #PublicSystem #PerformanceAnalytics
#DAX #DataVisualization #ExcelPowerQuery

