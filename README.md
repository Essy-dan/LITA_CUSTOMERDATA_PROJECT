# LITA_CUSTOMERDATA_PROJECT

[Project Overview](#project-overview)

[Goal](#goal)

[Objective](objective)

[Key Metrics](#key-metrics)

[Dataset Explanation](#dataset-explanation)

[Data Preparation](#data-preparation)

[Tasks](#tasks)

[Analysis and Discussion](#analysis-and-discussion)

[Interactive Dashboard](#interactive-dashboard)

[Key Insights and Recommendations](#key-insight-and-recommenadtion)

[Conclusion](#conclusion)

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

### Analysis and Discussion
---

# Excel Analysis

Subscription Patterns

![Screenshot (262)](https://github.com/user-attachments/assets/4c26d465-0112-4e5f-8992-64372fea33f7)


Summary of Subscription Data

1. East Region - Basic Subscription Type:

2022:

March: 1,690 subscribers

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

**Key Insights and Observations**

1. Stable Subscription Counts Across Regions and Subscription Types:

Across the regions, there are generally small fluctuations month-to-month and year-to-year. This consistency might suggest strong customer loyalty, with minor seasonal or monthly variations.

2. Marginal Declines in Certain Regions and Months:

For the East region (Basic), March and July counts in 2023 are slightly lower than in 2022, indicating a minor decline in subscriber retention or acquisition.

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

**Revenue Parity Across Subscription Types**

Basic’s Regional Split: While Basic has the highest total revenue, this is largely due to its presence in both the East and North. When we look at individual regions, the revenue from Basic in each region (East and North) is comparable to what Premium brings in from the South or what Standard brings in from the West. This suggests that the revenue generation per region is fairly balanced across all subscription types.

**Average Subscription Duration**

![Screenshot (244)](https://github.com/user-attachments/assets/10f4e2ad-3381-4ea3-bb45-17cdaea02a80)

1. Consistency in Average Subscription Duration

Uniform Subscription Duration: The fact that the average subscription duration is 12 months across all subscription types suggests that customers generally maintain their subscriptions for a full year regardless of tier. This could indicate:

Satisfaction with Annual Commitments: The 12-month average could mean that customers find value in the company’s offerings and are willing to commit annually, likely due to cost-effectiveness or perceived benefits.

Alignment with Pricing Model: If subscriptions are primarily structured on an annual basis, customers may naturally renew for the full year. This may reflect a successful pricing model that encourages sustained engagement.

Potential for Long-Term Retention: With the majority of subscribers maintaining this duration, the company could focus on strategies to encourage renewals, potentially increasing lifetime value by promoting benefits of multi-year commitments or providing renewal incentives.

2. Popularity of the Basic Subscription Type

Broad Appeal of Basic Subscription: Basic’s popularity in both the East and North regions might indicate that a larger segment of customers prioritizes affordability or simplicity in their subscriptions, making Basic an accessible and attractive option.

Lower Price Sensitivity Regions: Since Basic is most utilized in the East and North, these regions might represent areas where customers are more price-sensitive, favoring lower-tier plans. Alternatively, it could suggest that the majority of users in these regions primarily seek essential features or are in the early stages of engagement with the company's offerings.

Opportunities for Upselling: Basic’s popularity implies that there may be room to introduce tailored features or minor upgrades to encourage customers to consider moving to a higher tier. For instance, offering limited-time discounts on upgrades or showcasing added benefits of Premium might appeal to Basic subscribers in the East and North.

3. Geographic Distribution of Subscription Types

Distinct Regional Preferences: Each subscription type’s unique regional popularity — with Basic in the East and North, Premium in the South, and Standard in the West — suggests regional variances in customer preferences and spending patterns.

Premium in the South: Premium’s prominence in the South might reflect a customer base willing to invest in higher-tier services, possibly due to higher spending power or demand for enhanced features. The company could leverage this by offering exclusive, region-specific benefits or bundles to retain and attract Premium subscribers.

Standard in the West: Standard’s appeal in the West suggests a preference for a middle-ground subscription. This could mean that customers in the West seek a balance between cost and value, making Standard a good fit. The company could explore promotions or value-added services to solidify loyalty in this region.

Customizing Marketing and Engagement: Recognizing that each region has its subscription preference, the company can craft marketing campaigns and retention strategies to target the unique needs and preferences of each region. For example, highlighting cost savings in the East and North might attract and retain Basic subscribers, while emphasizing quality and exclusivity in the South could strengthen Premium’s appeal.

4. Insights on Customer Base and Service Strategy

High Reach with Basic as Entry Point: Basic’s widespread popularity indicates it functions well as an entry-level offering, providing access to a broad customer base and serving as a foundational tier. This positions Basic as a critical subscription type to maintain customer acquisition and engagement across diverse regions.

Opportunities for Tiered Growth: Given the consistent 12-month duration and Basic’s broad appeal, the company could focus on nurturing customer loyalty and engagement at the Basic level and then encouraging growth through tiered offerings. For instance, running educational campaigns or showcasing Premium benefits to Basic users might help them understand the value of upgrading.

Region-Based Tailoring for Subscription Enhancement: Recognizing the regional preferences for each type, the company can customize feature enhancements or promotional campaigns to match customer demand. In the South, for example, adding more exclusive Premium features might improve perceived value, while in the West, offering flexible subscription options or periodic benefits could appeal to Standard users.

![Screenshot (261)](https://github.com/user-attachments/assets/918a3145-1692-4f64-9e0c-4f2f98408a14)

Subscription Type Positioning

- Basic as the Popular Option: Basic’s widespread use might be due to factors such as affordability, accessibility, or general feature appeal. If Basic is viewed as an entry-level option, its success across two regions may imply that there’s a strong customer base that prefers a simpler, cost-effective subscription.

- Premium and Standard as Higher-Tier Options: Since Premium and Standard are available in only one region each but still generate revenue on par with Basic, it suggests they may be effectively positioned as higher-tier options with a more specific value proposition. This could appeal to customers looking for additional features or services.

![Screenshot (255)](https://github.com/user-attachments/assets/b8a30afd-30f7-4dbf-bd65-34d2a4dc4b8e)

1. Basic Subscription – East vs. North

No Cancellations in the East: The fact that there were zero cancellations for Basic in the East region suggests high customer satisfaction and loyalty. This could be attributed to:

Greater alignment with customer expectations: Customers in the East might feel that the Basic subscription meets their needs, reducing their likelihood to cancel.

Potential cultural or regional differences: There may be regional characteristics that make East customers more likely to retain their subscription. This could be due to economic factors, loyalty to the brand, or lesser exposure to competing services.

Service Quality or Customer Engagement: If there are differences in how services are delivered or promoted in the East (such as more effective customer support, tailored content, or local partnerships), this might contribute to higher retention for Basic users.

Significant Cancellations in the North: With 5,067 cancellations for Basic in the North, we see a stark contrast to the East. Possible reasons for this could be:

- Unmet Expectations or Value Perception: Customers in the North may feel that the Basic tier lacks some features or benefits they value, leading to higher cancellations.

- Competition or Alternative Options: The North region could have more exposure to competitors or alternative services, prompting users to switch or reconsider their subscription.

- Demographic or Behavioral Differences: There may be demographic factors at play, such as a younger or more price-sensitive customer base in the North, that makes users more likely to cancel if they do not see immediate or consistent value.

2. Premium and Standard – South and West

Similar Cancellation Patterns: For Premium in the South and Standard in the West, cancellation patterns are quite similar, with a high number of cancellations (5,064 in the South and 5,044 in the West).

Regional Preferences and Subscription Type Fit: This similarity suggests that while these tiers (Premium and Standard) may be popular, they may not fully meet customer expectations across both regions:

- Feature Expectations vs. Pricing: The Premium subscribers in the South and Standard subscribers in the West might have high expectations in terms of features or benefits. If these expectations aren’t fully met, it could lead to cancellations.

- Considerations for Retention Strategies: The company could explore whether adding tailored features, promotions, or discounts for these regions could improve retention rates.

- Market Saturation or Churn Factors: If both regions have reached a market saturation point or if customers are quick to change services, it might reflect in high cancellation rates for these tiers.

**Cohort Analysis**

![Screenshot (263)](https://github.com/user-attachments/assets/5a242375-3791-493a-a86e-f27f9f32386c)

1. Batch Enrollment Strategy:

This pattern could reflect a batch enrollment strategy, where subscriptions are only initiated at specific intervals (e.g., every three or four months) to streamline administrative processes. By limiting start dates, companies can synchronize operations, reducing the complexity of onboarding, billing, and managing subscriptions at various points in time.

2. Operational or Resource Optimization:

If there are resource-intensive steps involved in setting up a new subscription, such as account setup, training, or customer support, limiting start dates to specific months might help optimize these resources. For example, customer service teams can be better prepared for influxes of new customers at predictable times, improving the quality of service during onboarding periods.

3. Seasonal or Regional Marketing Campaigns:

This structure might also align with seasonal marketing campaigns that promote new subscriptions at regular intervals. For instance, launching enrollment campaigns every few months can create a sense of urgency, where potential customers wait for these “open” periods. The strategy might also be tailored to seasonal demand patterns, which vary by region (e.g., aligning subscription start dates with known high-demand periods).

4. Predictable Revenue Cycles:

A cyclical subscription model creates predictable revenue inflows as subscriptions renew at set intervals. This regularity can be helpful for financial planning and for analyzing customer behavior over consistent time frames.

Potential Implications and Areas for Analysis

1. Customer Behavior and Retention Patterns:

The specific start months could influence customer retention and cancellation trends. For instance, it may be interesting to see if customers who subscribe in certain months (e.g., March vs. July) have higher retention rates or different usage patterns.

2. Opportunities for New Enrollment Periods:

If you notice demand exists for start dates outside the current cycle, consider piloting an additional enrollment month to evaluate if there’s interest. For instance, adding a month between existing start dates could test if there’s demand for greater flexibility in each region.

3. Evaluation of Regional Consistency:

It’s also worth examining why some regions follow different cycles. For instance, the West has Standard subscriptions starting only in April, August, and December. This suggests regional differences in demand or operational considerations, which could be linked to regional resource availability or specific customer preferences.

**SQL Queries**

1 retrieve the total number of customers from each region.

 ```SQL
SELECT COUNT(CustomerName) AS Total_Customer, Region AS TotalPerRegion FROM [dbo].[CustomerDataProject]
GROUP BY Region
```

 Q2. find the most popular subscription type by the number of customers.

```SQL
SELECT COUNT(CustomerName) AS Total_Customer, SubscriptionType AS Most_Popular FROM [dbo].[CustomerDataProject]
GROUP BY SubscriptionType
ORDER BY  Total_Customer DESC
```

Q3.  find customers who canceled their subscription within 6 months.
```SQL
ALTER TABLE [dbo].[CustomerDataProject]
ADD Subscriptiondurationmonths Int
```

```SQL
UPDATE [dbo].[CustomerDataProject]
SET Subscription_duration_months = DATEDIFF(month, SubscriptionStart, SubscriptionEnd)
```

```SQL
SELECT COUNT(*) AS CUSTOMERWITHSHORTSUBSCRIPTIONS FROM [dbo].[CustomerDataProject]
WHERE SUBSCRIPTION_DURATION_MONTHS < 6
```

Q4 calculate the average subscription duration for all customers.

```SQL
SELECT AVG(Subscription_duration_months) AS Averagesubscriptionduration FROM [dbo].[CustomerDataProject]
```

5. find customers with subscriptions longer than 12 months. 

 ```SQL
SELECT CUSTOMERID, subscription_duration_months FROM [dbo].[CustomerDataProject]
 WHERE subscription_duration_months > 12
```

6. calculate total revenue by subscription type.

```SQL
SELECT SubscriptionType, SUM(Revenue) AS Total_Revenue FROM [dbo].[CustomerDataProject]
GROUP BY SubscriptionType
ORDER BY Total_Revenue
```


7.find the top 3 regions by subscription cancellations. 

```SQL
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
``` 

8. find the total number of active and canceled subscriptions.

TOTAL CANCELLATION

```SQL
SELECT COUNT(*) AS CANCELEDSUBSCRIPTION FROM [dbo].[CustomerDataProject]
WHERE CANCELED =1
```

ACTIVE CUSTOMERS 

``SQL
SELECT COUNT(*) AS ACTIVESUBSCRIPTION FROM [dbo].[CustomerDataProject]
WHERE CANCELED =0
```

### Interactive Dashboard
---

![Screenshot (269)](https://github.com/user-attachments/assets/a5466c70-24e6-4878-8894-5f79fa52ab7c)

### Key Insights and Recommendation

Maintaining High Retention in the East: With zero cancellations, the East is a model region for the Basic subscription. To maintain this, the company should:

- Leverage What’s Working: Investigate what drives satisfaction in the East and look for ways to replicate this success in other regions.

- Promote Regional Loyalty: Emphasizing regional loyalty programs or exclusive East-focused benefits could continue fostering the high retention rate here.

- Customized Engagement for Premium and Standard in the South and West: For these higher tiers, the company could:

- Focus on Added Value: Consider adding premium benefits or rewards for long-term subscribers in the South and West to make the subscription feel more valuable.

- Address Potential Service Gaps: Ensure that the features and benefits of these subscription types align closely with customer expectations, possibly by introducing customizable options.

**company could consider specific strategies to retain these users. This might include:**

- Adding Flexible Options: Introducing flexible plans, feature upgrades, or discount promotions could make the Basic subscription more appealing and reduce churn in the North.

- Targeted Customer Feedback: Gathering feedback from North region customers who canceled could provide valuable insights into unmet needs or areas for improvement in the Basic subscription.
Summary

The restricted start months likely reflect a deliberate strategy to manage subscriptions in regular intervals for consistency in operations, marketing, or financial cycles. While this can streamline processes, it’s useful to periodically assess if this pattern best serves customer needs or if demand exists for more flexible start dates.

The popularity of the Basic subscription type, coupled with the consistent 12-month subscription duration, highlights both stable customer engagement and an opportunity for growth through targeted regional strategies. The company can leverage Basic’s strong appeal as an acquisition tool while customizing marketing, engagement, and retention efforts per region to encourage upgrades and increase customer lifetime value across all subscription tiers.

### Conclusion
---

The revenue pattern suggests that while Basic achieves the highest cumulative revenue due to its dual-region presence, on a per-region basis, each subscription type performs comparably. This indicates balanced demand across regions and shows that the company’s regional approach is well-aligned with customer preferences. The company could consider exploring opportunities to introduce Premium or Standard to additional regions to capitalize on their high revenue potential, potentially boosting overall revenue while maintaining market balance.

The difference in cancellations for Basic in the East versus the North points to regional differences in customer satisfaction and expectations. The company could benefit from adopting a region-specific approach, tailoring retention strategies to address each region’s unique needs. In the North, targeted engagement could help reduce cancellations for Basic, while maintaining the loyalty of East subscribers should be a priority. For Premium in the South and Standard in the West, exploring ways to enhance perceived value could improve retention in those regions.



