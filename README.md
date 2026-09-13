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

### Part 4 — Optimiser Comparison

* Compared four optimisers:
  * SGD
  * SGD with Momentum
  * RMSProp
  * Adam
* Tested the optimisers using a common learning rate.
* Repeated the experiment using a tuned learning rate for each optimiser.
* Compared:
  * Epochs to reach 85% validation accuracy
  * Final validation accuracy
  * Wall-clock training time
* Plotted the training loss curves for all four optimisers.
* RMSProp achieved strong validation performance and fast convergence.

### Part 5 — Forcing Overfitting

* Reduced the training set to 2,000 samples.
* Increased the network size to four hidden layers with 512 units each.
* Used ReLU activation in the hidden layers.
* Trained the model until it achieved very high training accuracy.
* The model achieved:
  * Training accuracy: 99.25%
  * Validation accuracy: 82.44%
  * Generalisation gap: 16.81 percentage points
* The large gap between training and validation accuracy demonstrated overfitting and high variance.
* Plotted training and validation loss to show where overfitting began.

### Part 6 — Regularisation Study

* Applied different regularisation techniques to the overfitted model.
* Tested L2 weight decay using multiple lambda values.
* Applied L1 regularisation and measured the percentage of weights below 1e-3.
* Tested dropout using rates of 0.2, 0.4 and 0.6.
* Applied batch normalisation.
* Used early stopping with a patience value of 5.
* Applied data augmentation using random horizontal flipping and small random rotations.
* Increased the training data to 10,000 and 20,000 samples.
* Dropout with a rate of 0.6 produced the largest reduction in the generalisation gap.
* Increasing the training data also improved validation accuracy.

### Part 7 — Hyperparameter Tuning

* Used random search with 12 different configurations.
* Applied 5-fold stratified cross-validation.
* Tuned three hyperparameters:
  * Learning rate
  * Hidden layer width
  * Dropout rate
* The best configuration was:
  * Learning rate: 0.001
  * Hidden width: 256
  * Dropout rate: 0.2
* The selected configuration achieved a mean cross-validation accuracy of 88.90%.

### Final Model Evaluation

* Retrained the selected model using the chosen configuration.
* Evaluated the model once on the untouched Fashion-MNIST test set.
* Final test results:
  * Test accuracy: 89.57%
  * Macro precision: 89.59%
  * Macro recall: 89.57%
  * Macro F1: 89.53%
* Generated a confusion matrix for the final model.
* The final test accuracy improved by 2.16 percentage points compared with the Part 2 baseline accuracy of 87.41%.

## Final Results

The final tuned neural network achieved a test accuracy of **89.57%** on Fashion-MNIST.

The experiments showed that model architecture, activation functions, optimisation, regularisation, training-data size, and hyperparameter tuning all affect neural network performance and generalisation.

## Dataset

**Fashion-MNIST** was used for the classification experiments.

A separate **Diabetes dataset** from Scikit-learn was used for the regression experiment.

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
