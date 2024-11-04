# LITA_CUSTOMERDATA_PROJECT

[Project Overview](#project-overview)

### Project Overview
This project focuses on analyzing customer data for a subscription service, aiming to provide insights into customer segments, subscription behaviors, and trends in cancellations and renewals. The analysis seeks to understand key customer patterns, such as churn rates, retention, and preferred subscription types, to aid in strategic decision-making and improve customer engagement.

The dataset contains detailed customer information, including subscription dates, types, revenue, and status (active or canceled). This data serves as the foundation for identifying trends and performing cohort analysis on customer retention and subscription lifecycle.

The project was executed using a blend of tools:

Excel for initial exploration, summary statistics, and pivot analysis to understand baseline patterns.

SQL to perform deeper queries, allowing for the extraction of targeted insights on customer behavior, revenue trends, and churn analysis.

Power BI to build a comprehensive dashboard that visualizes key metrics, customer segments, and interactive trends in cancellations and renewals.

### Goal
---

To understand customer behavior, track subscription types, and identify key trends in cancellations and renewals. 

### Objectives
---

- 1. Identify key customer segments based on subscription types and regions.

- 2. Analyze churn rates to understand patterns in cancellations and retention.

- 3. Visualize subscription trends to capture shifts in customer behavior over time.

### Key Metrics
---
- Total Customers
- Active vs. Churned Customers
- Subscription Trends
- Revenue by Subscription Type and Region
- Cohort Analysis


### Dataset Explanation
---

-  Customer ID: A unique identifier assigned to each customer in the dataset. This ensures that each customer is distinguishable from others, even if other details (like name or region) are similar.
  
 - Customer Name: The full name of each customer. This field helps in identifying individual customers and can be useful for personalized insights or reports.
   
- Region: The geographical area or location associated with each customer, such as East, West, North, or South. This information allows for regional analysis of customer trends, subscriptions, and revenue.
  
- Subscription Type: The category of subscription each customer has chosen, such as Basic, Premium, or Standard. This helps segment customers based on the level or type of service they’ve subscribed to.
  
- Subscription Start: The date on which each customer’s subscription began. It provides a starting point for tracking the length of the subscription and any subscription-related metrics.
  
- Subscription End: The date on which each customer’s subscription is set to end or has ended. It’s essential for calculating the subscription duration and determining if a customer has churned.
  
- Canceled: A status indicator (often a true/false or 0/1 value) showing whether a customer’s subscription was canceled before the subscription end date. This helps in identifying churned customers.
  
- Revenue: The amount of money generated from each customer’s subscription. This figure is crucial for analyzing revenue across various customer segments, regions, and subscription types.
  
- Month: The month of the subscription or activity, often extracted from the Subscription Start or Subscription End date. This field helps in analyzing monthly trends or grouping data by month.
  
- Subscription Duration: The total length of each customer’s subscription, calculated from Subscription Start to Subscription End. This is useful for cohort analysis and understanding customer retention.
  
- Year: The year of the subscription or activity, often extracted from the Subscription Start or Subscription End date. This field supports year-over-year trend analysis.

  ### Data Preparation
  ---

- Data was sourced from the learning management system (LMS) platform and downloaded as an Excel file for local access.

  Initial data preparation included verification of columns, handling missing values, and removing duplicates to bring the dataset into an analysis-ready state.

- Data explored to uncover trends, gain insights, and identify patterns that would inform further analysis.  Dataset was loaded and explored for initial checks, including verifying columns, handling missing values, and duplicates.
  
- After dataset was brought to analysis ready state it was analysed as required using excel formulars and pivot tables.
  
- The dataset was converted to a CSV file and imported into the SQL Server environment. This process allowed for the execution and validation of SQL queries to extract insights from the data, enabling a deeper analysis of customer behavior and subscription trends."

- The data was loaded into Power BI from the original Excel source file. After loading, the data was transformed to ensure accuracy and consistency, which included steps like handling missing values, correcting data types, and creating calculated columns and measures. This transformation enabled comprehensive analysis and effective visualization within the Power BI environment.

### Tasks
---

1. In Excel:

- Analyze customer data using pivot tables to find subscription patterns.
  
- Calculate the average subscription duration and identify the most popular 
subscription types.

2. In SQL:

Write queries to extract key insights.

3. Power BI: 
- Build a Power BI dashboard that visualizes key customer segments, 
cancellations, and subscription trends. Include slicers for interactive analysis.

### Analysis
---

# Excel Analysis

Subscription Patterns

![Screenshot (262)](https://github.com/user-attachments/assets/4c26d465-0112-4e5f-8992-64372fea33f7)


Summary of Subscription Data

1. East Region - Basic Subscription Type:

2022:

March: 169,000 subscribers

July: 1,714 subscribers

November: 1,718 subscribers


2023:

March: 1,666 subscribers (slight decrease from 2022)

July: 1,680 subscribers (slight increase from March 2023)

2. North Region - Basic Subscription Type:

2022:

January: 1,693 subscribers

May: 1,673 subscribers

September: 1,685 subscribers


2023:

January: 1,692 subscribers (consistent with the prior year)

May: 1,690 subscribers (marginal increase)




3. South Region - Premium Subscription Type:

2022:

February: 1,693 subscribers

June: 1,679 subscribers

October: 1,692 subscribers


2023:

February: 1,686 subscribers (slight decline)




4. West Region - Standard Subscription Type:

2022:

April: 1,662 subscribers

August: 1,676 subscribers

December: 1,700 subscribers


2023:

April: 1,687 subscribers (increase from prior year)

December: 1,695 subscribers (slight decrease from December 2022)





Key Insights and Observations

1. Stable Subscription Counts Across Regions and Subscription Types:

Across the regions, there are generally small fluctuations month-to-month and year-to-year. This consistency might suggest strong customer loyalty, with minor seasonal or monthly variations.



2. Marginal Declines in Certain Regions and Months:

For the East region (Basic), the March and July counts in 2023 are slightly lower than in 2022, indicating a minor decline in subscriber retention or acquisition.

In the South region (Premium), February 2023 shows a small decline compared to 2022. This could reflect a reduced appeal or shift in customer preferences for premium plans.



3. Higher Consistency in the North for Basic Subscriptions:

The North region shows very stable subscriber counts for the basic subscription between 2022 and 2023, with nearly identical numbers in January and only a slight increase in May. This stability might suggest a reliable customer base with a consistent preference for the basic plan.



4. Increased Subscription Counts in the West Region (Standard Subscription):

In the West region for the standard subscription, April and December 2023 show slight increases from 2022. This could point to a rising interest in the standard subscription in this region, possibly due to targeted promotions or improved satisfaction with the standard package.



5. Patterns in Monthly Subscription Uptake:

Each region appears to have specific months with higher subscriber counts, potentially influenced by regional or seasonal factors. For example:

Basic in the East and North shows a larger count in months like March and July for the East, and January for the North.

Premium in the South shows stable interest around February.

Standard in the West peaks around December, suggesting possible end-of-year promotions or renewals.




6. Potential Regional Preferences for Subscription Types:

The data suggests a clear regional preference:

East and North regions favor Basic subscriptions.

South favors Premium.

West leans towards Standard.


This trend could imply that different subscription tiers meet unique needs in each region. Further investigation could clarify whether factors like income levels, regional service availability, or targeted marketing campaigns contribute to these preferences



![Screenshot (254)](https://github.com/user-attachments/assets/f9c80c4d-5fc5-46b2-9f0a-75c22750c7b8)


**Observations on Revenue Consistency**

- Uniform Pricing and Customer Base: The revenue figures across regions are very close, which could indicate that each region has a similar-sized subscriber base and a uniform pricing structure for each subscription type. This implies that pricing and subscription adoption rates may be stable across
different regions, suggesting a successful standardization of the subscription model.

**Strong Revenue Performance from Regional Distribution**

Balanced Revenue Contributions: The fact that each subscription type in its respective region is generating similar revenue shows the company has successfully tailored or promoted these types to fit the preferences of each region. It reflects a good alignment between each subscription type and the unique customer demographics or needs of each region.


![Screenshot (253)](https://github.com/user-attachments/assets/547d3f3c-8c62-4d92-b3c9-4b32e71050f1)
 
- Limited Regional Variability in Spending: The small differences in revenue across regions imply minimal variation in customer spending behavior. This may indicate that the subscription appeal is consistent across these regions, with each region having a similar level of engagement and perceived value in the subscription offerings.

  ![Screenshot (259)](https://github.com/user-attachments/assets/1080d726-6aa4-4d65-9e8a-407411544c5f)

- Subscription Type Appeal: Since each region predominantly relies on a different subscription type but generates similar revenue, it could suggest that each subscription type is effectively priced to balance between value and revenue generation.
  
 For example:
Basic performs strongly in the East and North.
Premium is successful in the South.
Standard meets the needs of the West.

![Screenshot (260)](https://github.com/user-attachments/assets/671f2464-29ae-4b9e-8462-d402ff41bd09)

Revenue Parity Across Subscription Types

Basic’s Regional Split: While Basic has the highest total revenue, this is largely due to its presence in both the East and North. When we look at individual regions, the revenue from Basic in each region (East and North) is comparable to what Premium brings in from the South or what Standard brings in from the West. This suggests that the revenue generation per region is fairly balanced across all subscription types.

Average Subscription Duration

![Screenshot (244)](https://github.com/user-attachments/assets/10f4e2ad-3381-4ea3-bb45-17cdaea02a80)



![Screenshot (261)](https://github.com/user-attachments/assets/918a3145-1692-4f64-9e0c-4f2f98408a14)


Subscription Type Positioning

Basic as the Popular Option: Basic’s widespread use might be due to factors such as affordability, accessibility, or general feature appeal. If Basic is viewed as an entry-level option, its success across two regions may imply that there’s a strong customer base that prefers a simpler, cost-effective subscription.

Premium and Standard as Higher-Tier Options: Since Premium and Standard are available in only one region each but still generate revenue on par with Basic, it suggests they may be effectively positioned as higher-tier options with a more specific value proposition. This could appeal to customers looking for additional features or services.


![Screenshot (255)](https://github.com/user-attachments/assets/b8a30afd-30f7-4dbf-bd65-34d2a4dc4b8e)

1. Basic Subscription – East vs. North

No Cancellations in the East: The fact that there were zero cancellations for Basic in the East region suggests high customer satisfaction and loyalty. This could be attributed to:

Greater alignment with customer expectations: Customers in the East might feel that the Basic subscription meets their needs, reducing their likelihood to cancel.

Potential cultural or regional differences: There may be regional characteristics that make East customers more likely to retain their subscription. This could be due to economic factors, loyalty to the brand, or lesser exposure to competing services.

Service Quality or Customer Engagement: If there are differences in how services are delivered or promoted in the East (such as more effective customer support, tailored content, or local partnerships), this might contribute to higher retention for Basic users.


Significant Cancellations in the North: With 5,067 cancellations for Basic in the North, we see a stark contrast to the East. Possible reasons for this could be:

Unmet Expectations or Value Perception: Customers in the North may feel that the Basic tier lacks some features or benefits they value, leading to higher cancellations.

Competition or Alternative Options: The North region could have more exposure to competitors or alternative services, prompting users to switch or reconsider their subscription.

Demographic or Behavioral Differences: There may be demographic factors at play, such as a younger or more price-sensitive customer base in the North, that makes users more likely to cancel if they do not see immediate or consistent value.

2. Premium and Standard – South and West

Similar Cancellation Patterns: For Premium in the South and Standard in the West, cancellation patterns are quite similar, with a high number of cancellations (5,064 in the South and 5,044 in the West) relative to the non-cancellations.

Regional Preferences and Subscription Type Fit: This similarity suggests that while these tiers (Premium and Standard) may be popular, they may not fully meet customer expectations across both regions:

Feature Expectations vs. Pricing: The Premium subscribers in the South and Standard subscribers in the West might have high expectations in terms of features or benefits. If these expectations aren’t fully met, it could lead to cancellations.

Considerations for Retention Strategies: The company could explore whether adding tailored features, promotions, or discounts for these regions could improve retention rates.

Market Saturation or Churn Factors: If both regions have reached a market saturation point or if customers are quick to change services, it might reflect in high cancellation rates for these tiers.

1 retrieve the total number of customers from each region.

SELECT COUNT(CustomerName) AS Total_Customer, Region AS TotalPerRegion FROM [dbo].[CustomerDataProject]
GROUP BY Region

 Q2. find the most popular subscription type by the number of customers.

SELECT COUNT(CustomerName) AS Total_Customer, SubscriptionType AS Most_Popular FROM [dbo].[CustomerDataProject]
GROUP BY SubscriptionType
ORDER BY  Total_Customer DESC

Q3.  find customers who canceled their subscription within 6 months.
ALTER TABLE [dbo].[CustomerDataProject]
ADD Subscriptiondurationmonths Int

UPDATE [dbo].[CustomerDataProject]
SET Subscription_duration_months = DATEDIFF(month, SubscriptionStart, SubscriptionEnd)

SELECT COUNT(*) AS CUSTOMERWITHSHORTSUBSCRIPTIONS FROM [dbo].[CustomerDataProject]
WHERE SUBSCRIPTION_DURATION_MONTHS < 6

Q4 calculate the average subscription duration for all customers.

SELECT AVG(Subscription_duration_months) AS Averagesubscriptionduration FROM [dbo].[CustomerDataProject]

 5. find customers with subscriptions longer than 12 months. 

 SELECT CUSTOMERID, subscription_duration_months FROM [dbo].[CustomerDataProject]
 WHERE subscription_duration_months > 12

6. calculate total revenue by subscription type.

SELECT SubscriptionType, SUM(Revenue) AS Total_Revenue FROM [dbo].[CustomerDataProject]
GROUP BY SubscriptionType
ORDER BY Total_Revenue


7.find the top 3 regions by subscription cancellations. 

SELECT TOP 3
    Region, 
    COUNT(*) AS TotalCancellations
    FROM [dbo].[CustomerDataProject]
WHERE 
    Canceled = 1 
GROUP BY 
    Region
ORDER BY 
    TotalCancellations DESC 

8. find the total number of active and canceled subscriptions.


CUSTOMERS WITH LESS THAN 6 MONTHS CANCELLATIONS


TOTAL CANCELLATION

SELECT COUNT(*) AS CANCELEDSUBSCRIPTION FROM [dbo].[CustomerDataProject]
WHERE CANCELED =1
ACTIVE CUSTOMERS 
SELECT COUNT(*) AS ACTIVESUBSCRIPTION FROM [dbo].[CustomerDataProject]
WHERE CANCELED =0

### Key Insights and Recommendation

Maintaining High Retention in the East: With zero cancellations, the East is a model region for the Basic subscription. To maintain this, the company should:

Leverage What’s Working: Investigate what drives satisfaction in the East and look for ways to replicate this success in other regions.

Promote Regional Loyalty: Emphasizing regional loyalty programs or exclusive East-focused benefits could continue fostering the high retention rate here.


Customized Engagement for Premium and Standard in the South and West: For these higher tiers, the company could:

Focus on Added Value: Consider adding premium benefits or rewards for long-term subscribers in the South and West to make the subscription feel more valuable.

Address Potential Service Gaps: Ensure that the features and benefits of these subscription types align closely with customer expectations, possibly by introducing customizable options.

company could consider specific strategies to retain these users. This might include:

Adding Flexible Options: Introducing flexible plans, feature upgrades, or discount promotions could make the Basic subscription more appealing and reduce churn in the North.

Targeted Customer Feedback: Gathering feedback from North region customers who canceled could provide valuable insights into unmet needs or areas for improvement in the Basic subscription.



