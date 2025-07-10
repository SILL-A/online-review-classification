**Fake Review Detection and Classification using Machine Learning**

This project focuses on building a robust system to detect fake online product reviews using advanced machine learning techniques. Initially launched as "Fake Review Detection and Analysis using ML and DL", the system has evolved into a more refined and explainable ML-based classification model with enhanced feature engineering and improved evaluation strategy.

**📌 Project Evolution**

Version	Title	Summary
Version1: Fake Review Detection and Analysis using ML and DL : Introduced the problem of fake reviews using ML and DL (XGBoost, DNN, etc.). Focused on accuracy and robustness.
Version2:	Online Review Classification using Machine Learning (Final) :	Refined version of version1 with improved feature engineering, optimized models, added explainability, dimensionality reduction, and comparative benchmarking.

**🎯 Objective**

To detect and classify online reviews as genuine or fake, using a combination of:
Textual analysis (via TF-IDF, sentiment)
Behavioral & linguistic metadata (e.g., emoji usage, typo density, readability)
Robust ML algorithms trained and evaluated on a balanced Amazon product reviews dataset

**📦 Dataset**

Source: Amazon Product Review Dataset
Samples: 21,000 (10,500 genuine, 10,500 fake)
Product Categories: 30+ (Wireless, Kitchen, Furniture, etc.)
Attributes:
REVIEW_TEXT, REVIEW_TITLE, PRODUCT_CATEGORY, RATING, VERIFIED_PURCHASE, LABEL (0: real, 1: fake), etc.

**🧠 Machine Learning Models**

| Model         | Accuracy  | Precision | Recall | F1-score |
| ------------- | --------- | --------- | ------ | -------- |
| XGBoost       | **99.3%** | 99.4%     | 99.2%  | 99.3%    |
| KNN           | 98.5%     | 98.2%     | 98.8%  | 98.5%    |
| Decision Tree | 97.4%     | 96.6%     | 98.3%  | 97.4%    |
| Random Forest | 95.8%     | 94.9%     | 97.9%  | 96.4%    |

📌 All models were evaluated using Accuracy, Precision, Recall, F1-score & Confusion Matrix.
📌 XGBoost outperformed all others in both performance and computational efficiency.

**🧪 Features Extracted**

TF-IDF of REVIEW_TEXT (10,000 dimensions)
**Metadata features:
**
Text length, sentence count
Readability (Flesch-Kincaid score)
Stopword & capital letter frequency
Typo density (spell-check errors)
Sentiment polarity score
Sentiment-rating dissonance
Emoji presence

**📉 Dimensionality reduction using PCA:**

Reduced feature space from 10,009 ➝ 50, preserving 99.99% variance

**🔁 Workflow Summary**

Preprocessing: Label encoding, text normalization, vectorization
Feature Engineering: Linguistic, behavioral, and semantic cues
Model Training: 4 classifiers + comparative hyperparameter tuning
Evaluation: Performance metrics, confusion matrix, runtime analysis
Benchmarking: Compared with existing DL/ML research models (e.g. BERT, CNN, Naive Bayes)

**📈 Performance Highlights**

XGBoost: Highest accuracy (99.3%), Fast prediction (1.08s training, low FP/FN)
Decision Tree: Fastest prediction time (~2.5ms/1k reviews)
KNN: Fastest training (8.3ms), but slowest prediction
Random Forest: Slightly higher FP rate

**🔍 Comparative Research References**

Benchmarked against various ML/DL methods:
BERT + Sentiment Fusion (98%)
Fuzzy CNN (95%+)
Naive Bayes, Logistic Regression
LSTM + Word2Vec (92%–97%)

📌 Project’s XGBoost model is simpler, faster, and more accurate than most deep learning approaches, making it deployment-ready and scalable.

