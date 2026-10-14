# Machine Learning Approach — SMS Spam Classifier

## 1. Introduction

SMS spam classification is a supervised machine learning task in which a model learns from labeled text messages to predict whether a new message is spam or legitimate (ham).

This project uses text vectorization and the Multinomial Naive Bayes algorithm.

## 2. Machine Learning Pipeline

The proposed pipeline consists of the following stages:

1. **Data loading:** Load labeled SMS messages from the UCI SMS Spam Collection dataset.
2. **Data validation:** Check labels, empty messages, duplicates, and dataset format.
3. **Train-test split:** Divide the data into training and testing sets while preserving the approximate class distribution.
4. **Text vectorization:** Transform text into numerical features using CountVectorizer or TfidfVectorizer.
5. **Model training:** Train a Multinomial Naive Bayes classifier on the training data.
6. **Model evaluation:** Measure performance on the held-out test set.
7. **Prediction:** Use the fitted vectorizer and classifier to analyze new SMS messages.

The vectorizer must be fitted on training data only to prevent data leakage.

## 3. Text Vectorization

Machine learning algorithms generally require numerical input rather than raw text.

A text vectorizer represents each message using numerical features derived from its words or tokens.

### CountVectorizer

CountVectorizer represents text using token occurrence counts.

For example:

- Message A: "Win a prize"
- Message B: "Win a reward"

The vectorizer builds a vocabulary and represents each message using the counts of vocabulary terms.

### TfidfVectorizer

TfidfVectorizer weights terms based on their frequency in a message and their distribution across the document collection.

The implementation will use the vectorizer selected and tested in the actual application.

## 4. Multinomial Naive Bayes

Multinomial Naive Bayes is a probabilistic classification algorithm commonly used for text classification.

It applies Bayes' theorem:

P(C | X) = P(X | C) × P(C) / P(X)

Where:

- **P(C | X):** Probability of class C given message features X.
- **P(X | C):** Likelihood of the features given class C.
- **P(C):** Prior probability of class C.
- **P(X):** Overall probability of the observed features.

The classifier estimates which class—SPAM or HAM—is more likely based on patterns learned during training.

The algorithm makes simplifying conditional-independence assumptions about features. Actual predictions may be incorrect.

## 5. Model Evaluation

The trained classifier will be evaluated using a held-out test set.

### Accuracy

The proportion of all predictions that are correct.

Accuracy = (True Positives + True Negatives) / Total Predictions

### Precision

The proportion of messages predicted as spam that are actually spam.

Precision = TP / (TP + FP)

### Recall

The proportion of actual spam messages correctly identified.

Recall = TP / (TP + FN)

### F1-Score

The harmonic mean of precision and recall.

F1 = 2 × (Precision × Recall) / (Precision + Recall)

### Confusion Matrix

A confusion matrix helps identify:
- True positives: Spam correctly identified as spam.
- True negatives: Ham correctly identified as ham.
- False positives: Ham incorrectly classified as spam.
- False negatives: Spam incorrectly classified as ham.

For this project, both false positives and false negatives matter because legitimate messages can be incorrectly flagged and spam messages can be missed.

## 6. Reproducibility and Data Leakage Prevention

- Use a fixed random state for reproducible train-test splitting.
- Use stratification where appropriate.
- Fit the vectorizer only on training messages.
- Evaluate using data excluded from model fitting.
- Report actual measured results rather than assumed accuracy.
- Keep preprocessing and model inference consistent.

## 7. Limitations

- The model learns patterns from the available dataset.
- New vocabulary, obfuscated words, and evolving spam tactics can reduce performance.
- Predicted probabilities are model estimates and may not represent calibrated real-world certainty.
- Test-set performance may differ from performance on messages encountered in real use.

## 8. Implementation Status

This document describes the intended machine learning approach. The selected vectorizer, trained model, and measured evaluation results should be documented after implementation and testing.
