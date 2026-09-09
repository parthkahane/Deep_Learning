# Assignment 2 – Wine Classification Using MLP

## Objective

The objective of this assignment is to implement a **Multi-Layer Perceptron (MLP) Neural Network** for classifying samples from the Wine dataset.

## Dataset

The **Wine dataset** from Scikit-learn is used for this assignment. The dataset contains chemical properties of wine samples belonging to three different classes.

The dataset is divided into:

* 80% training data
* 20% testing data

## Steps Performed

1. Imported the required libraries from Scikit-learn.
2. Loaded the Wine dataset using `load_wine()`.
3. Separated the dataset into input features (`X`) and target labels (`y`).
4. Split the data into training and testing sets using `train_test_split()`.
5. Standardized the features using `StandardScaler`.
6. Created an MLP neural network with two hidden layers.
7. Used ReLU as the activation function and Adam as the optimizer.
8. Trained the model using the training dataset.
9. Generated predictions for the test dataset.
10. Evaluated the model using:

* Accuracy
* Confusion Matrix
* Classification Report

The implementation in the assignment follows these steps and uses an MLP with two hidden layers containing 10 neurons each.

## Result

The model achieved an **accuracy of 100%** on the test dataset.

The confusion matrix shows that all 36 test samples were classified correctly, with no incorrect predictions.

## Conclusion

The assignment demonstrates the use of a **neural network-based classification model** for the Wine dataset. Feature standardization was performed before training, and the trained MLP model successfully classified the test samples with 100% accuracy.
