# Quantium- Data Analytics Virtual Experience Program.
This repository contains the analysis and insights generated from the Quantium Data Analytics Virtual Experience Program. Using R Programming, this project dives into customer behaviour, sales trends, and market insights to help optimize retail strategies. 

# Project Overview
This experience program focused on analyzing chip purchases in retail giants to better understand customer buying behaviours. The objective was to analyze the customer purchasing behaviours and assess the impact of a new store layout implemented in trial stores. The objective was to deliver valuable insights into the preferences of the customer and determine the success of the trial, providing data-driven recommendations to the client.

# Task 1: Data Preparation and Customer Analytics

## Data Preparation

In Task 1, the focus was on analyzing customer behavior related to chips purchases. The following data-cleaning steps were performed:

- **Standardization**: Column names were standardized, and date values were reformatted for consistency.
- **Data Filtering**: Entries related to salsa products were excluded from the dataset.
- **Outlier Removal**: Outliers were identified and removed to ensure data accuracy.
- **Brand Name Correction**: A new column, **"Brand,"** was added, derived from the `prod_name` field. Inconsistencies in brand names were corrected, merging pairs like **"Snbts"** to **"Sunbites"** and **"Infzns"** to **"Infuzions"**.

## Customer Segmentation Analysis

The analysis aimed to answer the following key questions about customer segments:

### 1. Who spends the most on chips?

The analysis examined customer behavior by life stage and premium purchase status. It was found that **Mainstream - Young Singles/Couples** and **Mainstream - Retirees** contribute the most to sales, primarily due to the high number of unique customers in these segments. On the other hand, the **Budget - Older Families** segment, despite having a high frequency of purchases, did not contribute as significantly to total sales.

### 2. How many customers are in each segment?

This analysis provided insights into the distribution of customers across various segments, highlighting the size and purchasing habits of each.

### 3. How many chips are purchased per customer by segment?

A detailed examination of purchase volumes showed varying patterns across segments, with some groups purchasing more chips than others.

### 4. What’s the average chip price by customer segment?

The average price per unit was higher for **Mainstream - Young and Mid-Age Singles and Couples** compared to **Budget** and **Premium** counterparts. This suggests that these customers are willing to pay more per packet of chips.

## Statistical Analysis of Price Differences

To further validate the findings regarding price differences, a **t-test** was conducted to compare the average unit prices between the **Mainstream - Young and Mid-Age Singles and Couples** segment and the **Budget** and **Premium - Young and Mid-Age Singles and Couples** segments. The t-test results indicated a **p-value < 2.2e-16**, confirming that the unit price for the **Mainstream** segment is statistically significantly higher than for the other segments. This reinforces the observation that **Mainstream** customers are more willing to pay a premium for chips compared to those in the **Budget** or **Premium** segments.


# Customer Segment Analysis: Mainstream - Young Singles/Couples

To retain and further increase sales from high-contributing customer segments, we conducted an in-depth analysis of the **Mainstream - Young Singles/Couples** segment. The aim was to identify whether this segment shows a preference for specific chip brands or pack sizes. The key findings are as follows:

### Key Findings

- **Tyrrells Preference**: Customers in the **Mainstream - Young Singles/Couples** segment are **23% more likely** to purchase **Tyrrells** chips compared to the rest of the population.
- **Burger Rings Disinterest**: This segment is **56% less likely** to purchase **Burger Rings** compared to other customer groups.
- **Pack Size Preference**: Customers in this segment are **27% more likely** to purchase a **270g pack** of chips. Since **Twisties** is the only brand offering 270g packs, this indicates a higher likelihood of purchasing **Twisties** among this segment.

### Impulsive Purchasing Behavior

Additionally, **Mainstream - Young Singles/Couples** customers tend to pay more per packet of chips, reflecting more impulsive purchasing behavior. Their increased willingness to spend aligns with their higher likelihood of purchasing **Tyrrells** chips, which is **23% greater** than the general population.

### Recommendation

By understanding these preferences, we can more effectively target the **Mainstream - Young Singles/Couples** segment, optimizing product offerings to align with their purchasing habits and drive both retention and growth in sales. The Category Manager may consider boosting the category’s performance by strategically placing Tyrrells and smaller packs of chips in high-traffic, discretionary spaces near areas frequented by young singles and couples. This placement would enhance visibility and encourage impulse purchases, potentially driving increased sales in these segments.

