# nm
Here’s a **project description** you can use for your code:

---

# 📌 Project Description: IMDB Movie Review Sentiment Analysis

This project focuses on **Sentiment Analysis** of the IMDB Movie Review dataset using **Natural Language Processing (NLP)** techniques and **Naïve Bayes classifiers**. The goal is to automatically classify movie reviews as **positive** or **negative** based on the text provided by users.

---

## 🔹 Objectives

1. Preprocess raw IMDB reviews by cleaning and normalizing text.
2. Remove unnecessary noise such as HTML tags, special characters, and stopwords.
3. Apply **stemming** to reduce words to their root forms.
4. Convert textual data into numerical features using **Bag-of-Words (CountVectorizer)**.
5. Train and evaluate **Naïve Bayes classifiers** (GaussianNB, MultinomialNB, BernoulliNB).
6. Save trained models and vectorizers for later prediction on new reviews.

---

## 🔹 Dataset

* **Dataset Name**: IMDB Movie Review Dataset
* **Size**: 50,000 labeled reviews
* **Labels**:

  * `1` → Positive sentiment
  * `0` → Negative sentiment

The dataset is balanced with 25,000 positive and 25,000 negative reviews.

---

## 🔹 Preprocessing Steps

1. **HTML tag removal** using regex.
2. **Special character and punctuation removal**.
3. **Lowercasing** all text for uniformity.
4. **Stopword removal** using NLTK stopword list.
5. **Stemming** using Snowball Stemmer.
6. **Feature extraction** with `CountVectorizer(max_features=1000)` to generate a Bag-of-Words model.

---

## 🔹 Model Training

Three **Naïve Bayes classifiers** were trained and tested:

* **GaussianNB** → Accuracy: ~81.1%
* **MultinomialNB** → Accuracy: ~83.1% (Best performer)
* **BernoulliNB** → Accuracy: ~82.4%

---

## 🔹 Model Deployment

* Models were saved using **Pickle** (`gaussian_nb.pkl`, `multinomial_nb.pkl`, `bernoulli_nb.pkl`).
* A **Bag-of-Words vocabulary file** (`bow.pkl` / `vectorizer.pkl`) was saved for consistent feature extraction during inference.
* New movie reviews can be cleaned, vectorized, and passed to the trained models for **real-time sentiment prediction**.

---

## 🔹 Example Prediction

Input:
`"I really enjoyed the movie, it was fantastic!"`

Output:
`Prediction: Positive (1)`

---

## 🔹 Tech Stack

* **Programming Language**: Python
* **Libraries**:

  * `pandas`, `numpy` → Data processing
  * `nltk` → Text preprocessing (stopwords, stemming, tokenization)
  * `scikit-learn` → Feature extraction and machine learning models
  * `pickle` → Model serialization

---

## 🔹 Applications

* Automating review classification for movie platforms.
* Assisting recommendation systems by analyzing sentiment trends.
* Building customer feedback analysis tools.

---

✨ In short, this project demonstrates the end-to-end pipeline of an **NLP-based sentiment analysis system**, from data preprocessing → feature engineering → model training → evaluation → saving models for future deployment.

---

Do you want me to also **write this in a proper "README.md" format** (with headings, bullet points, and code snippets) so you can directly use it in your project repository?
