# AI Phishing Email Detector — Project Report

## 1. Project Overview

The AI Phishing Email Detector is an educational cybersecurity project that uses Natural Language Processing (NLP) and machine learning to classify email text as either Safe Email or Phishing Email. It also displays an estimated phishing probability and provides basic safety guidance.

## 2. Problem Statement

Phishing messages may impersonate trusted organizations or people to persuade recipients to reveal passwords, financial information, or one-time passwords (OTPs). This project explores how machine learning can help identify suspicious patterns in email text.

## 3. Objectives

- Prepare and inspect an email dataset.
- Train a text-classification model.
- Predict whether email text resembles phishing.
- Evaluate the model using a held-out test set.
- Provide single-email and batch-analysis demonstrations.

## 4. Tools and Technologies

- Python
- Google Colab
- Pandas
- Scikit-learn
- TF-IDF text vectorization
- Logistic Regression
- Matplotlib
- Joblib
- IPyWidgets

## 5. Dataset Preparation

The project dataset was cleaned by removing records with missing or blank email text, removing duplicate email texts, and excluding placeholder values. The final dataset contained 17,521 records:

- Safe Email: 10,978
- Phishing Email: 6,543

The dataset was divided using a stratified 80/20 train-test split:

- Training samples: 14,016
- Testing samples: 3,505

## 6. Model Methodology

The model uses a Scikit-learn pipeline with two main stages:

1. **TF-IDF Vectorizer:** Converts email text into numerical features and considers single words and two-word phrases.
2. **Logistic Regression:** Learns patterns from the training data and predicts the email category.

The fitted model was saved using Joblib for later reuse.

## 7. Evaluation Results

The held-out test-set evaluation produced the following results:

| Metric | Result |
|---|---:|
| Accuracy | 98.32% |
| Phishing precision | Approximately 98% |
| Phishing recall | Approximately 97.17% |
| Phishing F1-score | Approximately 97.6% |

The confusion matrix, with rows representing actual labels and columns representing predicted labels, was:

| Actual / Predicted | Safe Email | Phishing Email |
|---|---:|---:|
| Safe Email | 2,174 | 22 |
| Phishing Email | 37 | 1,272 |

The model correctly classified 2,174 safe-labeled emails and 1,272 phishing-labeled emails in the test set. It incorrectly flagged 22 safe-labeled emails and missed 37 phishing-labeled emails.

These are results from the selected dataset and split. They do not establish how the model will perform on new, real-world emails.

## 8. Application Features

- Interactive email text input in Google Colab
- Single-email prediction
- Estimated phishing probability
- Basic safety advice
- Batch analysis of multiple email texts
- Exportable evaluation metrics and prediction results

## 9. Limitations and Responsible Use

- The classifier can produce false positives and false negatives.
- Its probability score is not a guarantee that a message is malicious or safe.
- The current model analyzes email text only; it does not authenticate senders, inspect full email headers, or safely analyze destination URLs.
- Dataset-specific accuracy may be affected by duplicates, source characteristics, and differences between training data and real-world messages.
- Do not paste confidential emails or personal information into a public demo.

This prototype is intended for learning and demonstration. It should not be used as the sole basis for cybersecurity decisions.

## 10. Future Improvements

- Evaluate on a newer, independent dataset.
- Test generalization across different email sources and writing styles.
- Add safe URL-feature analysis and sender-authentication checks.
- Build a standalone web interface.
- Monitor false positives and false negatives during further testing.

## 11. Conclusion

This project demonstrates an end-to-end beginner machine-learning workflow for email text classification, including data cleaning, TF-IDF feature extraction, Logistic Regression training, evaluation, interactive prediction, and artifact saving. It provides a foundation for further experimentation in phishing detection.

## Author

Ankit Tripathi

Educational cybersecurity and machine-learning portfolio project.
