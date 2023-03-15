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

**Summary table of the data quality framework**


| Data set | Accuracy | Completeness | Consistency | Uniqueness | Relevancy | Validity |
|-------------------------|----------|----------|----------|----------|----------|----------| 
| Customer Demographic | DOB info is  inaccurate| Job title and Job industry category is missing data| Gender inconsistency | No duplicates| Default Column with no relevance  |  |
| New Customer |          | Customer id is incompete| Gender inconsistency| No duplicates  |There are many columns unamed|          |
| Transactions | Profit is missing | Various columns have nulls that is insightful in analysis |          | No duplicates | Cancellation status need to be updated   | List price format should be corrected  |
|Impact |Regulatory implications like fines. Reputational damage from litigation|  | Missed opportunity in accurate segments| Skewed data leading to inaccurate analysis| Memory cost implications

### TASK TWO 

>Sprocket Central Pty Ltd has given us a new list of 1000 potential customers with their demographics and attributes. However, these customers have prior transaction history with the organisation. 
The marketing team at Sprocket Central Pty Ltd is sure that, if correctly analysed, the data would reveal useful customer insights which could help optimise resource allocation for targeted marketing. Hence, improve performance by focusing on high value customers.

**The marketing team is looking to boost business by analysing their existing customer dataset to determine customer trends and behaviour.**
**Using the existing 3 datasets (Customer demographic, customer address and transactions) as a labelled dataset, please recommend which of these 1000 new customers should be targeted to drive the most value for the organisation.**

### Data Exploration

#### Most Profitable Brand
When conducting analysis it is important to factor in what was the most sold good in the company. The graph shows which is the most profitable brand sold in the company. From there we can calculate which product the company ought to focus on more. The data indicates that Trek Bicycles is the profitable good as compared to other products in the company.

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Profitable%20Brand.png" alt="Image description" width="400" height="400">


#### Bike Related Purchase according to Gender
Males are predominantly purchasing bike related products in the company as opposed to other genders. Nonetheless, it is worth noting that females are not far as well having a slighlty less purchases than males. This indicates to the marketing team they can focus on gender neutral products and it would not have a big impact in their sales saving cost on certain production measures. 

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Bike%20related%20purchase%20by%20gender.png" alt="Image description" width="400" height="400">

### Data Development

>The “RFM” in RFM analysis stands for recency, frequency and monetary value. RFM analysis is a way to use data based on existing customer behavior to predict how a new customer is likely to act in the future. An RFM model is built using three key factors:
>1. How recently a customer has transacted with a brand
>2. How frequently they’ve engaged with a brand
>3. How much money they’ve spent on a brand’s products and services

>Rather than analyzing the entire customer database, it’s better to segment customers by characteristics like age or geography and separate them into a customer group. By engaging them in a well-segmented marketing campaign, you are able to create a relevant, personalized offer for a high-value customer.

We observe from the new customer list we have a large majority of the customers being platinum members followed by Bronze , Gold and Silver respectively 

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/RFM_score.png" alt="Image description" width="400" height="400">

#### Scatter plot of recency and monetary value

The chart shows that customers who purchased more recently have generated more revenue than customers who visited a while ago. 
Customers from recent past (50-100) days also show to generate a moderate amount of revenue.
Those who visited more than 200 days ago generate low revenue

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Scatter%20Recency%20vs%20MonetaryValue.png" alt="Image description" width="500" height="400">

#### Scatter plot of monetary value and frequency
Customers classified as “Platinum”, “Gold”, “Bronze” and “Silver” are represented in the scatter plot. 
Platinum customers bring more value and visit the company frequently whilst Silver customers visit the company lest frequently hence bringing lower monetary value

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Scatter%20MonetaryValue%20vs%20Frequency.png" alt="Image description" width="500" height="400">

#### Profitable brand according to rfm score
From the previous analysis we observed that the most profitable brand was Trek Bicycles. From new developments using the RFM values we observe that WeareA2B is the most profitable good. 
Platinum and Gold are buying more of the brand which indicates that the company should look for a strategy to invest more on that brand to attract the new customers 

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Profitable%20brand%20per%20RFM.png" alt="Image description" width="500" height="400">

#### Segmentation of gender according to title
Platinum member being they are the most we observe that females are more dominant in each customer title category.
The company should interpret this as an opportunity to learn their clientele's needs in order to sell what they prefer increasing sales.

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/Gender%20vs%20Customer%20Title.png" alt="Image description" width="500" height="400">

#### Segmentation of wealth segment according to title
A large proportion of wealth segement lies in the mass customer as they comprise with more platinum member as compared to the other segments. 
It is worth noting that High Net worth customers on the platinum side is higher than an affluent customer meaning the company can strategize how they can increase sales by having more gold member become platinum

<img src="https://github.com/Mugambi99/Financial-analysis-projects/blob/main/RFM%20Model/Plots/wealth%20segment.PNG" alt="Image description" width="500" height="400">

### Recommendation 




