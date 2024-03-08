# Natural Language Processing for sentiment analysis of 25,000 movie reviews
This Python script aims to perform sentiment analysis on a dataset consisting of 25,000 movie reviews. The goal is to classify each review as either positive or negative based on its textual content.
The ultimate objective of this script is to build and evaluate models capable of accurately predicting the sentiment in human-created text.

## Prerequisites:
* Python 3.x
* pip

__Data used:__ 
* _labeledTrainData_ - The labeled training set. The file is tab-delimited and has a header row followed by 25,000 rows containing an id, sentiment, and text for each review.  
* _testData_ - The test set. The tab-delimited file has a header row followed by 25,000 rows containing an id and text for each review. Your task is to predict the sentiment for each one. 
* _unlabeledTrainData_ - An extra training set with no labels. The tab-delimited file has a header row followed by 50,000 rows containing an id and text for each review. 

__Steps:__ 
> 1. Data Preprocessing:
>> * The movie review dataset is loaded and preprocessed to remove HTML tags, punctuation, and stopwords.
>> * The cleaned text data is tokenized into words and sentences.
> 2. Word Embedding with Word2Vec:
>> * The Word2Vec algorithm is employed to learn distributed representations of words from the movie review corpus.
>> * Word embeddings capture semantic relationships between words, allowing for better understanding of their meanings in context.
> 3. Feature Extraction:
>> * The average feature vectors for each review are computed by averaging the Word2Vec word embeddings of its constituent words.
>> * These average feature vectors serve as numerical representations of the review texts and are used as input for classification.
> 4. Classification:
>> * Two classification approaches are implemented:
>>> * Random Forest Classifier: A machine learning model is trained on the training data to classify reviews into positive or negative categories.
>>> * KMeans Clustering: Unsupervised clustering is performed to group similar reviews together based on their feature representations.
