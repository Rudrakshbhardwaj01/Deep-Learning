# LSTM-Based Next Word Predictor

This project implements an LSTM-based next word predictor in Python using Keras. It is trained on a small dataset of casual English sentences and generates text one word at a time deterministically using the most probable next word. The model uses a tokenizer to convert words into integer sequences, an embedding layer to represent words in a dense vector space, and an LSTM layer to capture the context of sequences, allowing it to predict coherent text based on a given seed word or phrase.
