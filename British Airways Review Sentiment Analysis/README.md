# ✈️ British Airways Review Sentiment Analysis

This project involves scraping customer reviews from [Skytrax](https://www.airlinequality.com/) for British Airways and performing sentiment and rating analysis using Python.

It explores how review sentiment relates to star ratings and whether customers recommend the airline. The project uses basic web scraping, natural language processing (NLP), exploratory data analysis (EDA), and hypothesis testing.

---

## 🧰 Tools & Libraries Used

- `requests`, `BeautifulSoup` – for web scraping  
- `pandas`, `numpy` – for data manipulation  
- `matplotlib`, `seaborn` – for visualizations  
- `nltk` (VADER) – for sentiment analysis  
- `scipy.stats` – for hypothesis testing  

---

## 📊 Project Overview

### 1. **Data Collection**
- Scraped customer reviews from 10 pages of the British Airways section on Skytrax.
- Extracted:
  - Free-text review content
  - Star ratings for categories like *Seat Comfort*, *Food & Beverages*, *Value for Money*, etc.
  - Whether the customer *recommended* the airline.

### 2. **Data Cleaning**
- Removed irrelevant symbols, "Verified/Not Verified" labels, and extra characters using regex.
- Mapped `Recommended` column to binary values (`1 = Yes`, `0 = No`).
- Standardized and lowercased all review texts.

### 3. **Sentiment Analysis**
- Used `nltk`'s `SentimentIntensityAnalyzer` to compute a compound sentiment score for each review.
- Visualized sentiment distribution.
- Compared average sentiment between recommended vs. not recommended reviews.

### 4. **Exploratory Data Analysis**
- Distribution of ratings for each category (e.g., *Seat Comfort*, *Cabin Staff Service*).
- Count of recommended vs. not recommended reviews.
- Correlation matrix to identify relationships between sentiment, ratings, and recommendation status.

### 5. **Hypothesis Testing**
- **H1**: Sentiment differs significantly between recommended and not recommended reviews (T-test).
- **H2**: Sentiment correlates with `Value for Money` rating (Pearson correlation).

---

## 📈 Key Insights

- Recommended reviews had significantly higher sentiment scores.
- Strong positive correlation between sentiment and *Value for Money* rating.
- Categories like *Cabin Staff Service* and *Seat Comfort* showed influence on customer recommendation.
- Most reviews were neutral to slightly positive, with a few highly negative outliers.

---

## 🗂️ Files

- `airline_review_scraper.ipynb`: Full code for scraping, cleaning, EDA, and sentiment analysis.
- `cleaned_reviews_with_ratings_and_info.csv`: Output dataset.
- `images/`: Folder for visualizations (optional).

---

## ▶️ How to Use

1. Clone the repo or open the notebook in Google Colab.
2. Make sure `nltk` and other dependencies are installed.
3. Run the notebook to scrape reviews and perform analysis.
4. You can replace the base URL to analyze reviews for another airline.

> ⚠️ Note: Web scraping is subject to website structure changes. The code may need updates if the HTML layout changes.


---

This project is a personal learning exercise in data analysis, EDA, and sentiment interpretation using real-world customer feedback data.

