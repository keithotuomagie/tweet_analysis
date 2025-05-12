# Business Understanding

KBO Marketing Company LLC is a marketing firm.  The firm wants to develop a model that can predict sentiment analysis for technology products such as smartphones.

The company's C-suite executives request their in-house data scientists to develop a prototype.  For the prototype, the in-house data scientists will perform the following:

- Leverage tweets for the Apple and Google brand and its respective products
- Classify sentiment analysis into two groups: *Not Positive* and *Positive*

# Data Understanding

The data for examing the aforementioned problem comes from the following source: [Brands and Product Emotions](https://data.world/crowdflower/brands-and-product-emotions) 

Before beginning to create a model, I want to examine and become familiar with the dataset. I will conduct exploratory data analysis in order to understand the dataset attributes, which includes, but not limited to the following:

1. Number of Columns
2. Number of Rows
3. Column Names
4. Format of the data in each column

## Data Overview

I created a Pandas DataFrame from the csv file.  The DataFrame contains 8,721 rows of data.  The DataFrame contains the following columns:

- *df['tweet_text']* - this is the sentiment provided via tweet
- *df['emotion_in_tweet_is_directed_at']* - this is the brand, or product, in which the tweet is targeted
- *df['is_there_an_emotion_directed_at_a_brand_or_product']* - this is the emotional category of the tweet

All of the columns are in string format.

## Observations | Brand or Product

I utilized the following code - *df['emotion_in_tweet_is_directed_at'].value_counts()* - to understand the different brands and products that are captured by the respective column.  The different brands and products are the following: 

- *iPad*
- *Apple*
- *iPad or iPhone App*
- *Google*
- *iPhone*
- *Other Google product or service*
- *Android App*
- *Android*
- *Other Apple product or service*

A bar chart that breaks down the different brands and products is listed below.

![Breakdown of Brand and Product](image_1.png)

## Observations | Brand or Product Sentiment

I utilized the following code - *df['is_there_an_emotion_directed_at_a_brand_or_product'].value_counts()* - to understand the brand and product sentiment captured by the respective column.  There are a total of four different brand and product sentiments, which are the following:

- *No emotion toward brand or product*
- *Positive emotion*
- *Negative emotion*
- *I can't tell* 

## Observations | Missing Values

I utilized the following code - *df.isna().sum()* - to understand how many missing values are within each column.  There is a total of 5,552 missing values in the *df['emotion_in_tweet_is_directed_at']* column.

There is 1 missing value in the *df['tweet_text']* column.

The other column *df['is_there_an_emotion_directed_at_a_brand_or_product']* did not have any missing values.

## Observations | Duplicate Rows

I utilized the following code - *df.duplicated().sum()* - to understand how many duplicates are present in the dataset.  There is a total of 22 duplicate rows.

# Data Preparation

# Modeling

# Overall Conclusion and Recommendations
