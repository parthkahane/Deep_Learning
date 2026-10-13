# Assignment 5: Comparative Analysis of RNN, LSTM, and GRU

## Overview

This project implements and compares three recurrent neural network architectures: Simple RNN, Long Short-Term Memory (LSTM), and Gated Recurrent Unit (GRU). The models are trained on the Reuters Newswire Dataset to classify news articles into 46 different topics.

The experiment compares their classification performance, computational requirements, and ability to learn sequential text patterns.

## Problem Statement

Implement and compare RNN, LSTM, and GRU models for sequence classification, and analyze their performance using appropriate evaluation metrics.

## Objectives

- Understand recurrent neural networks and their applications.
- Implement RNN, LSTM, and GRU architectures.
- Perform sequence preprocessing and padding.
- Classify news articles into different categories.
- Compare models using evaluation metrics and training time.
- Visualize model performance and confusion matrices.

## Dataset

**Dataset Name:** Reuters Newswire Dataset

The Reuters dataset contains news articles belonging to 46 different categories, including topics related to economics, trade, politics, business, commodities, and finance.

Each article is represented as a sequence of integer word IDs.

### Dataset Configuration

- Maximum vocabulary size: 10,000 words
- Maximum sequence length: 200 tokens
- Embedding dimension: 128
- Number of output classes: 46
- Training epochs: 5
- Batch size: 128

## Technologies Used

- Python
- TensorFlow and Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Model Architectures

### 1. Simple RNN

A Simple Recurrent Neural Network maintains a hidden state that carries information from previous time steps. It is suitable for sequential data but can struggle with long-term dependencies due to the vanishing-gradient problem.

### 2. LSTM

Long Short-Term Memory networks use memory cells and gates to preserve relevant information across time steps. They are designed to learn longer-term dependencies in sequential data.

### 3. GRU

Gated Recurrent Units use update and reset gates to control information flow. They provide a gated recurrent architecture that often requires fewer parameters than an LSTM with a comparable configuration.

## Methodology

1. Load the Reuters Newswire Dataset.
2. Set random seeds for reproducibility.
3. Limit the vocabulary to 10,000 words.
4. Analyze sequence lengths and class distribution.
5. Pad sequences to a maximum length of 200.
6. Create an embedding layer.
7. Build separate RNN, LSTM, and GRU models.
8. Add dropout and dense classification layers.
9. Train each model for up to five epochs with early stopping.
10. Predict news categories on the test dataset.
11. Calculate accuracy, precision, recall, and F1-score.
12. Compare training time and parameter counts.
13. Generate performance graphs and confusion matrices.

## Model Configuration

Each model uses the following common components:

- Embedding layer with 128 dimensions
- Recurrent layer with 128 units
- Dropout layer with a rate of 0.3
- Dense layer with 64 neurons and ReLU activation
- Dropout layer with a rate of 0.2
- Softmax output layer with 46 classes

The models use the Adam optimizer with a learning rate of 0.001 and sparse categorical cross-entropy loss.

## Evaluation Metrics

- **Accuracy:** Percentage of correctly classified articles.
- **Precision:** Correct positive predictions relative to all positive predictions.
- **Recall:** Correctly identified samples relative to all actual samples.
- **F1-score:** Harmonic mean of precision and recall.
- **Confusion Matrix:** Displays classification results for individual classes.
- **Training Time:** Measures the time taken to train each model.

## Results

The final model comparison produced the following results:

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| RNN | 44.52% | 41.26% | 44.52% | 39.93% |
| LSTM | 57.26% | 51.78% | 57.26% | 53.23% |
| GRU | 56.77% | 52.15% | 56.77% | 52.80% |

### Training Performance

| Model | Training Time | Parameters |
|---|---:|---:|
| RNN | 128.94 seconds | 1,324,142 |
| LSTM | 348.47 seconds | 1,422,830 |
| GRU | 243.84 seconds | 1,390,318 |

*Training times are from the recorded execution and may vary across hardware and environments.*

### Key Findings

- **LSTM** achieved the highest accuracy and F1-score in the recorded final comparison.
- **GRU** achieved the highest precision and required less training time than LSTM in this execution.
- **RNN** had the shortest training time but the lowest classification accuracy.
- The results illustrate the trade-off between classification performance and computational cost.

## Visualizations

The implementation generates:

- Sequence length distribution
- Reuters class distribution
- Training accuracy comparison
- Validation accuracy comparison
- Training and validation loss graphs
- Confusion matrices for all three models
- Final model comparison charts

## How to Run

1. Open Google Colab or a compatible Python environment.
2. Install the required libraries:

   ```bash
   pip install tensorflow numpy pandas matplotlib seaborn scikit-learn
   ```

3. Copy the assignment implementation into a notebook or Python file.
4. Execute the code to load the Reuters dataset, train all three models, and compare their performance.

The Reuters dataset is loaded through TensorFlow Keras.

## Conclusion

This experiment compares three recurrent neural network architectures for multi-class news classification. LSTM achieved the best overall accuracy in the recorded final comparison, while GRU provided competitive performance with a shorter training time. The experiment highlights the importance of evaluating both predictive performance and computational efficiency when selecting a sequence-classification model.

## Author

**Parth Kahane**  
Department: CSE (AI)  
Vishwakarma Institute of Technology, Pune  
Subject: Deep Learning  
Practical No.: 5
