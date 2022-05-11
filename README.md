# Handwriting-Classification
This repository contains an example demonstration of how machine learning techniques can be used to classify handwritten letters provided by the [EMNIST dataset.](https://arxiv.org/abs/1702.05373)

The EMNIST-letters dataset contains 145,600 handwriting samples balanced across 26 classes (one class per English letter). The purpose of this repository is to train a convolutional neural network to classify uppercase and lowercase handwritten letters from this dataset. Images of various clarity will be fed into the network to determine how image blurriness affects network learning. 
 

## Dependancies
This project uses tensorflow and extended keras datasets
* pip install tensorflow
* pip install extra-keras-datasets

The notebook in this repository describes the step by step process to create this neural netwrork and analyze its results. 

### Table of Contents
* Image Preparation
* Training a CNN on the original EMNIST images
* Analyzing accuracy of the CNN
* Image Blurring 
  * kernel sizes of 5, 10, 20 and 30 are used
* Analysis of network accuracy based on image blurriness

## Image Preparation
To get the images, we downloaded handwritten letters from the EMNIST - letters dataset. We immediately split the images into a training set and a test set.
The training set was duplicated 3 times and images were blurred using a kernel size of 5, 10 or 20. Different kernel sizes were used to determine how blurring affects the accuracy of our network classification. The first 30 images of each training set were printed for visual confirmation of different levels of blurriness. The images were then reshaped and the RGB codes were normalized so the size of each image was 28 x 28 x 1. Lastly, one hot encoding was performed to convert category names to numbers. 

## Network Creation
A simple convolutional neural network was created to process the images. The network contains 4 blocks, and each block adds 2 2D convolutional layers to the model. The end of each block adds a Max pooling layer with a pool size of 2x2. The layers are then flattened before a dense layer of 256 units is added. Finally, a dense layer of 27 units is added so that the number of possible outputs equals the number of possible categories. The adam optimizer was used, and categorical crossentropy was used to calculate the loss for each epoch. 

The network was trained on the original EMNIST letters, as well as the 3 training sets conisiting of blurred images. 

## Analyzing the Results






