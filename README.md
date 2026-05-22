ml-fundamentals
A collection of machine learning projects built during undergraduate study at Manipal Institute of Technology. Each notebook is self-contained and covers a different concept, from basic regression through to convolutional neural networks.
Projects

1. Linear Regression
`Linear_Regression_model.ipynb`
Implements linear regression from scratch using NumPy. Covers the least squares formulation, gradient descent optimisation, and comparison against scikit-learn's built-in implementation. Includes visualisation of the regression line and residuals.
`NumPy` `Matplotlib` `scikit-learn`



2. Perceptron on MNIST
`perceptron on mnist.ipynb`
A single-layer perceptron trained on the MNIST handwritten digit dataset. Demonstrates the limitations of a linear classifier on a non-linearly separable problem and motivates the need for deeper architectures.
`NumPy` `scikit-learn` `Matplotlib`




3. Neural Network for Binary Classification with Custom Backpropagation
# 2-Class Spiral Dataset Neural Network

A feedforward neural network built from scratch with NumPy to classify a 2-class spiral dataset — a classic non-linearly separable problem.

## Overview

This project implements a shallow neural network (1 hidden layer) entirely from first principles — no Keras, no PyTorch. It demonstrates forward propagation, cost computation, and backpropagation on a synthetically generated spiral dataset.

## Dataset

The spiral dataset is generated procedurally: 400 points split evenly into two interlocking spiral classes. It is intentionally non-linearly separable, making it a good benchmark for testing whether a network can learn complex boundaries.

## Model Architecture

| Layer | Details |
|---|---|
| Input | 2 features (x1, x2) |
| Hidden | 4 units, tanh activation |
| Output | 1 unit, sigmoid activation |

## Training

| Hyperparameter | Value |
|---|---|
| Optimizer | Gradient Descent |
| Learning Rate | 0.01 |
| Epochs | 10,000 |

Cost is printed every 1,000 iterations to track convergence.

## Results

The model learns a non-linear decision boundary that separates the two spiral classes. Sample cost trajectory:

```
Epoch 0:    ~0.693
Epoch 9000: ~0.459
```

## Requirements

```
numpy
matplotlib
sklearn  (imported but unused — standard dependency)
```

## Key Concepts Demonstrated

Forward propagation, sigmoid and tanh activations, binary cross-entropy loss, backpropagation, gradient descent parameter updates, and decision boundary visualisation.



4. Fashion MNIST Image Classifier

A neural network built with TensorFlow/Keras to classify clothing items from the [Fashion MNIST](https://github.com/zalandoresearch/fashion-mnist) dataset.

## Overview

This project trains a simple feedforward neural network to recognize 10 categories of clothing — T-shirts, trousers, pullovers, dresses, coats, sandals, shirts, sneakers, bags, and ankle boots — achieving ~88.5% accuracy on the test set.

## Model Architecture

| Layer | Details |
|---|---|
| Flatten | Input: 28×28 grayscale images |
| Dense | 128 units, ReLU activation |
| Dense | 10 units (output logits) |

Training uses the **Adam** optimizer with **Sparse Categorical Crossentropy** loss over **10 epochs**.

## Results

| Split | Accuracy |
|---|---|
| Train | ~91.1% |
| Test | ~88.5% |

## Requirements

```
tensorflow >= 2.17.0
numpy
matplotlib
```

## Usage

Run the notebook end-to-end. The model loads Fashion MNIST automatically via `tf.keras.datasets`, normalizes pixel values to `[0, 1]`, trains, evaluates, and visualizes predictions with color-coded confidence charts (blue = correct, red = incorrect).



5. MNIST Digit Classification with CNN and Early Stopping
MNIST Digit Classification with CNN and Early Stopping.ipynb
A two-block convolutional neural network trained on MNIST. The architecture stacks two Conv2D + MaxPooling layers (32 and 64 filters respectively), followed by a dense layer of 64 units and a softmax output over 10 classes (121,930 total parameters). Training uses RMSProp with categorical cross-entropy and early stopping (patience=5, monitoring validation loss), halting at epoch 13 with best weights restored from epoch 8. Achieves 98.95% validation accuracy. Plots training and validation loss and accuracy curves across epochs.
TensorFlow Keras NumPy Matplotlib



6. Library Management System
`librarymanagementsys.ipynb`
A Python-based library management system covering object-oriented design: classes for books, members, and borrowing records, with search and availability tracking.
`Python`
How to run
All notebooks can be opened directly in Google Colab or run locally with Jupyter.
Local setup:

```bash
pip install numpy matplotlib scikit-learn tensorflow
jupyter notebook

```

Google Colab: click the notebook file on GitHub, then replace `github.com` in the URL with `githubtocolab.com` to open it directly in Colab.
Related repositories

* [quantum-measurement-pipeline](https://github.com/jazz-dev/quantum-measurement-pipeline) — Python pipeline for quantum hardware measurement automation
* [Neural-Quantum-States-Reversible-Computing](https://github.com/jazz-dev/Neural-Quantum-States-Reversible-Computing) — Neural variational wavefunction diagnostics (ICHM 2026)
📧 jassmairasingh@gmail.com this is a readme file fo rmy ml fundamentals, jassmaira here, i want you to make some changes in it
