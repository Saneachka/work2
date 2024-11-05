# Fashion MNIST Image Classification

This repository contains a TensorFlow/Keras project aimed at classifying images from the Fashion MNIST dataset using Convolutional Neural Networks (CNNs). Two different CNN architectures are implemented and compared to analyze performance improvements achieved with regularization and deeper networks.

Table of Contents
Project Overview
Requirements
Dataset
Model Architecture
Training
Results
Usage
Conclusion
Project Overview
This project involves image classification of the Fashion MNIST dataset, consisting of 28x28 grayscale images of fashion items. The project explores two CNN architectures:

Model 1: A simple CNN without regularization.
Model 2: An enhanced CNN with dropout layers and pooling, to reduce overfitting.
Requirements
This code was developed using Python 3. The following libraries are required:

tensorflow >= 2.17.0
numpy
matplotlib
scikit-learn

Dataset
The Fashion MNIST dataset consists of:

Training set: 60,000 images
Test set: 10,000 images
Each image belongs to one of ten classes, labeled as follows:

T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot

Model Architecture
Model 1: Basic CNN
Layers: 3 Convolutional layers followed by 2 Dense layers
Activation: ReLU for hidden layers, Softmax for the output layer
Model 2: Improved CNN with Regularization
Layers: 3 Convolutional layers, pooling layers, Dropout layers for regularization, followed by Dense layers
Activation: ReLU for hidden layers, Softmax for the output layer
Dropout: 20% to reduce overfitting
Training
To train the models:

Data Preprocessing: Normalize the images by scaling pixel values between -0.5 and 0.5, reshape for CNN input, and one-hot encode labels.
Training Process: Run for 10 epochs with categorical_crossentropy loss and adam optimizer. The batch size is set to 32.

Results
Model 1: High training accuracy but significant overfitting. Validation accuracy stabilizes around ~90.6%.
Model 2: Reduced overfitting with added dropout layers and pooling, achieving similar validation accuracy (~91%) with a lower validation loss.
Accuracy and loss curves for both training and validation sets are plotted to visualize overfitting and performance stability.

Conclusion
Model 2 demonstrates improved generalization with dropout layers, reducing overfitting compared to Model 1. This project shows the effectiveness of CNNs in image classification tasks and highlights the role of regularization in model performance.

