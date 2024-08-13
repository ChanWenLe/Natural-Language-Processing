# Project Summary
Customer reviews and their associated ratings are feedback that sellers and Amazon should monitor to better comprehend customer experiences and address concerns effectively, thereby helping them remain competitive and stay relevant in the fast-paced retail sector.

The purpose of this project was to understand:

1. What messages and concerns would the customer like to convey in their comments?
2. What are the products that are on the list for positive and negative sentiments?

# Scope & Project Steps
### 1.)Scope

This project focuses on the Amazon Fashion segment, specifically analysing customer reviews of footwear to gain insights into their sentiments and preferences. The primary aim is to harness these insights to enhance customer satisfaction and loyalty, which are crucial for standing out from crowd and maintaining a competitive edge in the online retail market.

### 2.)Project Steps
1. Data Preprocessing and Wrangling
2. Data Visualisation
3. Data 
4. Evaluation of Results

# Data Preparation
With the raw dataset, a few data cleaning steps were conducted with Python. Code available in the "Amazon Reviews.ipynb" file.

**1.  Handling Null Values:** <br> The dataset underwent a null value check, revealing an empty 'style' column. <br>

**2.  Data Type Correction:** <br> To ensure consistency and facilitate numerical operations, 'style' column was converted from their original format to numeric. <br>

**3. Tokenising Customers Review:** <br> The dataset underwent a null value check, revealing an empty 'style' column. <br>

**4.  Data Type Correction:** <br> To ensure consistency and facilitate numerical operations, 'style' column was converted from their original format to numeric. <br>

### 1. Messages Dataset:
- Date: Date of message pushed live
- Category: Type of message (Product, Campaign, Promo)
- Total Recipient: Number of followers who received the message
- Open Count: Number of recipients who opened the message
- Clickthrough: Number of recipients who clicked on the image or link
- Content Format: Executed content type (Static, Carousel, Video, Text Bubble)

### 2. Friends Dataset:
- Total Friends: Total followers
- Target Reach Friends: The number of followers the account can reach through targeted messages based on gender, age, and/or region.
- Blocked Accounts: Total followers who block the branded account

# Key Insights
Designed to analyse a few trends and relationships:
1. Category vs Open Counts: Examining the correlation between message categories and open counts.
2. Category vs Clickthrough: Analyzing how different message categories impact user clickthrough rates.
3. Content Format vs Clickthrough: Assessing the effectiveness of various content formats in generating clickthrough.
4. Average Open Rate per Year: Calculating the average open rate per year (Total open counts/Total Recipients *100%).
5. Average Clickthrough Rate per Year: Determining the average clickthrough rate per year (Total clickthrough/Total Recipients *100%).
6. Trend of Friends, Blocked Accounts, and Target Reach Friends per Year: Tracking the annual trends in the number of friends, blocked accounts, and target reach friends.

# Dashboard Link
Explore the interactive dashboard [here](https://public.tableau.com/app/profile/k.f4836/viz/NikeLINEDashboard/Dashboard?publish=yes)
<img width="1428" alt="Screenshot 2023-11-19 at 10 45 13 AM" src="https://github.com/Kfkyyian1/linetableaudashboard/assets/146427900/e954cdde-afb9-4388-827f-f08379bd100f">

# Data Insights:
1. Yearly Trends: The average total friends show a consistent increase year on year. However, blocked accounts increased from 2020 to 2021, with a slight decrease in 2022. Simultaneously, the average number of target reach friends is decreasing, indicating potential user disengagement. They might be phasing out of LINE and prefer to use other social messaging platforms instead.
2. Category Analysis: Product and campaign categories exhibit higher average open counts, while product and promo categories have the highest average clickthrough. Users are more engaged with product-related messaging, indicating a desire to explore new product launches and make purchases.
3. Content Format Effectiveness: Plain vanilla static content format demonstrates the highest average clickthrough, suggesting that this format requires minimal user interaction and encourages direct engagement with the call-to-action.
