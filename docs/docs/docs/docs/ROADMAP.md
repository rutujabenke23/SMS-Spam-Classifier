# Project Roadmap — SMS Spam Classifier

This roadmap outlines the planned development stages for the SMS Spam Classifier project.

## Phase 1: Dataset and Preparation

- [ ] Obtain the UCI SMS Spam Collection dataset.
- [ ] Validate the dataset format and labels.
- [ ] Inspect class distribution and duplicate messages.
- [ ] Prepare reproducible training and testing datasets.

## Phase 2: Machine Learning Model

- [ ] Implement text vectorization.
- [ ] Train a Multinomial Naive Bayes classifier.
- [ ] Evaluate the model using accuracy, precision, recall, and F1-score.
- [ ] Generate a confusion matrix.
- [ ] Save and reload the trained model successfully.

## Phase 3: Web Application

- [ ] Develop a responsive frontend.
- [ ] Implement a Flask backend.
- [ ] Connect the frontend to the prediction API.
- [ ] Display model predictions and supported probability estimates.
- [ ] Add input validation and error handling.

## Phase 4: Testing and Reliability

- [ ] Test legitimate-looking and spam-like sample messages.
- [ ] Verify behavior for empty and invalid inputs.
- [ ] Test API health and metrics endpoints.
- [ ] Verify that the interface works on desktop and mobile.
- [ ] Document known limitations.

## Phase 5: GitHub Portfolio

- [ ] Add screenshots of the working application.
- [ ] Document installation and execution instructions.
- [ ] Record actual model evaluation results.
- [ ] Review repository structure and remove unnecessary files.
- [ ] Update the README to reflect completed features.

## Future Improvements

- Compare multiple text vectorization methods.
- Experiment with alternative classification algorithms.
- Investigate false positives and false negatives.
- Evaluate performance on additional, appropriately sourced messages.
- Improve accessibility and user experience.

## Status

The checklist reflects intended development tasks. Mark an item complete only after implementing and verifying it.
