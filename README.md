📊 PDS-Public-Distribution-System-Rice-Wheat--Performance

🔍 Project Overview

This project analyzes the Public Distribution System (PDS) dataset to evaluate the efficiency of grain allocation, distribution, and wastage across states and districts in India.

The workflow includes data cleaning, transformation, and visualization using Microsoft Excel, Power Query, and Power BI.

An interactive dashboard is developed to provide stakeholders with a Single Source of Truth, enabling data-driven decision-making for improving food distribution systems.

🎯 Objectives

End-to-End visibility Track the lifecycle of food grains from initial allocation to final distribution.

Gap analysis Quantify and localize wastage (the delta between allocation and distribution).

Regional benchmarking Compare state and district performance using a standardized efficiency index.

Historical trends (2017–2021)Analyse historical patterns (2017–2021) to identify seasonal supply chain pressures.

Data-driven accountability system Rank states based on a custom efficiency Index to drive systemic improvements.

Distribution efficiency Compare allocated vs actual distributed quantities to identify underperforming States

❗ Problem Statement

Managing food supply for a large population involves significant logistical challenges. The PDS system often faces:

Grain leakage

Distribution delays

Lack of centralized analytical visibility

This project converts raw transactional data into actionable insights to identify whether issues are localized or systemic.

📂 Data Source

Dataset: PDS District-Wise Monthly Wheat and Rice Data

Source: https://indiadataportal.com/p/public-distribution-system-pds

Domain: Supply Chain

Timeline: 2017 – 2021

🧾 Attribute Details

Attribute

Type

Description

Usage

State & Code

Dimension

Unique state identifier for mapping

Used in map visuals & filters

Total Wastage

Measure

Difference between allocation and distribution

Identifies leakage & inefficiency

Month Name

Dimension

Used for seasonal analysis

Enables monthly trend charts

Average Efficiency

Measure

Normalized performance metric

Compares regions fairly

Category

Dimension

Rice/Wheat filter

Slicer for commodity selection

Allocated Quantity

Fact

Total assigned grain

Baseline for performance analysis

Current YTD

Fact

Year-to-date distribution

Tracks annual progress

Performance Status

Dimension

High / Medium / Low classification

Highlights performance tiers

🛠️ Tools & Technologies

Microsoft Excel

Data cleaning

Handling missing values

Initial preprocessing

Power BI

Data modeling

Dashboard creation

Interactive visualizations

Power Query

Data transformation (ETL)

Removing duplicates

Data formatting

DAX

KPI calculations

Efficiency & ranking logic

Time intelligence measures

🧹 Data Preprocessing Steps

Data CleaningRemoved null values and corrected inconsistent naming conventions for states and districts.

Type ConversionStandardized numeric columns to decimal formats for precise calculation and ensured date columns followed a uniform DD-MM-YYYY format.

Column Splitting/MergingParsed "Location & ID" strings into distinct columns for cleaner filtering.

FormattingApplied consistent naming across all headers for better readability within the Power BI field pane.

Date EngineeringGenerated a comprehensive Calendar Table to support DAX time-intelligence functions.

🔗 Data Modeling

Fact Tables:

Public Distribution System

Rice Performance

Wheat Performance

Dimension Tables:

Calendar Table

Lookup tables

Relationships:

One-to-Many (1:*) relationships for efficient filtering

🧮 DAX Calculations

Calculated Columns

CategorySegments data based on grain types for rapid slicer interaction.

Performance TiersA logical column classifying districts into High, Medium, or Low performance based on distribution percentages.

Shortfall IndicatorA flag to highlight districts where distribution fell below 90% of the allocation.

Grain CategorySimplifies the selection between Wheat and Rice for end-users



Measures

Total AllocationEstablishes the baseline target. the total quantity of food grains the government intended to provide for a specific period or region.

Total Distribution Measures the actual execution. This is the most critical figure for determining the success of the supply chain.

Total WastageQuantifies "Leakage." In a PDS context, this identifies grain that was allocated but never reached the end consumer, signalling potential logistical issues, storage loss, or data reporting gaps.

Efficiency (%)Normalizes performance. It allows us to compare a small district with a large state fairly. An $85\%$ efficiency in a small district is objectively comparable to $85\%$ in a large state, even if the volumes differ

State RankGamifies performance. It automatically assigns a numerical rank to each state. If a user filters by "Wheat," the rank recalculates to show who the top wheat distributors are.

Average EfficiencyProvides a "Health Check" for a region. It calculates the mean performance across all sub-entities, helping to identify if a state's high volume is driven by just one good district or if performance is consistent across the board**.**

YTD DistributionTracks progress against annual goals. As the year progresses, this measure climbs, allowing officials to see if they are on track to meet their yearly distribution quotas.

Running Total (Monthly)Visualizes the  distribution over the months, making it easy to spot which months have the highest activity.

📈 Dashboard & Visualizations

TreemapMonthly performance distribution

Funnel ChartState ranking

Area ChartTrend analysis

Matrix TableDistrict-level details

Donut & Bar ChartsWastage analysis

KPI CardsKey metrics overview

💡 Key Insights

Performance Insights

High-performing districts achieve >95% efficiency

Low-performing districts fall below 70% efficiency

Active centers perform significantly better than inactive ones

Distribution Trends

Southern/Eastern regions prefer Rice

Northern regions prefer Wheat

Top districts contribute 40%+ of total distribution

Wastage Analysis

Gaps >10% indicate critical issues

Rural areas face logistical challenges

Zero distribution over time indicates high spoilage risk

📌 Conclusion

This project transforms raw PDS data into a powerful analytical solution.

It enables:

Improved supply chain efficiency

Reduced wastage

Better policy decision-making

Ultimately, it ensures that essential food resources reach the intended beneficiaries effectively and transparently.

📷 Dashboard Preview

(Add your Power BI screenshots here)

🚀 Author

Venkatesh VData Analyst | Excel | Power BI | SQL Enthusiast

⭐ If you found this project useful

Give it a ⭐ on GitHub and feel free to connect!

