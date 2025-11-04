# Blognews_Sentiment_Analysis
# 📰 BlogMe Sentiment and Keyword Analysis

## Project Overview  
This project analyzes a dataset of news articles from **BlogMe**, a blogging and media analytics platform, to uncover patterns in **sentiment, keyword frequency, and audience engagement**.  
Using **Python** and the **VADER (Valence Aware Dictionary and sEntiment Reasoner)** sentiment model, article headlines were processed to determine polarity scores (positive, negative, neutral).  
An interactive **Tableau dashboard** visualizes engagement trends, sentiment distributions, top-performing articles, and content sources across multiple news organizations.

---

## Objectives  

- **Keyword Extraction:** Identify and visualize the most frequent terms in article headlines.  
- **Sentiment Analysis:** Use VADER to detect and classify sentiment into positive, neutral, and negative categories.  
- **Engagement Insights:** Explore how sentiment and topic trends affect article reactions, comments, and shares.  
- **Visualization:** Build a Tableau dashboard highlighting sentiment trends, engagement metrics, and source-level comparisons.

---

## Data and Preprocessing  

### **Data Source**  
The dataset consists of article headlines and engagement metrics provided by BlogMe in an **Excel file**.

### **Data Cleaning Steps**  
- Imported dataset using `pandas.read_excel()` for structured processing.  
- Removed null entries and standardized column names.  
- Cleaned headline text by removing punctuation, extra spaces, and converting to lowercase.  
- Applied **keyword extraction** to identify commonly used words.  
- Generated **sentiment scores** using VADER and categorized them into *Positive*, *Negative*, or *Neutral* based on compound values.  
- Saved the transformed dataset for visualization in Tableau.

---

## Features Overview  

| Feature | Description | Type |
|----------|--------------|------|
| **Headline** | News article title | Text |
| **Source** | Publisher name (e.g., CNN, BBC, Reuters) | Categorical |
| **Engagement Count** | Combined engagement metric (likes, shares, comments) | Numerical |
| **Sentiment** | Positive / Negative / Neutral | Categorical |
| **Keyword** | Extracted frequent term in the headline | Text |
| **Date** | Publication date | DateTime |

---

## Libraries Used  

**Data Handling:** `pandas`, `numpy`  
**NLP & Sentiment Analysis:** `nltk`, `vaderSentiment`  
**Visualization:** `matplotlib`, `seaborn`, `Tableau`  
**Environment:** Jupyter Notebook / Google Colab  

---

## Methodology  

1. **Data Import & Exploration**  
   - Loaded Excel dataset into Pandas for exploration.  
   - Assessed missing values and feature distributions.  

2. **Data Cleaning & Transformation**  
   - Standardized column types and cleaned headline text.  
   - Derived sentiment categories using VADER’s compound score thresholds.  

3. **Keyword Extraction**  
   - Tokenized text and identified recurring terms to capture major topics and focus areas.  

4. **Sentiment Analysis (VADER)**  
   - Calculated sentiment intensity scores for each article:  
     - `compound ≥ 0.05 → Positive`  
     - `compound ≤ -0.05 → Negative`  
     - otherwise → Neutral  

5. **Data Visualization**  
   - Built a Tableau dashboard highlighting engagement, sentiment breakdowns, and content source comparisons.  
   - Integrated filters for **publication date** and **source name**.

---

## Tableau Dashboard  

You can explore the interactive dashboard here:  
👉 **[View on Tableau Public](https://public.tableau.com/app/profile/markynsai.lamar/viz/BlockMe_Dashboard/BlogMeNewsDashboard)**  

### **Dashboard Preview**
![BlogMe Dashboard](SCREENSHOT.png)

### **Dashboard Components**  
- **Engagement Over Time:** Displays total engagement trends by publish date (comments, shares, reactions).  
- **Top Negative Sentiment Titles:** Highlights most-engaged negative headlines by total interaction.  
- **Top Positive Sentiment Titles:** Lists most-engaged positive stories and uplifting articles.  
- **Articles Mentioning “Murder”:** Focused analysis of engagement patterns for violence-related news.  
- **Sources by Total Engagement:** Ranks publishers (CNN, BBC, Reuters, etc.) by engagement volume.  
- **Interactive Filters:**  
  - Date range slider (Sept 1 – Nov 30 2019).  
  - Publisher dropdown to isolate specific media sources.

---

## Results  

### **Sentiment Insights**  
- Negative headlines consistently generated **higher total engagement**, indicating stronger audience reaction to emotionally charged or controversial stories.  
- Positive articles—especially human-interest pieces (e.g., *“Astronaut takes stunning photo”*, *“Blessed Are the Refugees”*)—had fewer interactions but showed sustained reader interest.  
- Neutral or factual posts attracted moderate engagement and formed the largest share of total content.

### **Keyword & Topic Trends**  
- Keywords like *murder*, *trial*, and *shooting* dominated high-engagement clusters.  
- Articles involving legal verdicts and public figures drew the largest response peaks.

### **Engagement by Source**  
- **CNN**, **The New York Times**, and **BBC News** emerged as top-engagement sources.  
- US-based publishers showed higher average engagement per story compared to international outlets, suggesting stronger reach or audience activity within certain regions.  

---

## Conclusion  

The **BlogMe Sentiment and Keyword Analysis** provides clear evidence that **news sentiment strongly influences engagement levels**.  
From the dashboard, it’s apparent that:
- Articles with **negative or emotionally charged sentiment** trigger the highest engagement spikes.  
- Positive or inspirational pieces—though fewer—show consistent interest over time.  
- Engagement is highly concentrated among major publishers such as **CNN** and **The New York Times**.  
- Topic-specific sentiment filters (e.g., “Murder” analysis) reveal that sensitive or dramatic headlines tend to dominate interaction metrics.  

This project demonstrates how **Python-driven text analytics combined with Tableau visualization** can help media organizations track audience response, detect content bias, and tailor editorial strategies based on data-driven sentiment insights.

---

## Future Work  

- Add **time-based sentiment trends** to detect shifts in tone during major events.  
- Expand NLP processing with **topic modeling (LDA)** or **Named Entity Recognition (NER)**.  
- Compare **engagement vs. sentiment polarity** over larger datasets and longer timelines.  
- Automate the entire pipeline with scheduled data updates via BlogMe’s internal API.

---

## Dependencies  

```text
pandas
numpy
nltk
vaderSentiment
matplotlib
seaborn
tableau
jupyter

