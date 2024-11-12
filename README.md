-----------------------------Sentiment Analysis - Hotel Reviews---------------------
-
Sentiment analysis is part of the Natural Language Processing (NLP) techniques that consists in extracting emotions related to some raw texts. 
This is usually used on social media posts and customer reviews in order to automatically understand if some users are positive or negative and why. 
The goal of this study is to analyse the sentiment of the customers who visited & stayed at the hostel across Europe.

Below are the libraries used in the notebook.
- 
NLTK: the most famous python module for NLP techniques
googletrans: used to translate customer reviews from different languages to English.
Gensim: a topic-modelling and vector space modelling toolkit
Scikit-learn: the most used python machine learning library

We have used sample hotel reviews data. Each observation consists in one customer review for one hotel. 
Each customer review is composed of a textual feedback of the customer's experience at the hotel and an overall rating.

For each textual review, we want to predict if it corresponds to a good review (the customer is happy) or to a bad one (the customer is not satisfied). 
The reviews overall ratings can range from 2.5/10 to 10/10. In order to simplify the problem we will split those into two categories:

bad reviews have overall ratings < 5
good reviews have overall ratings >= 5
We have also implemented a mechanism to translate the customer reviews from different languages to English.

------------------------------------Project Execution Steps--------------------------------
-
1. Create Fabric Workspace
2. Create Lakehouse
3. Upload Hotel_Reviews.csv file to Lakehouse
4. Use notebook LoadHotelReviewsData.ipynb to load data and convert it to Delta table in Lakehouse
5. Use notebook SentimentAnalysisHotelReviews.ipynb for data analysis
6. Use PowerBI report SentimentAnalysisWithHotelReviews.pbix to see the sentiment analysis by slicing and dicing the data.
   - Hello Page - Welcome Page
   - Sentiment Analysis - Customer sentiment analysis page
   - Translation - Reviews translated feedback to english language
   - Analyze Data - Using various filter like year, quarter, hotel names, nationality and tags we can analyse the data
   - Trends - Average scores and review scores across hotels.
