# Deep-Learning-Neural-Networks
This repository contains the implementation and experiments for a deep learning study covering neural network training, activation functions, loss functions, and regression.

## Contents

### Part 1 — Backpropagation From Scratch

* Implemented a two-layer MLP using NumPy.
* Implemented forward propagation, backpropagation, and gradient descent manually.
* Trained the model on a subset of Fashion-MNIST.
* Verified the manually calculated gradients against PyTorch gradients.

### Part 2 — Activation Function Study

* Compared four hidden-layer activation functions:

  * Sigmoid
  * Tanh
  * ReLU
  * Leaky ReLU
* Compared validation loss and accuracy.
* Analyzed gradient magnitudes for sigmoid and ReLU.
* Checked the percentage of dead ReLU units.

### Part 3 — Loss Function Study

* Compared categorical cross-entropy and mean squared error for Fashion-MNIST classification.
* Compared their training behavior and test accuracy.
* Analyzed why cross-entropy is more suitable for classification.

### Part 4 — Regression

* Trained a small MLP on a tabular regression dataset.
* Evaluated the model using:
  * MSE
  * RMSE
  * MAE

## Dataset

**Fashion-MNIST** was used for the classification experiments.
A tabular regression dataset was used separately for the regression experiment.

## Technologies

* Python
* NumPy
* TensorFlow / Keras
* PyTorch
* Scikit-learn
* Matplotlib
* Pandas

## Reproducibility

A fixed random seed was used throughout the experiments.
**Random seed: 42**
The notebook contains the complete code, outputs, results, and plots needed to reproduce the experiments.

