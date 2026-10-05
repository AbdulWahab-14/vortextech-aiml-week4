# Vortex Tech Week 4 — Build a Sentiment Analysis Model

This repository contains the Week 4 Capstone submission for the Vortex Tech AI/ML Internship track.

## Project Overview
This project builds a Natural Language Processing (NLP) sentiment classification model that categorizes text reviews as positive or negative using TF-IDF feature extraction and Logistic Regression.

## Dataset & Preprocessing
- **Dataset:** IMDB Movie Reviews (50,000 reviews)
- **Cleaning:** Converted text to lowercase and stripped punctuation/special characters using regular expressions (`re`).
- **Feature Extraction:** Used `TfidfVectorizer` (top 5,000 features) to convert text into numerical vectors.

## Model & Performance
- **Model:** Logistic Regression (`scikit-learn`)
- **Train/Test Split:** 80% Training / 20% Testing (`random_state=42`)
- **Accuracy:** ~88.5%
- **F1-Score:** ~0.88

## Custom Sentence Testing
Tested the model on three custom sentences:
1. *"This was the best experience ever, absolutely loved the story!"* -> **Positive**
2. *"This was a complete waste of time and terrible acting."* -> **Negative**
3. *"The plot was okay, but the movie felt a bit too long."* -> **Negative**

## Limitations
- **Sarcasm & Context:** The model relies on TF-IDF word frequency and can struggle with sarcastic statements or nuanced context where positive words are used negatively.

## How to Run
Open `Week4_Sentiment_Analysis.ipynb` in Google Colab or Jupyter Notebook and execute all cells sequentially.
