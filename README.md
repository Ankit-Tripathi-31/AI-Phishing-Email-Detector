# AI Phishing Email Detector

## Overview
A beginner-friendly cybersecurity project that uses Machine
Learning and Natural Language Processing (NLP) to classify
email text as Safe Email or Phishing Email.

## Problem Statement
Phishing emails can trick people into revealing passwords,
financial information, or one-time passwords (OTPs).
This project explores automated detection of suspicious
email text.

## Technologies Used
- Python
- Pandas
- Scikit-learn
- TF-IDF Vectorization
- Logistic Regression
- Matplotlib
- Google Colab

## How It Works
1. Load and clean the email dataset.
2. Remove missing, duplicate, and placeholder email text.
3. Split data into training and testing sets.
4. Convert email text into numerical features using TF-IDF.
5. Train a Logistic Regression classifier.
6. Predict email categories and estimate phishing scores.
7. Evaluate performance using classification metrics.

## Dataset
The cleaned dataset contains 17,521 email records:
- Safe Email: 10,978
- Phishing Email: 6,543

The data was split into training and testing sets using
an 80/20 stratified split.

## Model
TF-IDF + Logistic Regression

## Evaluation
The initial test-set accuracy was 98.32%.
Phishing recall was approximately 97.17%.

These are dataset-specific results and do not guarantee
the same performance on new, real-world emails.

## Features
- Single-email analysis
- Interactive email input in Google Colab
- Batch email analysis
- Estimated phishing score
- Safety recommendations
- Model evaluation chart

## Limitations
- The model can produce false positives and false negatives.
- A high or low score does not guarantee that an email is safe.
- The current prototype analyzes email text, not full email
  headers, sender authentication, or destination URL behavior.
- Avoid pasting real confidential emails into the demo.

## Future Improvements
- Build a web dashboard.
- Test on an independent, newer dataset.
- Analyze URLs and sender information safely.
- Improve detection of previously unseen phishing patterns.

## Disclaimer
This project is an educational prototype and should not be
used as the sole method of deciding whether an email is safe.
