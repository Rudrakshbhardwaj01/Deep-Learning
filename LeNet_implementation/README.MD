# LeNet-5 CNN using Keras

This project implements the **LeNet-5 convolutional neural network** using TensorFlow/Keras.  
It is designed for grayscale images like the MNIST dataset.

---

## Model Architecture

1. **Conv2D**: 6 filters, 5x5 kernel, `tanh` activation  
2. **AveragePooling2D**: 2x2 pool size, stride 2  
3. **Conv2D**: 6 filters, 5x5 kernel, `tanh` activation  
4. **AveragePooling2D**: 2x2 pool size, stride 2  
5. **Flatten**  
6. **Dense**: 120 neurons, `tanh` activation  
7. **Dense**: 84 neurons, `tanh` activation  
8. **Dense**: 10 neurons, `softmax` activation

---