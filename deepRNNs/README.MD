# Deep RNN, LSTM, and GRU

This notebook showcases the implementation of **Deep Recurrent Neural Networks (RNNs)** using Keras, covering three major architectures — **Deep RNN**, **Deep LSTM**, and **Deep GRU**. These models are designed to process and learn from sequential data such as text, where temporal order and context are essential. By stacking multiple recurrent layers, the networks can capture both short-term and long-term dependencies effectively.

## Overview
- **Deep RNN:** Built using stacked `SimpleRNN` layers to model sequential relationships and learn temporal patterns from data.  
- **Deep LSTM:** Utilizes multiple `LSTM` layers to preserve information over longer sequences and reduce vanishing gradient issues.  
- **Deep GRU:** Features stacked `GRU` layers for efficient training with performance comparable to LSTMs but with fewer parameters.

## Key Concepts
- Demonstrates the use of `return_sequences=True` for stacking multiple recurrent layers.  .  
- Highlights differences in learning behavior and performance among RNN, LSTM, and GRU architectures.
