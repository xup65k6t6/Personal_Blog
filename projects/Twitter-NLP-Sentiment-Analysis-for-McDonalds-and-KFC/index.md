---
layout: page
title: "Twitter NLP Sentiment Analysis (Tweepy, TextBlob, NLTK, WordCloud)"
tags: [python, sentiment analysis, NLP, Tweepy, NLTK]
date: 2023-06-20
comments: false
---

June 20, 2023

# Introduction

The "Twitter Sentiment Analysis" project focuses on the sentiment analysis of tweets related to McDonald's and KFC. It utilizes Python and various libraries to collect tweets, preprocess the data, and determine the sentiment by calculating various metrics. It provides fundamental knowledge and hands-on code for those new to Python and sentiment analysis.

The project code is available on GitHub [here](https://github.com/xup65k6t6/Twitter_Sentiment_Analysis/blob/main/tweet_collection_final%20version.ipynb).

Result
- result 1
- result 2

# Language and libraries
**Language** : Python

**Libraries** : 
* Data Collection: tweepy
* Data Manipulation: pandas, numpy
* Data Visualization: matplotlib, WordCloud
* Natural Language Processing: nltk, Counter, TextBlob


# Data Collection

## Tweets
To collect the tweets, It employed the Tweepy library, which provides access to the Twitter API. Users can specify keywords or hashtags to gather relevant tweets. It retrieved 5000 tweets for the keyword "mcdonalds" and "kfc” respectively, setting the language to english only. The data collected includes the tweets from Oct 1, 2022, to Oct 3, 2022.

## Authors
It collected the author's information related to all the tweets mentioned above. There are 4406 unique author id in Mcdonald's and 4396 author id in KFC. We have fetched 4390 unique and valid author information for Mcdondals and 4373 for KFC. There are a few authors whose ids are not found which might be due to the cancellation of the account.

Note that Tweepy has a protection scheme that allows extracting only 300 authors' data every 15 minutes (as of Oct 3, 2022). So it included a sleep function when querying author data.

\\ start from here

# Data Preprocessing

The collected tweets undergo preprocessing steps to clean and prepare them for sentiment analysis. The NLTK library is used for tasks such as tokenization, removing stopwords, and stemming. URLs, mentions, and special characters are removed to extract the meaningful text for sentiment analysis.

- remove stop words and URL

# Sentiment Analysis

The sentiment analysis is performed using the VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analysis tool. VADER assigns sentiment scores to individual words and calculates an overall sentiment score for each tweet. The sentiment scores indicate the positivity, negativity, and neutrality of the text.

# Visualization

The project incorporates various visualizations to present the results of the sentiment analysis. These visualizations include graphs and plots that provide insights into the overall sentiment distribution, frequently used positive and negative words, and the top influential users in the collected tweets.

# Future Improvement
1. Utilize VADER Sentiment Analysis to deal with special wording on social media

The code is well-documented and can be accessed on GitHub for a detailed understanding of the implementation and further exploration.

