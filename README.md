# GENDER-DETECTION-AND-AGE-DETECTION
This project combines gender and age detection using machine learning techniques. It aims to predict individuals' genders and estimate their ages from given data or images. These predictions have numerous applications, from personalized marketing to demographic analysis.
# Gender and Age Detection

This repository contains code for a gender and age detection model using deep learning. The model is trained on a dataset of images and can predict both the gender and age of a person from a given image. Below, you'll find information on how to set up and use this code.

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Data Preprocessing](#data-preprocessing)
4. [Building the Neural Networks](#building-the-neural-networks)
5. [Training and Evaluation](#training-and-evaluation)
6. [Usage](#usage)
7. [Contributing](#contributing)

## Introduction

This project aims to build a gender and age detection model using deep learning techniques. The model takes an image as input and predicts the gender (male or female) and the age group (a range of ages) of the person in the image.

## Dataset

The dataset used for training the model is named "age_gender.csv." It contains the following columns:

- `age`: Age label of the person in the image.
- `ethnicity`: Ethnicity label of the person.
- `gender`: Gender label of the person (0 for male, 1 for female).
- `pixels`: Pixel values of the image.

Here are some statistics about the dataset:

- Total samples: 23,705
- Age labels: 104 unique values
- Ethnicity labels: 5 unique values
- Gender labels: 2 unique values (0 for male, 1 for female)

## Data Preprocessing

The data preprocessing steps include:

- Removing the "img_name" column from the dataset.
- Splitting the dataset into features (X) and target variables (y) for gender, age, and ethnicity.
- Normalizing pixel values to the range [0, 1].
- Reshaping images to the size (48x48x1).
- Performing data augmentation using the ImageDataGenerator.

## Building the Neural Networks

Three separate neural networks are built for predicting gender, age, and ethnicity. Each network consists of convolutional layers, batch normalization, max-pooling layers, dropout layers, and dense layers. The models are compiled using appropriate loss functions and optimizers.

## Training and Evaluation

The models are trained using a portion of the dataset and evaluated on another portion. Early stopping and learning rate reduction callbacks are used to prevent overfitting and improve training efficiency. Model performance is assessed using accuracy and loss metrics.

## Usage

To use this code, follow these steps:

1. Install the required libraries mentioned in the code (e.g., TensorFlow, pandas, matplotlib).
2. Download the dataset (age_gender.csv) and place it in the same directory as the code.
3. Run the code sections step by step, starting from data loading, preprocessing, model building, training, and evaluation.
