# Assignment 8: BERT-Based Sentiment Analysis

## Overview

This project implements a pre-trained BERT model for sentiment analysis of movie reviews. The model uses the Rotten Tomatoes movie-review dataset to classify text into positive and negative sentiment categories.

Instead of training a language model from scratch, the experiment fine-tunes the pre-trained `bert-base-uncased` model for binary text classification.

## Problem Statement

Implement a pre-trained BERT model for sentiment analysis or text classification on a sample dataset.

## Objectives

- Understand the BERT Transformer architecture.
- Apply a pre-trained language model to sentiment analysis.
- Perform text tokenization and preprocessing.
- Fine-tune BERT using labeled movie reviews.
- Evaluate the model using classification metrics.
- Test the trained model on new reviews.
- Save and reload the fine-tuned model.

## Dataset

**Dataset Name:** Rotten Tomatoes Movie Reviews

The dataset contains short movie-review sentences labeled according to their sentiment.

| Label | Sentiment |
|---|---|
| 0 | Negative |
| 1 | Positive |

### Dataset Configuration

The experiment uses a subset of the original dataset:

- Training samples: 2,000
- Testing samples: 500
- Model: `bert-base-uncased`
- Maximum tokenized sequence length: 256

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- Scikit-learn
- NumPy
- Pandas
- Matplotlib
- Seaborn

## What Is BERT?

BERT stands for **Bidirectional Encoder Representations from Transformers**.

It is a Transformer-based language model that learns contextual relationships between words by processing text bidirectionally.

Important characteristics include:

- Transformer-based architecture
- Bidirectional contextual understanding
- Pre-training on large text corpora
- Fine-tuning for downstream NLP tasks
- Case-insensitive processing with `bert-base-uncased`

## Methodology

1. Install the required Python libraries.
2. Load the Rotten Tomatoes dataset.
3. Select 2,000 training samples and 500 test samples.
4. Explore sample reviews and sentiment labels.
5. Analyze the distribution of positive and negative reviews.
6. Load the pre-trained BERT tokenizer.
7. Tokenize reviews and truncate sequences to a maximum length of 256.
8. Load BERT for sequence classification with two output classes.
9. Configure the training process using the Hugging Face Trainer API.
10. Fine-tune the model on the training data.
11. Evaluate predictions using accuracy, precision, recall, and F1-score.
12. Generate a confusion matrix and classification report.
13. Test the model on new movie reviews.
14. Save the fine-tuned model and tokenizer.
15. Reload the saved model for subsequent use.

## Model Configuration

- Pre-trained model: `bert-base-uncased`
- Task: Binary sentiment classification
- Number of output classes: 2
- Training epochs: 1
- Training batch size: 8
- Evaluation batch size: 16
- Learning rate: 0.00002
- Weight decay: 0.01
- Maximum sequence length: 256
- Optimizer: AdamW through the Hugging Face training configuration

The classification head is fine-tuned alongside the pre-trained model parameters.

## Evaluation Metrics

- **Accuracy:** Percentage of correctly classified reviews.
- **Precision:** Correct positive predictions relative to all positive predictions.
- **Recall:** Ability to identify actual positive reviews.
- **F1-score:** Harmonic mean of precision and recall.
- **Confusion Matrix:** Displays correct and incorrect predictions for both sentiment classes.

## Results

The recorded evaluation results are:

| Metric | Score |
|---|---:|
| Accuracy | 82.80% |
| Precision | 81.86% |
| Recall | 81.86% |
| F1-score | 81.86% |

These values correspond to the recorded evaluation of the fine-tuned model.

## Testing New Reviews

The implementation supports sentiment predictions for new movie-review text. It displays:

- Input review
- Predicted sentiment
- Prediction confidence

The predicted sentiment is either `POSITIVE` or `NEGATIVE`.

## Saving the Model

The fine-tuned model and tokenizer are saved to:

```text
./bert_rotten_tomatoes_model
```

The saved artifacts can be loaded again for future predictions without repeating the original fine-tuning process.

## How to Run

1. Open Google Colab or a compatible Python environment.
2. Install the required libraries:

   ```bash
   pip install -U transformers datasets accelerate scikit-learn matplotlib seaborn torch
   ```

3. Copy the assignment implementation into a notebook or Python file.
4. Run the code to download the dataset and pre-trained model.
5. Execute the preprocessing, fine-tuning, evaluation, and model-saving steps.

An internet connection is required initially to download the dataset and pre-trained BERT model unless these resources are already available locally.

## Conclusion

This experiment demonstrates how a pre-trained Transformer model can be adapted to movie-review sentiment analysis through fine-tuning. The recorded test evaluation achieved 82.80% accuracy, with an F1-score of 81.86%. The saved model can subsequently be used to classify new reviews as positive or negative.

## Author

**Parth Kahane**  
Department: CSE (AI)  
Vishwakarma Institute of Technology, Pune  
Subject: Deep Learning  
Practical No.: 8
