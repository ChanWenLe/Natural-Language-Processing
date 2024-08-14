
![Screenshot 2024-08-13 191328](https://github.com/user-attachments/assets/0a7f496c-e38f-421d-aec0-3cba5f1fe6f5)

# Project Summary
Customer reviews and their associated ratings are feedback that sellers and Amazon should monitor to better comprehend customer experiences and address concerns effectively, thereby helping them remain competitive and stay relevant in the fast-paced retail sector.

The purpose of this project was to understand:

1. What messages and concerns would the customer like to convey in their comments?
2. What are the products that are on the list for positive and negative sentiments?

Dataset is available [Here](https://github.com/ChanWenLe/Natural-Language-Processing/blob/main/New%20folder/AMAZON_FASHION_5.json.gz)

# Scope & Project Steps
### 1.)Scope

This project focuses on the Amazon Fashion segment, specifically analysing customer reviews of footwear to gain insights into their sentiments and preferences. The primary aim is to harness these insights to enhance customer satisfaction and loyalty, which are crucial for standing out from crowd and maintaining a competitive edge in the online retail market.

### 2.)Project Steps
1. Data Preprocessing and Wrangling
2. Sentiment Analysis <br>
   -NLTK <br>
   -TextBlob <br>
   -SpaCy
4. Data Visualisation 
5. Evaluation of Results

# Data Preprocessing and Wrangling
With the raw dataset, a few data cleaning steps were conducted with Python. Code available in the "Amazon Reviews.ipynb" file.

**1.  Handling Null Values:** <br> The dataset underwent a null value check, revealing a few empty 'style' columns. <br>

**2.  Data Type Correction:** <br> To ensure consistency in textual analysis and facilitate analysis operations, 'style' column was converted from their original format to string. <br>

**3. Data Preprocessing for Sentiment Analysis:** <br>The text was cleaned by removing punctuation and converting all letters to lowercase. Stop words were removed to focus on more meaningful words, subsequently, lemmatization was applied to bring words to their base or root form, aiding in the simplification and standardization of data for analysis. <br>

**4.  Tokenisation of the Corpus:** <br> To identify the list of words that emerge most frequently from customer comments, the cleaned corpus was broken down into individual words or phrases. This process is essential for analysing the frequency and distribution of distinct words.  <br>

# Sentiment Analysis

Different libraries, such as NLTK and TextBlob, were used to conduct sentiment analysis. The results were then compared with customer ratings recorded under the 'overall' column, ranging from 1 to 5, with the assumption that these ratings genuinely reflect customer satisfaction levels.

Ratings of 1 and 2 are classified as negative sentiment, 3 as neutral, and 4 and 5 as positive sentiment. Similarly, sentiment scores from the models are categorized as negative if they are below -0.05 and recognized as positive if they are above 0.05. After standardizing the results from both columns, they were compared for accuracy using the sklearn library.

It was observed that NLTK's VADER model, with an accuracy of 81.23%, slightly outperformed TextBlob, which had an accuracy of 79.22%. Thus, the NLTK sentiment analysis model is preferred due to its higher accuracy rate.

### 1.NLTK:
![Distribution of Sentiment Scores for NLTK](https://github.com/user-attachments/assets/f39fb666-6840-4941-98bc-dac6f91b7c47)
![Distribution of Sentiment Scores for NLTK2](https://github.com/user-attachments/assets/2852de58-c19c-41a8-8bb8-91847631f99f)



### 2. TextBlob:
![Distribution of Sentiment Scores for Textblob](https://github.com/user-attachments/assets/cefd0636-a762-4445-9789-e1403b16aa94)
![Distribution of Sentiment Scores for Textblob 2](https://github.com/user-attachments/assets/4f784a06-4385-432e-a68f-a6fc8e3d4585)


### 3. SpaCy
After using NLTK for initial sentiment analysis, spaCy was deployed to enhance accuracy and efficiency. While NLTK and TextBlob are great for basic text processing, spaCy's advanced capabilities in Named Entity Recognition (NER) and dependency parsing, along with its high performance and easy integration, make it ideal for refining and expanding the analysis.
![Screenshot 2024-08-13 191328](https://github.com/user-attachments/assets/df7891b7-ea79-4bbc-b926-67011075de1a)
![Picture1](https://github.com/user-attachments/assets/8983906e-3c59-4394-82a8-c65d8707c168)

A predominance of 'CARDINAL' entities has been observed. It typically consists of numeric data that could relate to product sizes, quantities, or frequency of use mentioned in customer reviews. These insights could inform stock management decisions and help anticipate customer needs. 'ORG' is another entity which deserve the attention, it highlights the brand mentions which are invaluable for measuring brand visibility and perception in the market. Brands like 'Nike' are prominently mentioned, indicating significant customer engagement that could drive strategic marketing campaigns.

'CARDINAL' terms such as 'half' or specific numbers may inform businesses about prevalent customer preferences or sizing issues. Meanwhile, the frequent citation of 'Nike' and similar 'supreme tr' entities could signal which brands are top-of-mind for consumers, guiding competitive strategy and brand positioning.

The presence of 'DATE' entities might reflect on the usage patterns, durability of products or customer experiences. For instance, frequent references to "several years" or "daily" suggest the usage patterns or durability of product, informing potential promotional narratives or product improvement strategies.


# Evaluation of Results


### 1. What messages and concerns would the customer like to convey in their comments?

![image](https://github.com/user-attachments/assets/6976de95-4b97-4211-945c-8e9d55492f33)
![image](https://github.com/user-attachments/assets/bd115277-4106-4340-98ef-2fd07963fa77)

Using the NLTK model, it showed that 82.7% of reviews were positive, 10.6% were neutral, and 6.6% were negative. Two different subsets were filtered out: the positive sentiment subset and the negative sentiment subset. The positive sentiment subset consisted of reviews with a sentiment score of 0.5 or higher and a rating of 4 or 5, whereas the negative sentiment subset included data with a sentiment score of -0.05 or below, or ratings of 1 and 2. This distribution into two groups aims to closely examine and understand the feedback categorized under the respective sentiments. It is necessary since negative sentiment constitutes only 6.6% of the total data.

From the observation of the word cloud above, the most frequent words identified in positive sentiment feedback—'shoe,' 'comfortable,' 'love,' 'fit,' and 'great'—dominate these visuals, highlighting customer priorities and satisfaction. The recurrence of terms like 'comfortable,' 'love,' and 'fit' suggests a positive reception of the products' quality and alignment with advertisement claims, while 'great' signals overall approval. These findings, especially the frequent mention of 'love', may indicate strong performance by sellers, reflecting well on customer satisfaction and product fit.

On the other hand, the most common key terms associated with negative sentiment feedback include "return," "size," and "hurt," indicating common issues customers have encountered. The significant presence of "return" suggests a substantial volume of returns due to dissatisfaction. Terms like "small" and "big" likely refer to problems with sizing or fit, while "discomfort" and "hurt" could point to issues with the physical experience of wearing the products.

### 2. What are the products that are on the list for positive and negative sentiments?
![image](https://github.com/user-attachments/assets/6c796208-e84c-45af-95d4-4b54080c0182)
![image](https://github.com/user-attachments/assets/c2ec7b97-fd0d-49ee-ac3b-bb0486282897)

The analysis highlights the specific styles that have received positive feedback from customers, particularly in the shoe sizes of 8 B(M) US, 9 B(M) US, and 8.5 B(M) US, and in the colour combination Black/White/Anthracite/Stealth. This information is valuable for the platform and vendors to understand consumer preferences.
