  #  DIGITAL MARKETING CAMPAIGN PROJECT ANALYSIS REPORT(POWER BI)
## Introduction
This report analyzes digital marketing campaign data using a Power BI dataset. The objective is to evaluate channel effectiveness, product performance, and campaign efficiency, while recommending actionable strategies to improve ROI and revenue growth.
## Data Source
•	File Used: PBI_Marketing_Data.xlsx( shared from Aixa Africa cohort 8 Data Analytics)
•	Records: 1,000 campaign entries.
•	Columns Include: Campaign ID, Product Name, Category, Ad Spend, Impressions, Clicks, Conversions, Revenue, ROI, Campaign Date, Marketing Channel.
## Problem Statement
Digital marketing teams invest across multiple platforms (Google Ads, Email, Instagram, Influencer, Referrals). However:
•	ROI varies significantly across channels.
•	Some campaigns consume budget but fail to convert.
•	Product categories do not perform equally.
The challenge is to identify where money should go for maximum returns and how to optimize underperforming areas.
## Pre-Analysis Questions
Before analysis, the following  questions were defined:
1.	Which channels deliver the highest ROI and revenue efficiency?
2.	Which products and categories drive the most revenue vs. the highest ROI?
3.	How do ad spend, clicks, and conversions correlate over time?
4.	What are the seasonal trends (Nov 2024 – Feb 2025)?
5.	Are there cost inefficiencies in CPC (Cost per Conversion) or CTR (Click-Through Rate)?
## Data Cleaning & Preparation
 The cleaning was performed in Power BI 
•	Removed Missing Values: Dataset had no nulls or duplicate values
•	Converted Date: Campaign Date formatted to Date for time series.
•	Calculated Columns/Measures (DAX Functions):
o	CTR (Click Through Rate):
o	CTR = DIVIDE (SUM (marketing [Clicks], SUM (marketing [Impressions]), 0)
o	Conversion Rate (CR):
o	Conversion Rate = DIVIDE (SUM (marketing [Conversions], SUM (marketing [Clicks]), 0)
o	Cost per Conversion (CPC):
o	CPC = DIVIDE (SUM (marketing [Ad Spend (INR)], SUM (marketing [Conversions]), 0)
o	ROI (%):
o	ROI = DIVIDE (SUM (marketing [Revenue (INR)] -SUM (marketing [Ad Spend (INR)]), SUM (marketing [Ad Spend (INR)], 0) * 1000
o	ROAS (Return on Ad Spend):
o	ROAS = DIVIDE (SUM (marketing [Revenue (INR)], SUM (marketing [Ad Spend (INR)], 0)
o	CPM (Cost Per Mille):
o	CPM=DIVIDE (SUM (marketing [Ad Spend (INR)]), SUM (marketing [Impressions]),0)*1000
o	Total Revenue = SUM (marketing [Revenue (INR)])
•	Outliers in ROI checked, some campaigns with very high returns were retained as genuine cases (low-cost but high-conversion campaigns).
    ##  Insights & Findings
    ## Overall Performance (Dashboard KPIs)
•	Impressions: 242M
•	Clicks: 12M (CTR = 5.09%, healthy engagement).
•	Conversions: 1M (CR = 9.81%, strong conversion rate).
•	Ad Spend: ₦2.42M vs Revenue: ₦344M.
•	ROI: ₦142 for every ₦1 spent.
•	ROAS: ₦143.
 Campaigns overall were highly profitable.
   ## Ad Spend by Marketing Channel
•	Distribution: Google Ads (21.94%), Referral (21.38%), Email (19.06%), Instagram Ads (18.96%), Influencer Marketing (18.68%).
•	Finding: Spend was spread evenly, but ROI differed.
•	Insight: Influencer and Instagram performed best in conversions, while Email gave reach but weaker returns.
  ## Impressions vs Clicks 
•	Nov 2024: Impressions = 49M, Clicks = 2M.
•	Dec 2024: Still Strong at Impressions  78M, Clicks 4.1M.
•	Jan 2025: Impressions peaked at 91M, 4.7M clicks.
•	Feb 2025: Dropped significantly at 25M impressions,1.3M clicks.
•	Finding: December and January were peak campaign months.
•	Insight: Seasonality (holidays) drives engagement, more budget should be allocated in Nov–Jan.
 ## Conversion Rate & CPM by Category
•	Household: CR ~1010%, CPM ₦10.
•	Groceries: CR ~986%.
•	Beverages: CR ~1029%.
•	Personal Care: CR ~1049% (high cost, low return).
•	Snacks: CR ~960%.
•	Finding: Household & Beverages efficient; Personal Care overspends for lower ROI.
•	Insight: Shift spending away from Personal Care campaigns.
 ## Revenue by Product
•	Top Revenue Drivers: Cold Drink (₦19.1M), Biscuits (₦19.0M), Dishwasher Liquid, Air Freshener, Cooking Oil (all >₦18M).
•	Finding: Snacks & Beverages dominate sales volume.
•	Insight: Focus campaigns on top-sellers but diversify into high-ROI everyday items.
 6 Ad Spend vs Conversion Over Time
•	Dec 2024 & Jan 2025: High spend aligned with high conversions.
•	Feb 2025: Spend dropped — conversions dropped too.
•	Finding: Positive correlation between spend and conversions.
•	Insight: Controlled spend in low-demand months avoids waste.
 ## ROI (%) by Product
•	Air Freshener: ₦259
•	Eggs: ₦241
•	Biscuits: ₦194
•	Shampoo: ₦179
•	Rice: ₦171
•	Finding: Some low-cost daily products gave the highest ROI despite not being top in revenue.
•	Insight: High-ROI “everyday goods” should get more attention in campaigns.
 ## Ad Spend & Revenue Over Time
•	Revenue peaked at ₦128M (Jan 2025), ₦119M (Dec 2024).
•	Spend remained below ₦1M in those months.
•	Finding: Revenue growth far exceeded spend growth.
•	Insight: Campaign efficiency improves with scale during the festive season.
 ## Ad Clicks and ROI Over Time
•	Dec 2024 and Jan 2025 have the highest clicks at 4.1M, ROI 128 (Dec 2024), and clicks at 4.7M, ROI 149 (Jan 2025) 
•	Nov 2024 and Feb 2025 with low clicks and ROI
•	Findings: Dec 2024 showing a strong balance between engagement and returns, and Jan 2025 performing better than  all other months
•	Insight: festive season again wins with (Dec–Jan) drives both higher engagement and stronger ROI, confirming it to be the most profitable period for campaigns.
## Ad Clicks and ROI Over Time
•	Dec 2024 and Jan 2025 have the highest clicks at 4.1M, ROI 128 (Dec 2024), and clicks at 4.7M, ROI 149 (Jan 2025) 
•	Nov 2024 and Feb 2025 with low clicks and ROI
•	Findings: Dec 2024 showing a strong balance between engagement and returns, and Jan 2025 performing better than  all other months
•	Insight: festive season again wins with (Dec–Jan) drives both higher engagement and stronger ROI, confirming it to be the most profitable period for campaigns.
## Recommendations
 Channel Optimization: Increase investment in Influencer and Instagram; reduce budget for underperforming Email campaigns.
 Category Focus: Push campaigns for Beverages, Snacks, Household essentials; cut back on Personal Care.
 Seasonal: Plan budgets around Nov–Jan festive peaks for maximum ROI.
 Product Strategy: Promote everyday high-ROI products (Air Freshener, Eggs, Biscuits).
 Efficiency Tracking: Regularly monitor CTR, CR, and CPC for early detection of underperforming campaigns.
## Conclusion
The campaigns were highly successful, generating massive ROI (₦142 per ₦1 spent). However, results were uneven across channels and categories. By reallocating budget to high-performing products and channels, and aligning campaign spend with seasonal demand, the business can unlock even higher revenue and efficiency in the next campaign cycle.

## DM Campaign Analysis Dashboard
"C:\Users\HP\Downloads\DM Campaign Analysis Dashboard 2.pdf"




