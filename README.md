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

By understanding these preferences, we can more effectively target the **Mainstream - Young Singles/Couples** segment, optimizing product offerings to align with their purchasing habits and drive both retention
and growth in sales. The Category Manager should consider boosting the category’s performance by strategically placing Tyrrells and smaller packs of chips in high-traffic, discretionary spaces near areas frequented by young singles and couples. This placement would enhance visibility and encourage impulse purchases, potentially driving increased sales in these segments.

# Task 2: Experimentation and Uplift Testing
Extend the analysis from Task 1 to help you identify the control stores that allow you to test the impact of trial stores on sales.

**Information about the task**
The category manager asked us to evaluate the performance of a trial which was performed in stores with numbers 77,86 and 88.
This can be broken down by:
  1. Total Sales Revenue.
  2. Total number of customers.
  3. Average number of transactions per customer.

Develop a measure to compare different control stores to each trial store, reducing the need to repeat the analysis for every trial store. Consider creating a reusable function that calculates this measure. You can use metrics like Pearson correlations or a magnitude distance metric, such as 1 - (Observed distance - minimum distance)/(Maximum distance - minimum distance). Once the control stores are identified, compare the performance of each trial and control pair during the trial period. Test whether total sales during the trial period significantly differ between the trial and control stores. If significant differences are observed, further analyze the drivers of the change, such as:
1. An increase in purchasing customers, or
2. An increase in the number of purchases per customer.
This approach ensures a systematic and repeatable method for analyzing trial and control store relationships.

**Main areas of Focus are**
1. Select control stores- Explore data, define metrics, visualize graphs.
2. Assessment of the trial - Insights/trends by comparing trial stores with control stores.
3. Collate findings - Summarize and provide recommendations.

**Experimenting and Testing**
1. Total Sales (tot_sales)
2. Unique no. of customers (no.of.customers)
3. Transaction per customer (no.of.transactions)
4. Chips per transaction (chips.per.transaction)
5. Average chip price (avg.chip.price)

Step 1: Filter stores with a full 12-month observation period and select data for the pre-trial period.

Step 2: Define a function **calCorrelation** to calculate the correlation between a specific store and other stores for a given metric. Loop through each store to compute pairwise correlations and return a data table with the store pair and correlation values.

Step 3: Define a function **calculateMagnitudeDistance** to compute the magnitude distance between a specific store and others for a selected metric. For each store comparison, calculate the absolute difference in the metric and normalize it between 0 and 1, representing the magnitude distance. Return the mean magnitude measure for each store pair.

Step 4: A trial store number 77 is selected for the analysis. Correlation is calculated for sales and customer numbers between the trial store and other stores. The magnitude distance between the trial store and control store is computed for both sales and customers.

Step 5: Correlation and magnitude distance scores are merged to create a combined score for sales and customer metrics. A final score is computed based on the sales and customer scores, which helps in identifying the control store.

Step 6: The store with the highest score is selected as the control store. We need to plot the sales and customer data to assess the pre-trial similarity between the trial and the control store. 

Step 7: We need to calculate a scaling factor to adjust the control store's sales and customer data to match the trial store's data. The percentage difference between the scaled control store data and the trial store data are calculated and tested against a null hypothesis. 

Step 8: We test the null hypothesis to determine whether the trial store's sales and customer metrics are significantly different from the control store's performance. 

Step 9: The control store's sales and customer data are adjusted to represent the 95th and 5th percentile for comparison. Then, the results are plotted to access the trial store's performance relative to control store's confidence interval.

Step 10: Repeat the steps to find the control stores for stores 86 and 88 and compare them to sales and customer data of the control stores to assess any significant performance differences.


### Insights and trends
1. Trial Store 77: Control Store 233
2. Trial Store 86: Control Store 155
3. Trial Store 88: Control Store 40
4. Both trial stores 77 and 86 showed a significant increase in total sales and number of customers in at least 2 of the 3 trial months but this was not the case for trial store 86. We can check that if the implementation of the trial was different in the trial store 86.
5. But overall the trial showed positive significant result.

# Task 3: Analytics and Commercial Application**

## **Project Overview**

In the final stage of the **Quantium Data Analytics Virtual Experience Program**, the insights and analytics from **Task 1: Data Preparation and Customer Analytics** and **Task 2: Experimentation and Uplift Testing** were used to prepare a comprehensive report for **Julia**, the Category Manager. This report was aimed at providing actionable insights and strategic recommendations for the next half-year plan, based on the analysis of customer behavior and sales trends.

## **Objective**

The objective of **Task 3** was to deliver insights that would guide the Category Manager in making data-driven decisions for future retail strategies, enabling them to optimize performance across stores and better understand customer purchasing behaviors.

## **Pyramid Principle Framework**

As best practice at Quantium, we used the **Pyramid Principle Framework** to organize the report. This framework ensures clarity and conciseness in presenting data insights and recommendations. The framework focuses on providing the most important information first, followed by supporting data and analysis.

## **Report Structure**

The report was structured as follows:

1. **Executive Summary**: A high-level overview of the key findings and recommendations.
2. **Problem Statement / Purpose**: Clearly defined objectives of the analysis.
3. **Data Insights**:
   - **Customer Segmentation Analysis**: Insights into customer segments and their purchasing patterns.
   - **Trial Store vs. Control Store Analysis**: Comparative analysis of sales and customer engagement between trial and control stores.
4. **Key Insights**:
   - **High-Contributing Segments**: Identification of key customer segments, such as **Mainstream - Young Singles/Couples**, which significantly contribute to sales.
   - **Impulsive Purchasers**: Insights into segments willing to pay a premium for products like **Tyrrells**.
5. **Recommendations & Next Steps**:
   - **Optimizing Product Placement**: Strategic placement of products to enhance sales in key segments.
   - **Trial Store Performance Analysis**: Suggestions to improve the performance of trial stores based on data findings.

## **Final Deliverable**

The final deliverable was a **PowerPoint presentation** which included:
- A **clear agenda** to guide the presentation.
- **Easy-to-understand visualizations** to illustrate key data insights.
- **Actionable recommendations** for optimizing retail strategy and improving performance.
- **Next steps** to ensure the long-term success and effectiveness of future strategies.

## **Next Steps / Summary**

- Ensure that the recommendations are implemented in the upcoming strategic plans for the next half year.
- Monitor the effectiveness of trial store strategies and product placements to fine-tune future actions.
- Continue analyzing customer behavior to further refine marketing and sales strategies.

## **Conclusion**

By following best practices in data presentation and communication, the report provided **Julia**, the Category Manager, with valuable insights and actionable recommendations. The data-driven approach allowed her to effectively plan for the next half-year, optimizing store layouts, product placements, and customer engagement strategies to maximize sales and improve customer satisfaction.







