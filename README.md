# LITA_CUSTOMERDATA_PROJECT

### Project Overview
This project involves analyzing customer data for a subscription service to identify segments and trends. 
### Goal
To understand customer behavior, track subscription types, and identify key trends in cancellations and renewals. 
### Task
---



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
