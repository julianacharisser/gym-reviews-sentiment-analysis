# **NLP Analysis for Gym Review Insights**

## **Table of Contents**
1. [Background Information](#background-information)  
2. [Key Findings](#key-findings)  
3. [Main Files and Datasets](#main-files-and-datasets)  
    - [Jupyter Notebooks](#jupyter-notebooks)  
    - [Datasets](#datasets)  
4. [Techniques Used](#techniques-used)  
    - [Keyword Frequency Analysis](#1-keyword-frequency-analysis)  
    - [Word Clouds](#2-word-clouds)  
    - [Topic Modeling using LDA](#3-topic-modeling-using-lda)  
    - [Sentiment Analysis](#4-sentiment-analysis)  
5. [Broader Use Cases of this Project](#broader-use-case-of-this-project)  

## **Background Information**
In the competitive fitness industry, customer satisfaction and workout efficiency are critical to member retention and overall success. Everyday Fitness aims to differentiate itself by addressing members' concerns and improving their gym experience. To achieve this, we conducted a data-driven analysis, focusing on understanding how member experiences can be enhanced and workout efficiency increased.

The project leverages Natural Language Processing (NLP) techniques to analyze reviews from competitor gyms, including Fitness First and Virgin Active. By uncovering insights from customer feedback, we identified patterns, trends, and actionable recommendations for improving Everyday Fitness operations, strategy, and member satisfaction.

Through this project, we aimed to answer a core question: How can Everyday Fitness enhance member satisfaction and workout efficiency while maintaining its competitive edge in the fitness industry?

## **Key Findings**
- **Keyword Analysis:** Positive reviews emphasize friendliness and professionalism; negative reviews highlight issues with staff and equipment.
- **Sentiment by Topic:** Staff and equipment consistently influence satisfaction across all rating levels.
- **Word Clouds:** Visual contrasts between positive and negative feedback revealed actionable areas.

---

## Main Files and Datasets

### Jupyter Notebooks
1. **`combine_datasets.ipynb`**  
   - Purpose: Merges the review datasets from multiple gyms into a unified dataset for analysis.  
   - Key Functionality:
     - Combines CSV files for all outlets, feature engineering, handles missing data, and creates a comprehensive dataset for downstream tasks.
     - Count Plot for Ratings by Year to visualize the number of reviews per rating for each year.

2. **`competitor_gym_reviews_nlp.ipynb`**  
   - Purpose: Performs NLP analysis on the combined dataset to extract insights.  
   - Key Functionality:
     - Keyword frequency analysis over time.
     - Word cloud generation for positive and negative reviews.  
     - Topic modeling (LDA) to uncover recurring themes.  
     - Sentiment analysis by topic and rating level using polarity scores.  

### Datasets
1. **`datasets/`**  
   - Contains the raw review data scraped for each outlet, stored as CSV files.  

2. **`filtered-datasets/`**  
   - Contains processed and filtered datasets for each gym, ready for analysis.  
     
---

## **Techniques Used**

### 1. **Keyword Frequency Analysis**
- **Purpose:** Identify recurring themes, strengths, and weaknesses from the reviews.
- **Methods:** Word tokenization and frequency counts.
- **Tools:** `CountVectorizer`, Python libraries like `nltk` or `spaCy`.

### 2. **Word Clouds**
- **Purpose:** Visualize common words in positive (4–5 stars) and negative (1–2 stars) reviews to contrast key themes.
- **Tools:** Python `WordCloud` library.

### 3. **Topic Modeling using LDA**
- **Purpose:** Discover hidden themes in customer reviews to understand common concerns and strengths.  
- **Methods:** Applied Latent Dirichlet Allocation (LDA) to uncover underlying topics, such as "equipment," "classes," and "staff."  
- **Process:**  
  - Preprocessed text to remove noise (e.g., stop words, punctuation).  
  - Extracted dominant topics for analysis and interpretation.  
- **Tools:**  
  - `gensim` library for LDA implementation
    
### 4. **Sentiment Analysis**
- **Purpose:** Measure the polarity of sentiment for specific topics (e.g., equipment, classes, staff).
- **Process:**
  - Extracted topics using LDA.
  - Computed sentiment polarity using `TextBlob` or similar libraries.
  - Analyzed trends in sentiment across different rating levels.
- **Tools:**  
  - `TextBlob` for sentiment analysis  
  - Python visualization libraries like `matplotlib` and `seaborn` for trend analysis  

---

## Broader Use Cases of this Project
This project provides a robust framework for analyzing textual data using NLP techniques. The methods and tools can be adapted for a wide range of use cases across different industries. Below are some possible applications:

### 1. Feedback Form Analysis
- **Purpose**: Analyze employee or customer feedback forms to understand:
  - What areas are performing well (e.g., satisfaction with service, product quality).
  - Which areas need improvement (e.g., slow response times, lack of features).
- **Example**: An HR team could use this project to process employee feedback and identify recurring themes like "work-life balance" or "communication gaps."

### 2. Competitive Benchmarking
- **Purpose**: Analyze reviews of competitors in your industry to:
  - Learn from their strengths (e.g., friendly staff, engaging features).
  - Avoid their weaknesses (e.g., long wait times, poor customer support).
- **Example**: A company in the hospitality industry can scrape reviews of competing hotels or resorts to identify opportunities to differentiate their offerings.

### Why Use This Framework?
- **Customizable**: Easily adapt the notebooks and analysis techniques to suit your specific dataset and objectives.
- **Scalable**: Works with datasets of any size, from small feedback forms to large-scale online reviews.
- **Actionable Insights**: Provides visualizations (e.g., word clouds, sentiment trends) and data-backed insights to guide decision-making.

With slight modifications, this project can provide valuable insights to help organizations understand customer sentiment, prioritize improvements, and stand out in their respective industries.
