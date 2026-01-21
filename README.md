# 📊 Meta Ads Performance Analysis Dashboard
## 1. Project Overview

This project analyzes the performance of paid advertising campaigns on Facebook and Instagram (Meta Ads).
The dashboard provides insights into reach, engagement, conversions, and budget efficiency, helping marketing teams evaluate campaign effectiveness and optimize advertising strategies.

The project is designed end-to-end, from business requirements definition to data modeling, dashboard building, and insight generation using Power BI.

## 2. Business Objective

### The primary goal of this project is to build a performance tracking dashboard that enables marketing stakeholders to:

  - Monitor campaign reach and engagement

  - Measure conversion effectiveness and ROI

  - Identify high-performing platforms, audiences, and ad formats

  - Optimize budget allocation and campaign scheduling

### Scope

In scope

  - Paid advertising campaigns on Facebook and Instagram

Out of scope

  - Messenger, Audience Network

  - Organic (non-paid) engagement

## 3. Dataset & Domain Knowledge

The dataset is adapted from the Kaggle dataset “Social Media Advertisement Performance”, modeled after how Meta Ads platforms (Facebook & Instagram) capture data.

### Key KPIs Supported

  - Impressions

  - Clicks

  - Purchases (Conversions)

  - Engagements (Clicks + Shares + Comments)

  - CTR, Engagement Rate

  - Conversion Rate, Purchase Rate

  - Budget-based metrics (CPC, CPM, ROAS)

The dataset is suitable for analyzing:

  - Campaign performance

  - Audience demographics & interests

  - Funnel efficiency from awareness → conversion

## 4. Data Model

The data follows a Star Schema design:

### Fact Table

  - fact_ad_events

    + Event-level data (Impression, Click, Share, Comment, Purchase)

    + Used to calculate all KPIs

### Dimension Tables

  - dim_users: demographics, country, interests

  - dim_ads: platform, ad type, targeting attributes

  - dim_campaigns: campaign duration and budget

  - dim_date: time-based analysis (created in Power BI)

This model enables efficient slicing by:

  - Time

  - Geography

  - Platform

  - Audience segments

  - Ad formats

## 5. Data Processing

  - Data cleaning and transformation performed using Python

  - Duplicate records handled at user and event level

  - Age grouped into business-friendly age buckets

  - Final datasets exported as CSV files and loaded into Power BI

## 6. Dashboard Design & Visualizations

The Power BI dashboard was built strictly based on the Business Requirements Document (BRD).

### Key Visuals

  - KPI Cards: Impressions, Clicks, Purchases, CTR, Conversion Rate

  - Gender Distribution (Donut Chart)

  - Target Age Group Analysis (Bar Chart)

  - Country Performance Map

  - Calendar Heatmap (Monthly engagement)

  - Weekly Trend by Ad Type (Stacked Column)

  - Hourly Engagement Trend (Area Chart)

  - Ad Type Performance Matrix

### Dashboard Overview
<img width="1852" height="1059" alt="Overview Analysis" src="https://github.com/user-attachments/assets/46a3753a-d16a-4abb-99f9-ccfc39d067fb" />

### Facebook Ads Dashboard
<img width="2193" height="1256" alt="Facebook Ads" src="https://github.com/user-attachments/assets/08a79e36-e326-462e-aabb-81cc884a354b" />

### Instagram Ads Dashboard
<img width="2187" height="1251" alt="Instagram Ads" src="https://github.com/user-attachments/assets/0414a08c-9b7e-4d7d-b869-532745383acf" />

## 7. Key Insights
### Funnel Performance

  - High CTR (11.48%) & Engagement Rate (13.27%) indicate strong ad creatives and messaging.
  - Low Purchase Rate (0.60%) reveals inefficiency at the lower funnel.
    
  => Awareness is strong, but conversion needs optimization.

### Audience Insights

  - Females contribute the highest engagement.

  - Strongest engagement from users aged 18–30.
  
  => Core target audience: young adults, especially females.

### Geographic Insights

  - High engagement volume: US, UK, India

  - Better conversion potential: Japan, Mexico
  
  => Combine volume-driven markets with premium conversion-focused campaigns.

### Time-Based Insights

  - Engagement peaks during noon and evening hours (12–13, 18–21).

  - Stable weekly trends with campaign-driven spikes.
  
  => Schedule ads during peak hours and promotional periods.

### Ad Format Performance

  - Video ads perform best overall (highest CTR, ER, CR).

  - Stories ads show strong reach and engagement.
  
  => Allocate more budget to Video and Stories formats.

## 8. Tools & Technologies

  - Python (Pandas) – data processing

  - Power BI Desktop & Power BI Service – visualization

  - Git & GitHub – version control

  - CSV-based data pipeline

## 9. Project Structure
  - data/

    + raw/: Stores raw advertising data (CSV/SQLite) directly collected from the source.

    + processed/: Contains cleaned and transformed data used for analysis and dashboards.

  - notebooks/
    + 01_data_overview: Initial data exploration and data understanding.
    + 02_data_modeling: Data cleaning, transformation, and KPI preparation.

  - dashboard/

    + Meta marketing performance analysis.pbix: Main Power BI file for analyzing Meta (Facebook & Instagram) ad performance.

    + images/: Stores dashboard screenshots for documentation and reporting.

      + Dasboard_Overview.png: Overall performance dashboard images.
      + Facebook_Ads.png: Facebook Platform analysis images.
      + Instagram_Ads.png: Instagram Platform analysis images.

  - docs/

    + BRD_Meta_Ads_Performance.pdf: Business Requirements Document defining objectives, scope, and KPIs.

    + Domain_Knowledge.pdf: Business and marketing domain knowledge.

  - report/

    + Dashboard_Insights.pdf: Final insight report generated from the dashboard.

  - README.md: 
    Project overview, structure, and usage instructions.

## 10. Business Value

This dashboard enables marketing teams to:

  - Make data-driven budget decisions

  - Improve conversion funnel efficiency

  - Identify high-potential audiences and markets

  - Optimize campaign timing and creative formats

## 11. Future Improvements

  - Add ROAS & cost-based KPIs

  - Drill-through analysis by campaign

  - A/B testing comparison dashboard

  - Automated data refresh pipeline
