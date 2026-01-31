# 🎬 IMDB Movie Review Sentiment Analysis

### A Natural Language Processing (NLP) project that classifies movie reviews as Positive or Negative with 89% accuracy.

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Library](https://img.shields.io/badge/Library-Scikit--Learn-orange?style=flat&logo=scikit-learn)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Project Overview
Computers cannot understand human language directly. In this project, I built a machine learning model capable of reading movie reviews and determining the sentiment (Positive vs. Negative).

I used **TF-IDF (Term Frequency-Inverse Document Frequency)** to convert text data into numerical vectors and trained a **Logistic Regression** model to classify the sentiment.

## 📂 Dataset
The dataset is obtained from [Kaggle: IMDB Dataset of 50K Movie Reviews](https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews).

*   **Reviews:** 50,000 text reviews.
*   **Sentiment:** Balanced (25k Positive, 25k Negative).

## ⚙️ Text Preprocessing (NLP)
Raw text data is messy. I implemented a cleaning pipeline to standardize the input:
1.  **HTML Removal:** Stripped out `<br />` tags using Regex.
2.  **Cleaning:** Removed special characters, punctuation, and numbers.
3.  **Normalization:** Converted all text to lowercase.
4.  **Stopwords:** Removed common English words (like "the", "is", "and") that add noise but no sentiment value.

## 🤖 Model Pipeline
I used a Scikit-Learn `Pipeline` to streamline the workflow:

1.  **Vectorization:** `TfidfVectorizer`
    *   Converts words to numbers based on how unique they are to a specific document.
2.  **Classifier:** `Logistic Regression`
    *   A robust linear model perfect for high-dimensional sparse data like text.

**Performance:**
*   **Accuracy:** **89.00%** on the test set.
*   The model successfully distinguishes between "Masterpiece" (Positive) and "Trash" (Negative) with high confidence.

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/JusChillin96/Movie-Sentiment-Analysis.git
