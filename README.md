## Hotel Review Sentiment Analysis

**Overview**

This project aims to perform sentiment analysis on hotel reviews to classify them as positive or negative. It explores features such as review length, word frequency, and sentiment distribution to understand the factors that contribute to positive and negative guest experiences.

**Project Workflow**

1. **Data Loading and Preprocessing:**
    - **Source:** `review_hotel.csv` (Original dataset containing hotel reviews)
    - **Steps:**
        - Merged positive and negative reviews into a single column.
        - Created a binary label ("is_bad_review") based on the `Reviewer_Score`.
        - Cleaned the data by removing irrelevant tokens (e.g., "No Negative", "No Positive").
        - Applied text processing techniques:
            - Tokenization
            - Stop word removal
            - Part-of-speech tagging (optional, if used)
            - Lemmatization
    - **Output:** `123.csv` (Preprocessed data after cleaning and transformations)

2. **Feature Engineering:**
    - Added sentiment scores (neg, neu, pos, compound) using NLTK's `SentimentIntensityAnalyzer`.
    - Extracted additional features:
        - Character count (`nb_chars`)
        - Word count (`nb_words`)
    - Created TF-IDF features for high-dimensional text representation.
    - Output: `df1.csv` (Dataframe with engineered features and sentiment scores)

3. **Exploratory Data Analysis (EDA):**
    - Visualized word clouds for positive and negative reviews.
    - Identified reviews with extreme positive and negative sentiments.
    - Analyzed sentiment score distributions for good and bad reviews.
    - Conducted exploratory analysis on other features (e.g., review length, word count) to understand their relationship with sentiment.

**Key Features**

* **Sentiment Analysis:** Accurate classification of reviews as positive or negative.
* **Feature Engineering:** Extraction of relevant features for improved model performance.
* **Exploratory Data Analysis:** Insights into the factors influencing sentiment.

**Tools and Libraries**

* **Pandas:** Data manipulation and analysis.
* **NLTK:** Natural Language Toolkit (for tokenization, stop word removal, lemmatization, sentiment analysis).
* **Scikit-learn:** Machine learning library (for TF-IDF vectorization and model training).
* **Matplotlib, Seaborn:** Data visualization libraries.
* **WordCloud:** For generating word cloud visualizations.

**Usage**

1.  **Install dependencies:**
   ```bash
   pip install pandas nltk scikit-learn matplotlib seaborn wordcloud
