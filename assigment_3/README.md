# Assignment 3 – Fashion-MNIST Neural Network Experiment

## Objective

The objective of this assignment is to build and evaluate a **Neural Network** for image classification using the **Fashion-MNIST dataset**.

The assignment also studies how different **learning rates** and **numbers of epochs** affect the performance of the neural network.

## Dataset

The **Fashion-MNIST dataset** is used for this assignment.

It contains grayscale images of different fashion items. Each image is originally represented as a **28 × 28 pixel image**.

Before training, the images are:

* Reshaped from 28 × 28 pixels into 784 values.
* Normalized by dividing the pixel values by 255.

## Neural Network Architecture

The neural network consists of:

* Input layer with 784 input features
* First hidden layer with 128 neurons
* Second hidden layer with 64 neurons
* ReLU activation function in the hidden layers
* Output layer with 10 neurons
* Softmax activation in the output layer

The model is trained using the **Adam optimizer**.

## Experiments Performed

### 1. Learning Rate Experiment

Three different learning rates are tested:

* 0.1
* 0.01
* 0.001

Each model is trained for 5 epochs and evaluated on the test dataset.

The resulting accuracies are compared using a graph.

### 2. Epoch Experiment

Three different numbers of epochs are tested:

* 5
* 10
* 20

For this experiment, the learning rate is fixed at **0.001**.

The test accuracy for each number of epochs is recorded and compared using a graph.

### 3. Training and Validation Performance

A final model is trained using:

* Learning rate: 0.001
* Epochs: 20
* Batch size: 128
* Validation split: 20%

Training and validation accuracy are plotted to observe the model's learning behavior.

Training and validation loss are also plotted to analyze how the model's error changes during training.

## Model Evaluation

The final model is evaluated using:

### Accuracy

Measures the percentage of test images classified correctly.

### Confusion Matrix

Shows the relationship between the actual class and predicted class for each of the 10 Fashion-MNIST categories.

### Classification Report

Provides the following performance measures:

* Precision
* Recall
* F1-score
* Support

## Misclassified Images

The assignment also identifies images where the model's prediction is different from the actual label.

A sample of 25 misclassified images is displayed along with:

* True class
* Predicted class

This helps in understanding which types of clothing images are difficult for the neural network to classify.

## Technologies Used

* Python
* TensorFlow
* Keras
* Scikit-learn
* NumPy
* Pandas
* Matplotlib
* Seaborn

## Conclusion

This assignment demonstrates the implementation and evaluation of a neural network for Fashion-MNIST image classification.

Different learning rates and numbers of epochs are compared to understand their effect on model performance. The final model is further analyzed using accuracy, training and validation graphs, a confusion matrix, classification report, and visualization of misclassified images.
