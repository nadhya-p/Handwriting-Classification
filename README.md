# Handwriting-Classification
This repository contains an example demonstration of how machine learning techniques can be used to classify handwritten letters provided by the [EMNIST dataset.](https://arxiv.org/abs/1702.05373)

The EMNIST-letters dataset contains 145,600 handwriting samples balanced across 26 classes (one class per English letter). The purpose of this repository is to train a convolutional neural network with less than 1 million parameters to classify uppercase and lowercase handwritten letters from this dataset. Various network architectures are compared to determine the most efficient network type. 
 

## Dependancies
This project uses tensorflow and extended keras datasets
* pip install tensorflow
* pip install extra-keras-datasets

## Workflow plans
* import data in a way that can be run on any computer (done)
* load in the letters dataset (done)
* visualize the data to make sure sizing is correct (done)
* use train_test_split to create trainining in test sets (done)
* create neural network: try basic  model, resnet, mobilenet, adding SE block etc (in progress)
* visualize accuracy of each and plot
* compare accuracy and cross entropy loss for each
* draw conclusions about the best model type

