Project Overview

This project implements a Convolutional Neural Network (CNN) for classifying natural scene images from the Intel Image Classification dataset. The dataset contains over 25,000 images divided into 6 classes:

Buildings

Forest

Glacier

Mountain

Sea

Street

The workflow includes data preprocessing, CNN model building, training, evaluation, and visualization of predictions.

Dataset

Source: Intel Image Classification Dataset on Kaggle

Directory structure:

dataset/
  ├─ seg_train/
  ├─ seg_test/

Project Steps

Data Preprocessing

Resize images to 150×150 pixels.

Normalize pixel values to [0, 1].

Split training data into train and validation sets (80%-20%).

Apply data augmentation (rotation, flip, zoom, shift).

CNN Model

Minimum 3 convolutional layers with ReLU activations.

MaxPooling layers after convolution blocks.

Fully connected Dense layer with Dropout for regularization.

Softmax output layer for multi-class classification.

Training

Optimizer: Adam

Loss: Categorical Crossentropy

Callbacks: EarlyStopping and ModelCheckpoint (native Keras format .keras)

Monitor validation loss to save the best model.

Evaluation

Compute test accuracy.

Generate classification report (precision, recall, F1-score per class).

Plot confusion matrix.

Prediction Visualization

Display at least 10 random test images with predicted vs. actual labels.
