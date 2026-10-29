# 🛡️ AI Phishing Email Detector

A beginner-friendly cybersecurity and machine learning project that detects potential phishing emails using Natural Language Processing (NLP) and Logistic Regression.

## 📌 Project Overview

Phishing emails often attempt to steal passwords, financial information, and one-time passwords (OTPs). This project analyzes email text and predicts whether it resembles a phishing email or a safe email.

## ✨ Features

- Email text classification
- Interactive email analyzer in Google Colab
- Batch analysis of multiple emails
- Estimated phishing probability score
- Safety recommendations
- Model evaluation metrics and confusion matrix

## 🧰 Technologies Used

- Python
- Pandas
- Scikit-learn
- TF-IDF Vectorization
- Logistic Regression
- Matplotlib
- Google Colab

## ⚙️ How It Works

1. Load and inspect the email dataset.
2. Clean missing values, duplicate messages, and placeholder records.
3. Split the data into training and testing sets.
4. Transform email text using TF-IDF.
5. Train a Logistic Regression classifier.
6. Predict email categories and estimate phishing scores.
7. Evaluate the model using accuracy, precision, recall, and F1-score.

## 📊 Dataset and Results

- Cleaned records: 17,521
- Training samples: 14,016
- Testing samples: 3,505
- Model: TF-IDF + Logistic Regression
- Test-set accuracy: 98.32%
- Phishing recall: approximately 97.17%

These metrics describe performance on the selected test dataset and do not guarantee equivalent performance on real-world emails.

## 📁 Project Files

- `AI_Phishing_Email_Detector.ipynb` — development and analysis notebook
- `phishing_detector_model.joblib` — trained model
- `batch_analysis_results.csv` — sample batch predictions
- `model_evaluation_metrics.csv` — evaluation metrics
- `project_summary.json` — project summary
- `README.md` — project documentation

## 🚀 Run the Project

1. Open the notebook on GitHub.
2. Select **Open in Colab** if the option is available, or download the notebook and upload it to Google Colab.
3. Follow the notebook cells in order.
4. Run the training cells before using functions that depend on the trained model.

## ⚠️ Limitations

- Predictions can be incorrect.
- A high phishing score is not proof of malicious intent.
- A low score does not guarantee an email is safe.
- The prototype analyzes text only; it does not verify sender authentication or inspect link destinations.
- Do not submit confidential emails to a public demo.

## 🔮 Future Improvements

- Build a web dashboard.
- Test against a separate, newer dataset.
- Analyze suspicious URLs and sender information.
- Improve detection of previously unseen phishing attacks.

## 📚 Disclaimer

This project is for educational and portfolio purposes. It should not be used as the sole basis for deciding whether an email is safe.

## 👨‍💻 Author

**Ankit Tripathi**

Aspiring technology professional interested in cybersecurity, machine learning, and practical problem-solving.
