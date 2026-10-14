# SMS Spam Classifier

A machine learning project that classifies SMS messages as **SPAM** or **HAM (legitimate messages)** using Natural Language Processing (NLP) and the Multinomial Naive Bayes algorithm.

## Overview

Unwanted and fraudulent text messages can expose users to suspicious links, misleading offers, and potential scams. This project explores how machine learning can help distinguish spam messages from legitimate messages based on patterns learned from labeled SMS data.

## Objectives

- Build a text classification model using Python and scikit-learn.
- Process SMS messages into numerical features.
- Train a Multinomial Naive Bayes classifier.
- Evaluate model performance using standard classification metrics.
- Develop a user-friendly web interface for message analysis.

## Planned Features

- SMS message input and classification.
- SPAM and HAM prediction results.
- Model confidence or probability display, if supported.
- Model evaluation metrics.
- Responsive web interface.
- Input validation and clear error handling.

*Features will be marked as completed after implementation and testing.*

## Technology Stack

- **Language:** Python
- **Machine Learning:** scikit-learn
- **Data Processing:** pandas
- **Text Vectorization:** CountVectorizer or TfidfVectorizer
- **Classification:** Multinomial Naive Bayes
- **Backend:** Flask
- **Frontend:** HTML, CSS and JavaScript

## Machine Learning Workflow

1. Load and inspect the labeled SMS dataset.
2. Clean and validate the data.
3. Split the dataset into training and testing sets.
4. Convert text messages into numerical features.
5. Train the Naive Bayes classifier.
6. Evaluate predictions using accuracy, precision, recall, F1-score and a confusion matrix.
7. Integrate the trained model with the web application.

## Dataset

The project uses the [UCI SMS Spam Collection](https://archive.ics.uci.edu/dataset/228/sms+spam+collection).

The dataset contains labeled SMS messages classified as `spam` or `ham`. Refer to the dataset's terms and attribution requirements before redistributing the raw data.

## Project Status

**Status:** In development.

The model, web interface and evaluation results will be documented as they are implemented and tested.

## Limitations

- Predictions depend on the quality and coverage of the training dataset.
- New or unusual spam messages may be misclassified.
- A HAM prediction does not guarantee that a message is genuine or safe.
- Model evaluation results do not guarantee real-world performance.

## Future Improvements

- Compare different text vectorization techniques.
- Evaluate additional classification algorithms.
- Improve performance on previously unseen messages.
- Add more detailed evaluation visualizations.
- Explore multilingual SMS classification.

## Responsible Use

This project is intended for educational purposes. Do not rely solely on its predictions to determine whether a message is safe. Avoid clicking suspicious links or sharing OTPs, passwords, or financial information with untrusted sources.

## Author

Developed as a machine learning and web development portfolio project by a second-year Information Technology engineering student.
