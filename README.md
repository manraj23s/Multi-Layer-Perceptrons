# Multi-Layer Perceptron Networks Report

This project explores the application of Multi-Layer Perceptrons (MLPs)—a class of artificial neural networks—across three distinct classification tasks: employee attrition (HR data), handwritten digit recognition (MNIST), and flower species identification (IRIS). MLPs are particularly suited to problems with non-linear decision boundaries, enabling robust performance on complex datasets where linear classifiers are inadequate.

---

## What is an MLP?

A Multi-Layer Perceptron consists of one or more hidden layers of interconnected neurons, each applying an activation function to their inputs and passing results forward. The final output layer produces a set of probabilities for possible classes, enabling predictions for both binary and multi-class classification problems. MLPs are powerful because they:

- Can learn and model complex, non-linear relationships in data.
- Are robust to noise and irrelevant features in input data.
- Scale effectively with more hidden layers and neurons to handle larger, more complex datasets.

---

## Project Overview

### Model 1: HR Attrition Prediction

- **Dataset:** HR data with variables like salary, commute time, department, evaluations, satisfaction levels, and more.
- **Goal:** Predict whether an employee is likely to leave the company (binary classification).
- **Process:**
  - Data preprocessing included converting categorical variables (salary, department) to numerical.
  - Visualizations revealed the data was not linearly separable.
  - Sklearn's `MLPClassifier` was used with two hidden layers (20 and 19 neurons), rectilinear activation, learning rate 0.01, and the 'adam' solver.
- **Result:** Achieved **95.17% accuracy** in predicting employee attrition.

### Model 2: MNIST Handwritten Digit Recognition

- **Dataset:** MNIST—60,000 training and 10,000 test images of handwritten digits (0–9), each 28x28 pixels.
- **Goal:** Classify digits into one of ten classes (multi-class classification).
- **Process:**
  - Data normalized to [0, 1] range.
  - Built an MLP model with TensorFlow/Keras: two hidden layers (200 and 100 neurons, sigmoid activation), and a final output layer of 10 neurons.
  - Used 'adam' optimizer and sparse categorical cross-entropy loss.
  - Trained for 20 epochs with a batch size of 2,000 samples.
- **Result:** Achieved **94.05% accuracy** in digit classification.

### Model 3: IRIS Flower Species Classification

- **Dataset:** IRIS—150 samples, 4 features (sepal length/width, petal length/width), 3 species.
- **Goal:** Classify flowers as Setosa, Versicolor, or Virginica (multi-class classification).
- **Process:**
  - Explored and visualized data; clusters were not linearly separable.
  - Used Sklearn's `MLPClassifier` with two hidden layers (5 and 4 neurons), 'lbfgs' solver, and regularization to prevent overfitting.
- **Result:** Achieved **97.37% accuracy**, misclassifying only one sample.

---

## Key Insights

- **MLPs are highly effective for a variety of classification problems, especially where data is not linearly separable.**
- **Careful preprocessing, model tuning, and appropriate architecture selection contribute significantly to model performance.**
- **Neural networks can generalize well to different data types and domains, from HR analytics to image and species recognition.**

---

**Author:** Manraj Singh  
**Contact:** [manraj23singh@gmail.com](mailto:manraj23singh@gmail.com)
