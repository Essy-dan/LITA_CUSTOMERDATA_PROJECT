# LITA_CUSTOMERDATA_PROJECT

### Project Overview
This project involves analyzing customer data for a subscription service to identify 
segments and trends. 
### Goal
To understand customer behavior, track subscription types, and identify key trends in cancellations and renewals. The final deliverable is a Power BI 
dashboard that presents your analysis.



















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
