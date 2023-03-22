# Recency, Frequency and Monetary value model (RFM Model)

>Organisations of today need to better leverage data resources to create value, enhance competitiveness and drive business decisions.
The approach is based on the proposition that business success depends on what you actually do with your business information, not how much of it you control and collate.
Organisation can a holistic view of data, enabling you to learn from and use it to make better business decisions, grow revenue, enhance operational capabilities, and manage enterprise risks and compliance mandates.
With analytical and technical solutions deeply anchored in industry and functional knowledge, combined with a detailed understanding of clients' needs, the approaches demystify data management, tackle industry-specific challenge, and cover a range of important business issues.

>Sprocket Central Pty Ltd , a medium size bikes & cycling accessories organisation that is keen to learn more about Analytics, Information & Modelling 
Primarily, Sprocket Central Pty Ltd needs help with its customer and transactions data. The organisation has a large dataset relating to its customers, but their team is unsure how to effectively analyse it to help optimise its marketing strategy. 

The client provided with 3 datasets:
- Customer Demographic 
- Customer Addresses
- Transactions data in the past 12 months

### TASK ONE 

**Identify the data quality issues and strategies to mitigate these issues. Refering to ‘Data Quality Framework Table’ and resources below for criteria and dimensions which you should consider.**

>Criteria to observe during the data exploration analysis
>- Accuracy 
>- Completeness
>- Uniqueness
>- Validity
>- Relevancy 
>- Consistency 

**Summary of Data Quality Checks on Client Datasets.**


| Data set | Accuracy | Completeness | Consistency | Uniqueness | Relevancy | Validity |
|-------------------------|----------|----------|----------|----------|----------|----------| 
| Customer Demographic | DOB info is  inaccurate| Job title and Job industry category is missing data| Gender inconsistency | No duplicates| Default Column with no relevance  |  |
| New Customer |          | Customer id is incompete| Gender inconsistency| No duplicates  |There are many columns unamed|          |
| Transactions | Profit is missing | Various columns have nulls that is insightful in analysis |          | No duplicates | Cancellation status need to be updated   | List price format should be corrected  |
|Impact |Regulatory implications like fines. Reputational damage from litigation|  | Missed opportunity in accurate segments| Skewed data leading to inaccurate analysis| Memory cost implications

**Accuracy issues:**

The DOB data in the "Customer Demographic" sheet is inaccurate for some customers, and an age column is missing, which makes it difficult to analyze customer demographics accurately. To mitigate this, the company should adjust the DOB data for each customer to ensure accuracy, and add an age column to the sheet to have a clear view of the age distribution of customers. This information will be valuable in understanding customer behavior and preferences, and in developing targeted marketing strategies.

The "Transaction" sheet is missing the profit realized in the year, which is crucial information for analyzing revenue and forecasting sales trends. The company should ensure that all necessary financial data is included in the transaction sheet for accurate analysis.

**Completeness:**

Some essential data, such as job title and job industry category in the "Customer Demographic" sheet, is missing, which makes it difficult to understand the customer's professional background. The company should ensure that all relevant customer data is captured in the sheet to enable better analysis of customer demographics and behavior.

The number of customer IDs is incomplete, which may make it difficult to identify customers and analyze their behavior. The company should ensure that all customer IDs are captured accurately to enable comprehensive analysis of customer behavior.

Columns such as product class, brand, standard cost, product line, and product date sold are vital information that assists in tracking changes in cost and revenue details for forecasting. The company should ensure that these columns are complete and accurate to enable better analysis and forecasting of product sales and revenue.

**Consistency:**

The gender column in the "Customer Demographic" and "New Customer" sheets have inconsistencies that need clarification. The company should ensure that gender data is captured accurately and consistently to enable comprehensive analysis of customer demographics and behavior.

**Uniqueness:**

The data set has no duplicates, which is good news for the company. The company should ensure that all future data is checked for duplicates to maintain data quality.

**Relevancy:**

The "default" column in the "Customer Demographic" sheet has no relevancy to the data. The company should remove this column to maintain data cleanliness and consistency.

The "Transaction" sheet includes canceled orders, which may skew the analysis of customer behavior and revenue. The company should filter out canceled orders to enable accurate analysis of sales and revenue trends.

**Overall, the company should prioritize data quality to ensure that accurate, complete, consistent, and relevant data is used for analysis and decision-making. The company should also consider investing in data management tools and software to improve data accuracy and completeness, reduce inconsistencies, and ensure better data quality control.**

### TASK TWO 

>Sprocket Central Pty Ltd has given us a new list of 1000 potential customers with their demographics and attributes. However, these customers have prior transaction history with the organisation. 
The marketing team at Sprocket Central Pty Ltd is sure that, if correctly analysed, the data would reveal useful customer insights which could help optimise resource allocation for targeted marketing. Hence, improve performance by focusing on high value customers.

**The marketing team is looking to boost business by analysing their existing customer dataset to determine customer trends and behaviour.**
**Using the existing 3 datasets (Customer demographic, customer address and transactions) as a labelled dataset, please recommend which of these 1000 new customers should be targeted to drive the most value for the organisation.**

### Data Exploration

#### Most Profitable Brand
When conducting analysis it is important to factor in what was the most sold good in the company. The graph shows which is the most profitable brand sold in the company. From there we can calculate which product the company ought to focus on more. The data indicates that WeareA2B is the profitable good as compared to other products in the company. In this research study we should explore why is that the case that many customers in the company prefer that product over others.

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Profitable%20Brand.png" alt="Image description" width="400" height="400">


#### Bike Related Purchase according to Gender
Males are predominantly purchasing bike related products in the company as opposed to other genders. Nonetheless, it is worth noting that females are not far as well having a slighlty less purchases than males. This indicates to the marketing team they can focus on gender neutral products and it would not have a big impact in their sales saving cost on certain production measures. The Marketing team finds itself in a good position where they won't have to over spend in their marketing strategies in regards to gender. 

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Bike%20related%20purchase%20by%20gender.png" alt="Image description" width="400" height="400">

### Model Development

>The “RFM” in RFM analysis stands for recency, frequency and monetary value. RFM analysis is a way to use data based on existing customer behavior to predict how a new customer is likely to act in the future. An RFM model is built using three key factors:
>1. How recently a customer has transacted with a brand
>2. How frequently they’ve engaged with a brand
>3. How much money they’ve spent on a brand’s products and services

>Rather than analyzing the entire customer database, it’s better to segment customers by characteristics like age or geography and separate them into a customer group. By engaging them in a well-segmented marketing campaign, you are able to create a relevant, personalized offer for a high-value customer.

It is important to understand the rankings of the customer title shown below: 
1. Platinum - They are customers are very loyal, have a high purchasing power and make frequent transactions with the company.
2. Gold - They are also Customers with a high purchasing power but they dont make as frequent transactions as Platinum members
3. Silver - They are customers not as profitable as Gold and Platinum but they make frequent transactions more than Bronze
4. Bronze - They are least profitable and highly demanding in nature. 

We observe from the new customer list we have a large majority of the customers being platinum members followed by Bronze , Gold and Silver respectively
The company they should look into why they have more bronze customers as opposed to the Gold customers. How can they turn them into Silver Customers? Areas they can look into is services offered to those customers, incentives like promotions/discounts can appeal to them and store credit 

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/RFM_score.png" alt="Image description" width="600" height="400">

#### Scatter plot of recency and monetary value

The chart shows that customers who purchased more recently have generated more revenue than customers who visited a while ago. 
Customers from recent past (50-100) days also show to generate a moderate amount of revenue.
Those who visited more than 200 days ago generate low revenue

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Scatter%20Recency%20vs%20MonetaryValue.png" alt="Image description" width="500" height="400">

#### Scatter plot of monetary value and frequency
Customers classified as “Platinum”, “Gold”, “Bronze” and “Silver” are represented in the scatter plot. 
Platinum customers bring more value and visit the company frequently whilst Bronze customers visit the company least frequently hence bringing lower monetary value

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Scatter%20MonetaryValue%20vs%20Frequency.png" alt="Image description" width="500" height="400">

#### Profitable brand according to RFM score
We observe that there isn't much change in the most profitable good from the previous analysis. It is worth noting that in each brand category they are more Platinum and Gold members buying more of the products which indicates that the company should look for a strategy to invest more on how they can retain the platinum members pushing sales higher.

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Profitable%20brand%20per%20RFM.png" alt="Image description" width="600" height="400">

#### Segmentation of gender according to title
Platinum member being they are the most we observe that females are more dominant in each customer title category.
The company should interpret this as an opportunity to learn their clientele's needs in order to sell what they prefer increasing sales.

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Gender%20vs%20Customer%20Title.png" alt="Image description" width="500" height="400">

#### Segmentation of wealth segment according to title
In the wealth segment, the categorization of customers into Mass, Affluent, and High Net Worth segments is based on their level of wealth and investable assets. The Mass segment typically comprises customers with lower levels of wealth, while the Affluent and High Net Worth segments consist of customers with higher levels of wealth and investable assets.
A large proportion of wealth segement lies in the mass customer as they comprise with more platinum member as compared to the other segments. 
It is worth noting that High Net worth customers on the platinum side is higher than an affluent customer meaning the company can strategize how they can increase sales by having more gold member become platinum. Focus on Retaining Platinum Members: Regardless of the segment, the Platinum members are the most valuable customers, and the company should focus on retaining them by providing personalized services, exclusive perks, and rewards. They can also offer incentives for referring other customers within their segment.

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/wealth%20segment.PNG" alt="Image description" width="500" height="400">

### Recommendation 

>Focus on Retaining Platinum Members: Since Platinum members are the most valuable customers, the company should focus on retaining them by providing personalized services, exclusive perks, and rewards. They can also offer incentives for referring other customers.

>Improve Services for Bronze Members: Bronze members are the least valuable customers in terms of their monetary value, but they still represent a significant portion of the customer base. The company can improve services for Bronze members to encourage them to upgrade to higher tiers.

>Upsell to Gold and Silver Members: Gold and Silver members have a higher monetary value than Bronze members, and they are likely to be more receptive to upselling and cross-selling efforts. The company can offer them upgrades, add-ons, or bundles to increase their lifetime value.

>Customize Marketing and Promotions: The company can customize its marketing and promotional efforts based on the different segments. For example, Platinum members may respond better to exclusive promotions and events, while Bronze members may be more interested in discounts and freebies.

>Collect and Analyze Customer Feedback: The company can collect feedback from all segments to identify areas for improvement and to tailor its services to meet the needs of different customers. This can help the company improve customer satisfaction and increase loyalty across all segments.

Overall, the company should aim to provide a personalized experience to all customers and focus on building long-term relationships. By understanding the different segments and their unique needs, the company can develop effective strategies to increase customer retention, loyalty, and revenue.


