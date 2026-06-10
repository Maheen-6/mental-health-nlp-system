# Mental Health Text Classification Using TF-IDF and Logistic Regression

## Project Overview

This project presents a Natural Language Processing (NLP) based Mental Health Text Classification system that predicts a person's mental health status from textual statements.

The model classifies statements into three categories:

* Normal
* Depression
* Suicidal

The project implements a complete machine learning pipeline including data preprocessing, text cleaning, feature extraction using TF-IDF, model training using Logistic Regression, evaluation, prediction, and model persistence.

---

## Dataset

The dataset was obtained from Kaggle and contains approximately 53,000 text records related to mental health.

### Dataset Features

| Column    | Description            |
| --------- | ---------------------- |
| statement | User text statement    |
| status    | Mental health category |

### Classes Used

The following mental health categories were selected for classification:

* Normal
* Depression
* Suicidal

Other categories present in the original dataset were excluded from the study.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* NLTK
* Scikit-Learn
* Joblib

---

## Project Workflow

Dataset
↓
Data Cleaning
↓
Text Preprocessing
↓
Stopword Removal
↓
Label Encoding
↓
Train-Test Split
↓
TF-IDF Vectorization
↓
Logistic Regression Training
↓
Model Evaluation
↓
Prediction
↓
Model Saving

---

## Data Preprocessing

The following preprocessing steps were applied:

* Filtering selected classes
* Removing missing values
* Removing duplicate records
* Resetting dataset indices
* Converting text to lowercase
* Removing punctuation
* Removing stopwords
* Preserving important negation words such as:

  * not
  * no
  * never
  * don't
  * can't
  * won't

Preserving negation words helps maintain the original sentiment and meaning of statements.

---

## Feature Extraction

TF-IDF (Term Frequency-Inverse Document Frequency) was used to convert textual data into numerical feature vectors.

### Configuration

* Maximum Features: 20,000
* N-Grams: Unigrams and Bigrams (1,2)

This allows the model to capture both individual words and meaningful word combinations.

---

## Machine Learning Model

### Logistic Regression

The classification model used in this project is Logistic Regression.

### Model Configuration

* Maximum Iterations: 2000
* Balanced Class Weights

### Reasons for Selection

* Effective for text classification tasks
* Fast training and prediction
* Supports multiclass classification
* Performs well with TF-IDF features
* Computationally efficient for large datasets

---

## Model Evaluation

The trained model was evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

Class distribution and confusion matrix visualizations were generated to analyze model performance.

---

## Prediction System

The project includes a custom prediction function that:

1. Cleans and preprocesses input text.
2. Converts text into TF-IDF vectors.
3. Uses the trained Logistic Regression model for prediction.
4. Returns the predicted mental health category.

Example categories predicted:

* Normal
* Depression
* Suicidal

---

## Model Persistence

The following trained components are saved for future use:

* model.pkl (Logistic Regression Model)
* tfidf.pkl (TF-IDF Vectorizer)
* label_encoder.pkl (Label Encoder)

These files allow predictions without retraining the model.

---

## Project Structure

Mental-Health-Text-Classification/

├── Mental_Health_Classification.ipynb
├── dataset.xlsx
├── model.pkl
├── tfidf.pkl
├── label_encoder.pkl
├── requirements.txt
└── README.md

---

## Future Improvements

Potential future enhancements include:

* Lemmatization and stemming
* Hyperparameter tuning
* Cross-validation
* Deep Learning models (LSTM, GRU)
* Transformer-based models (BERT, RoBERTa)
---

## Conclusion

This project demonstrates an end-to-end NLP pipeline for mental health text classification using TF-IDF feature extraction and Logistic Regression. The system preprocesses text data, extracts meaningful features, trains a multiclass classifier, evaluates model performance, predicts unseen statements, and saves trained artifacts for future use.

The project provides a simple, scalable, and effective approach for automated mental health text classification.
