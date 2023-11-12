# User-Research
# Amazon Reviews Sentiment Analysis

This project aims to perform sentiment analysis on Amazon product reviews using several NLP models and libraries. It includes web scraping with Scrapy to gather reviews, sentiment analysis with Transformers, TextBlob, and text2emotion, and the final sentiment predictions.

## Installation

Please ensure you have the following dependencies installed before running the code:

- transformers
- torch
- chardet
- text2emotion
- emoji==1.6.3
- scrapy

You can install these dependencies by running the following commands:

- !pip install transformers
- !pip install torch
- !pip install chardet
- !pip install text2emotion
- !pip install emoji==1.6.3
- !pip install scrapy

## Usage

1. Run the `AmazonReviewsSpider` spider using Scrapy to scrape Amazon product reviews. You can specify the ASINs (Amazon Standard Identification Numbers) in the `asin_list` variable within the spider. The reviews will be saved in the `output1.json` file.

2. Once the reviews are obtained, run the sentiment analysis code. It uses three different models to predict sentiment: Transformers, TextBlob, and text2emotion.

3. The sentiment analysis results will be printed for each review, including the original text and the predicted sentiment from each model.

## Code Explanation

- `AmazonReviewsSpider`: This Scrapy spider is responsible for scraping Amazon product reviews. It takes a list of ASINs, visits the corresponding review pages, and extracts the reviews' ASIN, text, title, and rating.

- `Pipeline_sentiment`: This function uses the Transformers pipeline for sentiment analysis. It takes a text as input and returns the predicted sentiment and its score.

- `emo`: This function utilizes text2emotion library to calculate the emotion scores for anger, sadness, fear, happiness, and surprise. It then compares the negative and positive emotion scores to predict sentiment.

- `get_sentiment`: This function uses TextBlob library to calculate the sentiment polarity of a given text. It returns "Positive," "Negative," or "Neutral" based on the polarity score.

## Results

The sentiment analysis results for each review will be printed, showing the original text and the predicted sentiment from each model.

