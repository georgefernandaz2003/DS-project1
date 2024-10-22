Scenario:
The demonetization of Indian currency was a step taken by Government of India on November 8 leaving the entire country into shock. Some of currency notes were banned and entire country became emotional and few have taken to twitter to express their feelings.

Challenge:
It's important to understand the implications of the steps taken by Government and take actions based on the citizen's response. You, as a Data Scientist, have to analyse these tweets to understand the overall reaction of citizens.

Dataset:
Data of tweets on #demonetization has been extracted from Twitter and is available in the file "demonetization_tweets_data.csv". This dataset contains 7470 rows and 12 columns. The description of the columns is as given below:

text: Text of tweet
favorited: Boolean; indicates whether the tweet has been liked by authenticating user
favoriteCount: Number of times this tweet has been liked
replyToSN: Screen Name of original tweet's author if this tweet is a reply
created: Timestamp of creation of tweet
truncated: Boolean; indicates whether the tweet has been truncated due to length limits
replyToSID: ID of the original tweet if this tweet is a reply
statusSource: Source used to post the tweet
screenName: Screen Name of the author of the tweet
retweetCount: Number of times this tweet has been retweeted
isRetweet: Boolean; indicates whether this tweet is a retweet or not
retweeted: Boolean; indicates whether this tweet has been retweeted by authenticating user

Load and analyse the data
Load the data from the required location into a DataFrame
Analyse the shape of the data by printing its total number of rows & columns
Also print 5 rows of the DataFrame
Print the 'text' of the tweet with highest number of retweets

Clean the data
Observe that the tweet text contains various elements such as 'Retweet tag RT@', 'punctuation marks' and 'stop words'
Use functions from Python libraries such as re, string and NLTK to remove these unnecessary elements

Process the data
Apart from cleaning, data also needs to be processed to remove elements which may cause issues in analysis

Examples of such elements are 'single characters', 'multiple spaces', 'Upper-cased'

Apply various text pre-processing techniques one-by-one to the cleaned data

Remove all the special characters
Remove single characters appearing in the text except the start
Remove single characters appearing at the start
Substitute multiple spaces with a single space
Remove prefix 'b'
Convert to lowercase
Print first five values of processed data
Add the processed data as a separate column to the DataFrame

Run Sentiment analysis
Import TextBlob from Python to calculate various Sentiment scores as described below:

Polarity is a float value within the range [-1.0 to 1.0] where 0 indicates neutral, +1 indicates a very positive sentiment and -1 represents a very negative sentiment.
Subjectivity is a float value within the range [0.0 to 1.0] where 0.0 is very objective and 1.0 is very subjective. Subjective sentence expresses some personal feelings, views, beliefs, opinions, allegations, desires, beliefs, suspicions, and speculations where as Objective sentences are factual.
After calculating the above scores, encode the polarity scores into three categories- 'positive', 'negative' and 'neutral'

Print the most positive and most negative tweet using Polarity score

Print the most subjective and most objective tweet using Subjectivity score

Apply Vectorization
Create a DataFrame containing only the columns of interest- Processed text & Polarity Category
Tokenize the text using TweetTokenizer from NLTK
Calculate the number of unique words (Bag of Words) using Count Vectorizer

Create a classification model on our data
Split the data into training and testing data sets
Use processed data as independent variable and polarity as dependent variable
Extract features using TFIDF Vectorizer
Perform Multinomial Naive Bayes Claasification
Apply MultinomialNB on training data
Predict polarity by fitting the model to testing data
Calculate accuracy of predicted values
Perform Random Forest classification on the processed data and compare the accuracy score of both these models

Conclusion: In this demonstration of the case study, we examined how to perform Sentiment Analysis on Twitter data through various phases such as data cleaning, data pre-processing, tokenization, sentiment scoring, feature extraction and classification using Machine Learning algorithms.
