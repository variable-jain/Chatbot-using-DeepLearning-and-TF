# Chatbot-using-DeepLearning-and-TF
Hi, In this project, I implemented a chatbot using reddit comments may2015 dataset on kaggle using se2seq model with attention mechanism

## The Dataset
The dataset has been obtained from kaggle reddit comments May2015 dataset. 
https://www.kaggle.com/reddit/reddit-comments-may-2015.<br>
This data is in the form of a .sqlite table.

We ran the script **create_database.py** to filter the data based on several filters and convert the sqlite file to a databse(.db) file. At this point we have >3M question-answers pairs in the database.

Further, we ran the script **create_train_test_set.py** to convert the database to training and test .txt files, each for questions and answers.

## The Model
We used a *Seq2Seq model* using *Keras* with tensorflow as backend with a *Bidirectional LSTM(**L**ong **S**hort **T**erm **M**emory)* layer with an attention mechanism. We trained the model on our data to generate cool responses for common questions.