# Twitter-Sentiment-Analysis
Model for sentiment analysis which classifies tweets as racist/sexist or normal.
# Dataset Inference
- the Training data consisted of 31962 tweets labelled as 0 or 1 , 1 corresponding to racist/sexist and 0 as normal.
- Test set consisted 17917 tweets.
- The Tweets were not clean so prepocessing had to be done in order to extract useful features.
# Workflow
- Data Preprocessing
- Exploratory Data Analysis
- Feature Extraction using :
  - Bag of Words
  - TfIdf
  - Word2Vec
- Model Building
  - Logistic Regression
  - SVM
  - Random Forest
  - XGBoost
- Fine Tuning
# Data Preprocessing
- Removed "@", emojis, special characters using regular expressions
- Removed Stopwords using nltk
- Stemming the tweet to replace words with similar meaning to reduce irregularities using PorterStemmer
# Exploratory Data Analysis
- Visualised words which occured most in the corpus of tweets using WordCloud
- Also same visualisation was done on corpus specific to normal and racist/sexist tweets
# Feature Extraction
- Bag of Words applied keeping top 1000 words as the main features
- TfIdf
- Word2Vec was used as it is famous for its ability to capture contextual meanings in a sentence.
# Model Building
- Logistic Regression Classification
  - f1 score of bag of words features on logistic regression : 0.57
  - accuracy score of bag of words features on logistic regression : 0.946
  - f1 score of tfidf features on logistic regression : 0.58
  - accuracy score of tfidf features on logistic regression : 0.946
  - f1 score of word2vec features on logistic regression : 0.58
  - accuracy score of word2vec features on logistic regression : 0.943
- SVM (rbf kernel gave best results)
  - f1 score of bag of words features on SVM : 0.58
  - accuracy score of bag of words features on SVM : 0.948
  - f1 score of tfidf features on SVM : 0.62
  - accuracy score of tfidf features on SVM : 0.949
  - f1 score of word2vec features on SVM : 0.59
  - accuracy score of word2vec features on SVM : 0.945
- Random Forest Classifier
  - f1 score of bag of words features on Random Forest : 0.58
  - accuracy score of bag of words features on Random Forest : 0.941
  - f1 score of tfidf features on Random Forest : 0.60
  - accuracy score of tfidf features on Random Forest : 0.953
  - f1 score of word2vec features on Random Forest : 0.59
  - accuracy score of word2vec features on Random Forest : 0.955
- XGBoost
  - f1 score of bag of words features on XGBoost : 0.56
  - accuracy score of bag of words features on XGBoost : 0.949
  - f1 score of tfidf features on XGBoost : 0.59
  - accuracy score of tfidf features on XGBoost : 0.952
  - f1 score of word2vec features on XGBoost : 0.65
  - accuracy score of word2vec features on XGBoost : 0.956
# Fine Tuning
 - fine tuning xgboost on word2vec as it has given best f1 score till now
 - fine tuning resulted in better f1 score of 0.69 and accuracy of 0.96
