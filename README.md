# Fake Job Posting Detection using Machine Learning

## Overview
With the rapid growth of online job portals, fraudulent job postings have become a serious concern. These fake listings can lead to financial loss, identity theft, and misinformation for job seekers.

This project aims to build a machine learning system that can automatically classify job postings as **real or fraudulent** using both textual and structured data.

---

##  Objective
- Detect fraudulent job postings using machine learning
- Compare multiple models for performance
- Improve accuracy using feature engineering and hyperparameter tuning

---

##  Dataset
The dataset contains job postings along with metadata.

### Features include:
- Job title, description, requirements, benefits
- Company profile
- Employment type, industry, education
- Binary indicators (telecommuting, company logo, questions)
- Target variable: `fraudulent` (0 = real, 1 = fake)

### Characteristics:
- Mixed data (text + categorical + binary)
- Missing values present
- Imbalanced dataset

---

##  Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Matplotlib, Seaborn
- NLTK

---

##  Data Preprocessing
- Removed irrelevant columns (e.g., job_id)
- Handled missing values
- Combined multiple text fields into one column
- Cleaned text:
  - Lowercasing
  - Removing special characters
  - Removing stopwords

---

##  Feature Engineering
- **TF-IDF Vectorization** for text data
- **Binary Encoding** for boolean features
- **One-Hot Encoding** for categorical variables
- Combined all features using sparse matrix stacking

---

## 🤖 Models Used
- Logistic Regression (Baseline model)
- Naive Bayes (Text classification)
- Support Vector Machine (High-dimensional data)
- Random Forest (Non-linear patterns)
- XGBoost (Boosting, best performance)
- AdaBoost (Iterative boosting)

---

##  Hyperparameter Tuning
- Performed using **GridSearchCV**
- Optimized parameters like:
  - Regularization strength (C)
  - Number of estimators
  - Learning rate
- Used **F1-score** for evaluation due to class imbalance

---

##  Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

> Special focus on minimizing false negatives (missing fraudulent jobs)

---

##  Results
- Logistic Regression provided a strong baseline
- Naive Bayes was fast but less effective with structured data
- SVM performed well with high-dimensional data
- Random Forest captured complex patterns
- **XGBoost achieved the best overall performance**
- AdaBoost showed moderate improvement

---

##  Conclusion
- Combining text and structured features improves model performance
- Boosting models outperform traditional models
- XGBoost is the most effective model for this task

---

## Future Scope
- Implement deep learning models (BERT, LSTM)
- Deploy as a web application
- Real-time fraud detection system
- Use advanced NLP techniques for better feature extraction

