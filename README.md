# Deep-Learning-model-for-Self-Driving-using-Udacity-s-slef-driving-car-simulator

## Introduction

In this project, we train a Deep Learning Model for self-driving using PyTorch.

Main Libraries: Pytorch, OpenCV, Numpy.

## Files
**self_driving.ipynb** contains the code for model training.



**Data.zip** contains the data files.
Data can be found in the following google drive link.
https://drive.google.com/file/d/1bzazEgZoKHf_qCO7NJFAIXCdoLXT71Fx/view?usp=sharing

## Data Collection and usage

- In order to collect the dataset we relied on Udacity's Self-driving car simulator. It has a built-in mechanism to record the driving data. 
- The dataset contains 3 images from left, right, and center cameras along with the corresponding steering, acceleration, and braking inputs.
- We train a deep learning model, and use the model to predict the controls of the vehicle.
- Once the model is trained, it needs to be connected to the Udacity's simulator for testing.
- Instructions of working with the simulator can found on the simulator's github page, and various other articles around the internet.

## Data Preperation steps

- Splitting the dataset into training and test samples.
- Data Augmentation has been used for better model generalization. (flipping the images, and modifying the corresponding steering values)
- Image Normalizarion.

## Model Architecture

- The model contains Convolution Layers with a dropout of 0.25 at the end to avoid over fitting.
- The convolution layers are followed by a fully connected network.
- Activation function used: ELU
- Optimizer: Adam
- Loss function: Mean Squared Error (MSE)
- Epochs: 25.
