# Greenwashing Detection Using BERT

A BERT-based NLP classification project for detecting greenwashing in corporate sustainability reports.

## Overview

This project uses a fine-tuned BERT transformer model to classify text from corporate sustainability reports into two categories: greenwashing and non-greenwashing.

The project involves data preprocessing, label creation, stratified dataset splitting, BERT tokenization, model fine-tuning, evaluation, and visualization of validation performance.

## Project Workflow

1. Load the preprocessed sustainability-report dataset.
2. Create a binary `greenwashing_label` using the median of the `total_score` column.
3. Split the dataset into:
   - 80% Training
   - 10% Validation
   - 10% Testing
4. Tokenize the text using the BERT tokenizer.
5. Fine-tune `bert-base-uncased` for binary text classification.
6. Train the model using PyTorch and Hugging Face Transformers.
7. Select the best model based on validation accuracy.
8. Apply early stopping to reduce unnecessary training.
9. Evaluate the final model on the test dataset.
10. Generate a classification report and validation-accuracy visualization.

## Model Configuration

- **Base Model:** `bert-base-uncased`
- **Task:** Binary Text Classification
- **Maximum Sequence Length:** 256
- **Training Batch Size:** 16
- **Learning Rate:** 2e-5
- **Maximum Epochs:** 10
- **Early Stopping Patience:** 2
- **Evaluation Metric:** Accuracy

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- BERT
- Pandas
- Scikit-learn
- Matplotlib

## Dataset

The project uses a preprocessed dataset containing:

- `preprocessed_content` — processed sustainability-report text
- `total_score` — score used to create the binary greenwashing label

The dataset is **not included in this repository**.

To run the notebook, provide the required dataset and update the dataset path if necessary.

## Evaluation

The model is evaluated using:

- Validation Accuracy
- Test Accuracy
- Classification Report
- Validation Accuracy Across Epochs

Actual performance values should be taken from the notebook execution results.

## Repository Structure

```text
greenwashing_detection_bert/
│
├── greenwashing_detection_bert.ipynb
├── README.md
└── requirements.txt
