# Sentiment Analysis on US Airline Reviews

This project performs sentiment analysis on US airline reviews using TensorFlow and Keras. The primary goal is to classify tweets about US airlines as positive or negative.

## Project Overview

This project uses a dataset of tweets about US airlines, including their sentiment (positive or negative). The tweets are preprocessed and tokenized, and a Long Short-Term Memory (LSTM) neural network is built and trained to classify the sentiment of the tweets.

## Dataset

The dataset used for this project is the `Tweets.csv` file, which contains tweets about US airlines along with their sentiment. The sentiment labels are 'positive' and 'negative'.

## Workflow

1. **Data Loading and Preprocessing:**
   - Load the dataset using pandas.
   - Filter out tweets with a neutral sentiment.
   - Factorize sentiment labels to convert them into numerical values.
   - Tokenize the tweets and pad the sequences to ensure uniform input length for the LSTM model.

2. **Model Building:**
   - Create an embedding layer to convert words into dense vectors of fixed size.
   - Add a spatial dropout layer to prevent overfitting.
   - Add an LSTM layer with dropout and recurrent dropout.
   - Add a dense layer with a sigmoid activation function for binary classification.

3. **Model Training:**
   - Compile the model using binary cross-entropy loss and the Adam optimizer.
   - Train the model with the preprocessed data, using 20% of the data for validation.
   - Plot the accuracy and loss for both training and validation sets.

4. **Prediction Function:**
   - Define a function to predict the sentiment of a given text input.
   - Tokenize and pad the input text, then use the trained model to predict its sentiment.
