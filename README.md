# NLP Assignment 1 – Wikipedia Text Classification

## 📌 Task Description

This project implements a **binary text classification system** to classify English Wikipedia articles as either **geographic** or **non-geographic**. The classifier is built using Natural Language Processing (NLP) techniques and trained on text fetched from Wikipedia using their public REST API.

## 🎯 Objective

Given an English Wikipedia article, determine whether the text is about a *geographic* topic or a *non-geographic* one using NLP techniques and a machine learning classifier.

---

## 🧪 Technologies Used

- **Programming Language**: Python 3.10+
- **NLP Libraries**: 
  - `NLTK` (tokenization, stopword removal, stemming)
  - `BeautifulSoup` (HTML parsing)
- **Machine Learning**: 
  - `Scikit-learn` (CountVectorizer, Naive Bayes, model evaluation)
- **Data Source**: 
  - Wikipedia REST API (`https://en.wikipedia.org/api/rest_v1/page/html/{title}`)

---

## 🔧 Pipeline Architecture

1. **Data Collection**:
   - Articles are fetched from Wikipedia using their public REST API.
   - Example titles include:
     - *Geographic*: `Geography_of_Italy`, `Mount_Everest`, `Amazon_River`
     - *Non-Geographic*: `Python_(programming_language)`, `Photosynthesis`, `Albert_Einstein`

2. **Text Preprocessing**:
   - Convert text to lowercase
   - Remove punctuation
   - Tokenize text
   - Remove English stopwords using `NLTK`
   - Apply stemming using **Porter Stemmer**

3. **Feature Extraction**:
   - Use **Bag of Words** with `CountVectorizer`

4. **Model Training**:
   - Train a **Naive Bayes classifier** (`MultinomialNB`) on the preprocessed data

5. **Evaluation**:
   - Evaluate the model using **Confusion Matrix** and **Classification Report** (precision, recall, F1-score)

