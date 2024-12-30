# Quantium- Data Analytics Virtual Experience Program.
This repository contains the analysis and insights generated from the Quantium Data Analytics Virtual Experience Program. Using R Programming, this project dives into customer behaviour, sales trends, and market insights to help optimize retail strategies. 

# Project Overview
This experience program focused on analyzing chip purchases in retail giants to better understand customer buying behaviours. The objective was to analyze the customer purchasing behaviours and assess the impact of a new store layout implemented in trial stores. The objective was to deliver valuable insights into the preferences of the customer and determine the success of the trial, providing data-driven recommendations to the client.

# Task 1- Data Preparation and Customer Analytics
In Task 1, the focus was on analyzing customer behavior about chips purchases. The following data-cleaning steps were undertaken:
* Standardization: Column names were standardized, and date values were reformatted for consistency.
* Data Filtering: Entries related to salsa products were excluded from the dataset.
* Outlier Removal: Outliers were identified and removed to ensure data accuracy.
* Brand Name Correction: A new column, "Brand," was added, derived from the prod_name field. Inconsistencies in brand names were corrected, merging pairs like "Snbts" to "Sunbites" and "Infzns" to "Infuzions".
  
* Customer Segmentation Analysis.
The analysis aimed to answer four key questions about customer segments:

1. Who spends the most on chips?
The analysis examined customer behavior by life stage and premium purchase status. It was found that Mainstream - young singles/couples and Mainstream - retirees contribute the most to sales, primarily due to the high number of unique customers in these segments. On the other hand, the Budget - older families segment, despite having a high frequency of purchases, did not contribute as significantly to total sales.

2. How many customers are in each segment?
This analysis provided insights into the distribution of customers across various segments, highlighting the size and purchasing habits of each.

3. How many chips are purchased per customer by segment?
A detailed examination of purchase volumes showed varying patterns across the segments, with some groups purchasing more chips than others.

4. What’s the average chip price by customer segment?
The average price per unit was higher for Mainstream - young and mid-age singles and couples compared to Budget and Premium counterparts. This suggests that these customers are willing to pay more per packet of chips.

* Statistical Analysis of Price Differences
To further validate the findings regarding price differences, a t-test was conducted to compare the average unit prices between the Mainstream - young and mid-age singles and couples segment and the Budget and Premium - young and mid-age singles and couples segments. The t-test results indicated a p-value < 2.2e-16, which confirms that the unit price for the Mainstream segment is statistically significantly higher than for the other segments. This reinforces the observation that Mainstream customers are more willing to pay a premium for chips compared to those in the Budget or Premium segments.

# Deep dive into specific customer segments for insights 
We wanted to target customer segments that contribute the most to sales to retain them or further increase sales. For that we took a deeper look at Mainstream- Young Singles/Couples. 

