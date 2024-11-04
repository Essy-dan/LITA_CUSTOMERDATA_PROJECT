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

![Screenshot (247)](https://github.com/user-attachments/assets/912f2063-9213-4e3c-94aa-2cd7da5dfcb1)


The pivot table "Subscription Patterns" provides an overview of revenue and customer counts across different regions (East, North, South, and West) and Subcription type for 2022 and the first eight months of 2023. Similar trend is observed across in revenue generated, customer count and subscription type. Aside from Basic subscription type which generated more revenue and and has has more customer base, reason b![Screenshot (247)](https://github.com/user-attachments/assets/03fc7554-90f5-40cb-9604-bfe765e34870)
eing that it was utilized in two regions, the trend would still be similar if treated individually.  

Key Insights:
Revenue by Region
Similar revenue pattern across regions, approximately #16.8 - #16.9 total revenue per Region for the period under review.

Total Revenue:
2022:
2023 (Jan-Aug)
Customer Count by Region and Month:
2022: Steady at 3,750 customers per region each month.
2023: Consistent at 3,750 customers per region each month.
Total Customer Count:
2022: 
2023 (Jan-Aug): 
Regional Performance:
South and West regions lead in revenue.
East and North regions slightly lower but show stable performance.
Overall Trends:
Stable subscription patterns with low churn.

Opportunities for growth in East and North regions.





![Screenshot (224)](https://github.com/user-attachments/assets/0b7a9b86-3290-49b2-8c3f-6bd122d0c8e0)

The most popular subscription type was seen to be Basic which was utilized in the East and the North regions.  and the avearge subscription months was seen to be 12 months. 














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




Insights:
Basic Subscription:

Generates the highest revenue.
The East region has the highest active subscriptions and no cancellations.
North region has a significant number of cancellations, though using the same subscription type as the East region. 
Premiun and Standard subscription type display similar performance in terms of active and cancelled subscriptions.
The South and West regions have consistent active and cancelled subscriptions.
Revenue Trends: All the four regions has similar revenue contribution for the period under review. 

North region shows fluctuating revenue with high cancellations in May.
South region exhibits steady growth followed by a decline.
West region has consistent revenue with a decline in August.
Recommendations:
Study the East Region:
Investigate factors contributing to high active subscriptions and zero cancellations. Implement successful strategies from the East region in other regions.
Analyze Cancellation Reasons:
Conduct a thorough analysis of the reasons behind the consistent cancellation numbers in the North, South, and West regions. Utilize insights to enhance customer retention strategies.
Optimize Subscription Types:
Promote and optimize Basic subscriptions across other regions, given its superior performance in revenue generation.
Enhance Revenue Stability:
Examine revenue fluctuations in the North, South, and West regions to identify and address causes of decline.
Utilize Cohort Analysis:
Leverage cohort month data to track and improve customer retention, focusing on identified churned months.
Conclusion
The Customer Subscription Analysis project, encompassing Excel, SQL, and Power BI, has provided a comprehensive view of subscription performance.



Basic subscriptions generated the highest revenue. The East region had the highest active subscriptions with no cancellations. North, South, and West regions had similar active subscriptions but high cancellations. Identified peak churn months varied by region. The project revealed that the East region's practices could be a model for success in other regions. There is a need to develop targeted retention strategies for regions with high cancellations. Promoting Basic subscriptions while enhancing Premium and Standard offerings can balance revenue streams. Leveraging cohort analysis will help anticipate and mitigate churn, ensuring proactive customer retention. Cuold it be that telecomunication company is situatedin the East and thus enhance her effectiveness, then the company should think of increasing infra-structures in other regions to enhance her customer retention and thus increase revenue. 

Overall, the integrated approach has provided actionable intelligence for optimizing subscription performance, enhancing customer retention, and maximizing revenue across all regions and subscription types.
