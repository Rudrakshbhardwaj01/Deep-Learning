# Hyperparameter Tuning with Keras Tuner

Automated hyperparameter tuning for a binary classification neural network using Keras Tuner.

## Overview

This project uses Keras Tuner to automatically find the best neural network architecture by testing different combinations of layers, units, activation functions, dropout rates, and optimizers.

## Tunable Hyperparameters

- **Number of Layers**: 1 to 10 hidden layers
- **Units per Layer**: 8 to 128 (increments of 8)
- **Activation Functions**: relu, tanh, sigmoid
- **Dropout Rate**: 0.1, 0.2, 0.3, 0.4
- **Optimizer**: adam, adadelta, sgd

## Installation
```bash
pip install tensorflow keras-tuner
```

## Usage
```python
from keras_tuner import RandomSearch

# Create tuner
tuner = RandomSearch(
    build_model,
    objective='val_accuracy',
    max_trials=10,
    directory='tuning_results',
    project_name='hp_tuning'
)

# Search for best hyperparameters
tuner.search(X_train, y_train, epochs=10, validation_data=(X_val, y_val))

# Get the best model
best_model = tuner.get_best_models(num_models=1)[0]

# View best hyperparameters
best_hp = tuner.get_best_hyperparameters(num_trials=1)[0]
print(best_hp.values)
```

## Model Configuration

- **Input Dimension**: 8 features
- **Output Layer**: Sigmoid activation for binary classification
- **Loss Function**: Binary crossentropy
- **Metric**: Accuracy
- **Regularization**: Dropout applied after each hidden layer

## How It Works

The `build_model` function creates a Sequential model with a variable number of layers. Each layer has its own tunable parameters for units, activation, and dropout. The tuner tests different combinations to find the best performing model.