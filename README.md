# 🎬 Sentiment Analysis on IMDb Reviews

This project performs **sentiment analysis** on movie reviews using two popular Natural Language Processing (NLP) techniques: **VADER** and **TextBlob**. It includes data preprocessing, visualization, model evaluation, and custom text testing.

---

## 📌 Project Overview

The goal of this project is to:

* Analyze movie reviews from a labeled dataset
* Compare sentiment predictions using different NLP tools
* Visualize sentiment distribution
* Evaluate model performance
* Allow users to test custom input text

---

## 📂 Dataset

* Dataset used: `imdb_labelled.csv`
* Contains:

  * `review` → Movie review text
  * `sentiment` / `label` → Actual sentiment (positive/negative)

---

## ⚙️ Technologies Used

* Python 🐍
* Pandas & NumPy (Data handling)
* NLTK (VADER Sentiment Analysis)
* TextBlob (Polarity-based sentiment)
* Matplotlib (Visualization)
* Scikit-learn (Evaluation metrics)

---

## 🔄 Workflow

### 1. Data Loading & Exploration

* Load dataset using Pandas
* Check shape, missing values, and label distribution

### 2. Text Preprocessing

* Convert text to lowercase
* Remove HTML tags
* Remove punctuation and special characters
* Strip extra spaces

### 3. Sentiment Analysis

#### 🔹 VADER

* Uses compound score:

  * ≥ 0.05 → Positive
  * ≤ -0.05 → Negative
  * Otherwise → Neutral

#### 🔹 TextBlob

* Uses polarity:

  * > 0 → Positive
  * < 0 → Negative
  * = 0 → Neutral

---

-

## 📈 Model Evaluation

* Accuracy calculated using `accuracy_score`
* Classification report for detailed metrics

Example:

```
VADER Accuracy:    XX.XX%
TextBlob Accuracy: XX.XX%
```

---

## 🧪 Custom Text Analysis

You can test your own text using:

```python
analyze_my_text("Your sentence here")
```

Output includes:

* Predicted sentiment
* VADER compound score
* TextBlob polarity score

---

## 📌 Key Insights

* VADER performs well on short, informal text
* TextBlob provides simple polarity-based classification
* Both models may struggle with sarcasm and context
* Visualization helps in comparing model predictions effectively
