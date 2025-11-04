# Blognews_Sentiment_Analysis
## Project Overview  
This project analyzes a dataset of news articles from **BlogMe**, a blogging and media platform, to uncover patterns in sentiment and engagement.  
Using **Python** for data cleaning and keyword extraction, and **VADER (Valence Aware Dictionary and sEntiment Reasoner)** for sentiment scoring, the analysis identifies positive, negative, and neutral trends across article headlines.  
An interactive **Tableau dashboard** visualizes overall sentiment distribution, top-performing articles, and keyword frequency insights.

---

## Objectives  

- **Keyword Extraction:** Identify and visualize frequently used terms across article headlines.  
- **Sentiment Analysis:** Classify each article as positive, negative, or neutral using VADER.  
- **Engagement Insights:** Explore how sentiment and keyword trends relate to article visibility and engagement.  
- **Visualization:** Build an interactive dashboard to communicate results to non-technical stakeholders.

---

## Data and Preprocessing  

### **Data Source**  
The dataset consists of news article metadata and headlines provided in an **Excel file** from BlogMe’s publishing system.

### **Data Cleaning Steps**  
- **Data Import:** Loaded Excel dataset using `pandas.read_excel()`.  
- **Null Value Handling:** Removed or replaced missing records in headline and sentiment columns.  
- **Text Cleaning:**  
  - Converted all text to lowercase.  
  - Removed punctuation, numbers, and extra spaces.  
  - Tokenized words for frequency analysis.  
- **Feature Derivation:**  
  - Added new columns for **keyword extraction** and **sentiment scores**.  
  - Classified sentiments into *Positive*, *Negative*, and *Neutral* based on compound VADER scores.

---

## Features Overview  

| Feature | Description | Type |
|----------|--------------|------|
| **Headline** | Title or headline of each article | Text |
| **Source** | Publisher or blog platform | Categorical |
| **Date** | Publication date | DateTime |
| **Keyword** | Extracted top words from each headline | Text |
| **Polarity Score** | Compound sentiment score from VADER | Continuous |
| **Sentiment** | Classified sentiment (Positive / Negative / Neutral) | Categorical |

---

## Libraries Used  

**Data Handling:** `pandas`, `numpy`  
**Sentiment Analysis:** `nltk`, `vaderSentiment`  
**Visualization:** `matplotlib`, `seaborn`, `Tableau`  
**Environment:** Jupyter Notebook / Google Colab

---

## Methodology  

1. **Data Import & Exploration:**  
   Loaded the Excel dataset and examined structure, missing values, and key columns.  

2. **Data Cleaning & Transformation:**  
   Cleaned text fields, standardized formatting, and prepared data for sentiment analysis.  

3. **Keyword Extraction:**  
   Applied tokenization and frequency analysis to extract recurring terms from headlines.  

4. **Sentiment Scoring (VADER):**  
   - Used VADER to compute *positive*, *negative*, *neutral*, and *compound* scores.  
   - Classified sentiment categories based on compound thresholds:  
     - `compound ≥ 0.05 → Positive`  
     - `compound ≤ -0.05 → Negative`  
     - otherwise → Neutral  

5. **Data Visualization:**  
   - Created bar charts showing sentiment distribution by source.  
   - Built a word cloud for most common keywords.  
   - Exported results to Tableau for interactive visualization.

---

## Data Visualization  

The **Tableau dashboard** includes:  
- **Sentiment Distribution:** Percentage of positive, negative, and neutral articles.  
- **Top Keywords:** Most frequent words appearing in article headlines.  
- **Top Articles:** Headlines ranked by highest engagement or sentiment intensity.  
- **Source Comparison:** Breakdown of sentiment across different news publishers.  

> Tableau Dashboard: *(Add your Tableau Public link here once published)*  

---

## Results  

- **Sentiment Overview:** Majority of headlines expressed a *neutral or slightly positive tone*, reflecting factual reporting trends.  
- **Top Keywords:** Frequently occurring terms aligned with major news events, political topics, and trending discussions.  
- **Engagement Insights:** Highly positive or highly negative headlines showed higher user engagement than neutral ones.  
- **Dashboard Insights:** The Tableau dashboard enables easy filtering by source, sentiment, and keyword category to explore media tone diversity.

---

## Conclusion  

The **BlogMe Sentiment and Keyword Analysis** project demonstrates how **lexicon-based NLP techniques** can extract actionable insights from large volumes of text data.  
The workflow showcases a full data pipeline — from text preprocessing and sentiment scoring to interactive visualization — enabling media analysts and editors to monitor audience tone and content trends in real time.

---
