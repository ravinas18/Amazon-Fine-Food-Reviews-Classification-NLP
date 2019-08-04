# Amazon-Fine-Food-Reviews-Classification-NLP
## Abstract
The project aimed at building best working model for classification of positive and negative reviews.  
Apply Logistic Regression algorithm using each technique.

## Dataset 
The dataset used is https://www.kaggle.com/snap/amazon-fine-food-reviews.  
This dataset consists of reviews of fine foods from amazon. The data span a period of more than 10 years, including all ~500,000                reviews up to October 2012. Reviews include product and user information, ratings, and a plain text review.  It also includes reviews            from all other Amazon categories.

## Procedure to execute classification is as follows:
_Step1_: Data Pre-processing is applied on given amazon reviews data-set.And Take sample of data from dataset because of computational limitations.  
_Step2_: Time based splitting on train and test datasets.  
_Step3_: Apply Feature generation techniques(Bow,tfidf).  
_Step4_: Apply Logistic Regression algorithm using each technique.  
_Step5_: To find lambda using gridsearch cross-validation and random cross-validation.  
_Step5_: L2 regularization.  
_Step6_: Feature Importance for postive and Negative reviews    
         1. Most Important Feature.  
         2. Bar plot of top 15 Important Features.  
### Preprocessing Review Text:
Our data requires some preprocessing before we go on further with analysis and making the prediction model.
Hence in the Preprocessing phase we do the following in the order below:-
         1.Begin by removing the html tags.  
         2.Remove any punctuations or limited set of special characters like , or . or # etc.  
         3.Check if the word is made up of english letters and is not alpha-numeric.  
         4.Check to see if the length of the word is greater than 2 (as it was researched that there is no adjective in 2-letters).  
         5.Convert the word to lowercase.  
         6.Remove Stopwords.  
         7.Finally Snowball Stemming the word (it was obsereved to be better than Porter Stemming).  
         8.After which we collect the words used to describe positive and negative reviews. 
### Splitting Training and Testing dataset based on Time:
The column Time is based on unix timestamp.The unix time stamp is a way to track time as a running total of seconds and In time technically does not change no matter where you are located on the globe. This is very useful to computer systems for tracking and sorting dated information in dynamic and distributed applications both online and client side. https://www.unixtimestamp.com/ .  
So here,time conversion is not necessary to process on amazon data.
### Methods to convert text into vector:
Methods:  
* Bag of Words.    
* Tf-idf.    
### Optimal Lambda for Logistic Regression:
lambda_LR is written function to calculate the optimal lambda value for Logistic Regression.
GridsearchCV and RandomsearchCV method are used to obtain optimal lambda with L2 penality,different scoring options(e.g,accuracy,precision,recall and F1-score) and broad range of lambda.  
Best parameter lambda and penalty for which model performs very well is obtained. 




