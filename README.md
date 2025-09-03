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
                  




