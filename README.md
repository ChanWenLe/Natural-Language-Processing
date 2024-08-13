
![Screenshot 2024-08-13 191328](https://github.com/user-attachments/assets/0a7f496c-e38f-421d-aec0-3cba5f1fe6f5)

# Project Summary
Customer reviews and their associated ratings are feedback that sellers and Amazon should monitor to better comprehend customer experiences and address concerns effectively, thereby helping them remain competitive and stay relevant in the fast-paced retail sector.

The purpose of this project was to understand:

1. What messages and concerns would the customer like to convey in their comments?
2. What are the products that are on the list for positive and negative sentiments?

Dataset is avaialable [Here](https://github.com/ChanWenLe/Natural-Language-Processing/blob/main/New%20folder/AMAZON_FASHION_5.json.gz)

# Scope & Project Steps
### 1.)Scope

This project focuses on the Amazon Fashion segment, specifically analysing customer reviews of footwear to gain insights into their sentiments and preferences. The primary aim is to harness these insights to enhance customer satisfaction and loyalty, which are crucial for standing out from crowd and maintaining a competitive edge in the online retail market.

### 2.)Project Steps
1. Data Preprocessing and Wrangling
2. Sentiment Analysis 
3. Data Visualisation 
4. Evaluation of Results

# Data Preprocessing and Wrangling
With the raw dataset, a few data cleaning steps were conducted with Python. Code available in the "Amazon Reviews.ipynb" file.

**1.  Handling Null Values:** <br> The dataset underwent a null value check, revealing a few empty 'style' columns. <br>

**2.  Data Type Correction:** <br> To ensure consistency in textual analysis and facilitate analysis operations, 'style' column was converted from their original format to string. <br>

**3. Data Preprocessing for Sentiment Analysis:** <br>The text was cleaned by removing punctuation and converting all letters to lowercase. Stop words were removed to focus on more meaningful words, subsequently, lemmatization was applied to bring words to their base or root form, aiding in the simplification and standardisation of data for analysis. <br>

**4.  Tokenisation of the Corpus:** <br> To identify the list of words that emerge most frequently from customer comments, the cleaned corpus was broken down into individual words or phrases. This process is essential for analysing the frequency and distribution of distinct words.  <br>

# Sentiment Analysis
### 1.NLTK:
![Distribution of Sentiment Scores for NLTK](https://github.com/user-attachments/assets/f39fb666-6840-4941-98bc-dac6f91b7c47)

- Date: Date of message pushed live
- Category: Type of message (Product, Campaign, Promo)
- Total Recipient: Number of followers who received the message
- Open Count: Number of recipients who opened the message
- Clickthrough: Number of recipients who clicked on the image or link
- Content Format: Executed content type (Static, Carousel, Video, Text Bubble)

### 2. TextBlob:
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
