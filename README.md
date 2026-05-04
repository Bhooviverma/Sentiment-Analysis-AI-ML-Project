# 🎬 IMDb Movie Review Sentiment Analyzer

A Python-based NLP project that performs sentiment analysis on IMDb movie reviews using two rule-based approaches — **VADER** and **TextBlob** — and compares their performance against labeled ground truth.

---

## 📌 Overview

This project analyzes movie reviews from the IMDb dataset to classify sentiments as **positive**, **negative**, or **neutral**. It uses two lexicon-based NLP tools and evaluates their accuracy side by side with visualizations.

---

## 🧠 Techniques Used

| Tool | Approach | Strength |
|------|----------|----------|
| **VADER** | Rule-based + lexicon | Great for social/informal text |
| **TextBlob** | Pattern-based NLP | Simple polarity scoring |

---

## 📁 Project Structure

```
sentiment-analysis/
│
├── imdb_labelled.csv         # Dataset: reviews with sentiment labels
├── sentiment_analysis.py     # Main script
├── sentiment_chart.png       # Bar chart: actual vs predicted
├── pie_chart.png             # Pie charts: VADER & TextBlob breakdown
└── README.md
```

---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-username/imdb-sentiment-analysis.git
cd imdb-sentiment-analysis
```

### 2. Install dependencies
```bash
pip install pandas numpy nltk matplotlib textblob scikit-learn
```

### 3. Download NLTK data
```python
import nltk
nltk.download('vader_lexicon')
nltk.download('stopwords')
nltk.download('punkt')
```

---

## 🚀 Usage

Run the main script:
```bash
python sentiment_analysis.py
```

This will:
1. Load and explore the IMDb dataset
2. Clean and preprocess review text
3. Predict sentiments using VADER and TextBlob
4. Generate bar and pie chart visualizations
5. Print accuracy scores and classification reports
6. Analyze a custom sample review

### Analyze your own text

You can call `analyze_my_text()` directly in the script:
```python
analyze_my_text("This movie was absolutely fantastic!")
```

**Sample Output:**
```
Your Text: This movie was absolutely fantastic!

VADER Result:    POSITIVE
  Compound Score: 0.6588

TextBlob Result: POSITIVE
  Polarity Score: 1.000
```

---

## 📊 Results

Both models are evaluated on binary classification (positive vs. negative):

| Model | Accuracy |
|-------|----------|
| VADER | ~69% |
| TextBlob | ~65% |

> Results may vary slightly depending on the dataset version used.

### Visualizations

- **Bar Chart** — Compares actual vs. predicted sentiment distributions
- **Pie Chart** — Shows percentage breakdown for each model's predictions

---

## 📦 Dataset

Uses the [IMDb Labelled Sentences dataset](https://archive.ics.uci.edu/ml/datasets/Sentiment+Labelled+Sentences) from the UCI ML Repository.

The CSV contains:
- `review` — raw movie review text
- `sentiment` — ground truth label (`positive` / `negative`)
- `label` — binary encoding (`1` = positive, `0` = negative)

---

## 🛠️ Dependencies

- `pandas` — data handling
- `numpy` — numerical operations
- `nltk` — VADER sentiment analyzer
- `textblob` — TextBlob sentiment analyzer
- `matplotlib` — plotting charts
- `scikit-learn` — accuracy scoring & classification report

---

## 📌 Future Improvements

- [ ] Add ML-based models (Logistic Regression, Naive Bayes, BERT)
- [ ] Build an interactive web UI with Streamlit
- [ ] Expand to multi-class sentiment (very positive, mixed, etc.)
- [ ] Add word cloud visualizations for positive/negative reviews

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

---
