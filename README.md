# English-to-French
Converting English to French using LSTM and RNN.
The Dataset is taken from "https://www.kaggle.com/datasets/digvijayyadav/frenchenglish"
![ETF](https://user-images.githubusercontent.com/102272183/213648773-b84a9247-91a2-4a12-b564-0545fc406f58.png)

# TensorFlow Seq2Seq Model for Translation
## Introduction
This repository contains code for training a seq2seq model for language translation using TensorFlow's Keras API. The model is trained on a dataset of French to English sentence pairs, and is able to generate French translations for new English sentences.

## Requirements
The code in this repository was developed using TensorFlow 2.x and requires the following packages:

tensorflow

numpy

## Data
The data used to train the model is a dataset of French to English sentence pairs. The dataset can be found in the input/frenchenglish/fra.txt file. The data is preprocessed to encode each sentence as a sequence of characters, and to create training examples that consist of pairs of input sequences (French sentences) and target sequences (English translations).

## Preprocessing
The preprocessing steps include:

Reading the data from the fra.txt file

Splitting the data into input texts (French sentences) and target texts (English translations)

Determining the unique characters in the input and target texts

Encoding the input and target texts as numerical sequences using a one-hot encoding scheme

Padding the sequences to the same length, so that they can be processed by the neural network

## Model
The model is a seq2seq model with an encoder-decoder architecture. The encoder is a single layer LSTM that encodes the input sequence into a hidden state representation. The decoder is also a single layer LSTM that uses the hidden state representation and the target sequence to generate the output sequence. The final layer of the decoder is a dense layer with a softmax activation function that predicts the probability distribution over the output characters.

## Training
The model is trained using the fit method from TensorFlow's Keras API. The training process uses the preprocessed training data to update the model's weights, and is run for 100 epochs with a batch size of 64. The model is trained using the categorical cross-entropy loss and the Adam optimizer.

## Usage
To train the model, simply run the code in this repository. The trained model can then be used to generate English translations for new French sentences.We can also change some code to get english from french.

## Conclusion
This code provides a basic example of how to train a seq2seq model for language translation using TensorFlow's Keras API. The code can be extended and modified to address different translation tasks and to experiment with different model architectures.

