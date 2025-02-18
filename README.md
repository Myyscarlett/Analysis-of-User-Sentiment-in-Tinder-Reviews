# Text Analysis of User Sentiment in Tinder Reviews

This repository contains the code and 2 pages report for text analysis in tinder reviews. The data is obtained from Kaggle: https://www.kaggle.com/datasets/shivkumarganesh/tinder-google-play-store-review/data 

## Introduction & Problem Statement

In the digital age, online dating platforms like Tinder play a significant role in social interactions and relationships. Understanding user sentiment and feedback is crucial for improving user experience and addressing concerns. Many users express their opinions about the app through Google Play reviews, which serve as a valuable data source for analyzing customer satisfaction and identifying key areas for improvement. 

By applying text analytics techniques, we can detect recurring issues such as technical bugs, privacy concerns, or dissatisfaction with app features. Tackling this problem is vital for enhancing user retention, increasing customer satisfaction, and improving the app’s reputation, ultimately impacting Tinder’s business success and competitive positioning.

## Analytics Approach

### 1. Data Preprocessing
To ensure structured and clean text data for analysis, the following Natural Language Processing (NLP) techniques were applied:
- **Tokenization**: Breaking down text into individual words for easier manipulation.
- **POS Tagging**: Categorizing words as adjectives, nouns, or verbs to understand their role in sentiment.
- **Lemmatization**: Reducing words to their base form for consistency.
- **Adjective Extraction**: Extracting key sentiment-carrying words.
- **Word Frequency Analysis**: Identifying commonly used descriptive words.
- **Visualization**: Word cloud and frequency distribution to highlight dominant sentiments.

### 2. Sentiment Classification
To classify reviews into positive, negative, and neutral sentiments, two models were implemented and compared:
- **Naïve Bayes Classifier**: Utilized both CountVectorizer and TF-IDF Vectorizer for text transformation. Hyperparameter tuning (alpha 0.1–2.0) resulted in an optimal accuracy of **84.29%** with TF-IDF.
- **K-Nearest Neighbors (KNN) with Cosine Similarity**: TF-IDF-based similarity computation with optimized k = 15 yielded an accuracy of **82.7%**.

#### Model Selection:
Naïve Bayes with TF-IDF was chosen for its superior accuracy and efficiency, despite KNN's strength in similarity-based classification.

### 3. Topic Modeling
Latent Dirichlet Allocation (LDA) was implemented to identify key themes from reviews:
- **Preprocessing**: Removal of stopwords, conversion to lowercase, and exclusion of domain-specific terms like "app" and "tinder".
- **Vectorization**: CountVectorizer and TF-IDF Vectorizer used to transform text.
- **Topic Extraction**: Models trained with 5 and 6 topics, revealing major concerns including **fake profiles, pricing concerns, account bans, subscription issues, and user engagement**.

## Conclusion
Our sentiment analysis provides critical insights that help Tinder improve user retention, enhance monetization strategies, and address key concerns such as fake profiles and privacy issues. By optimizing premium features and refining subscription models, Tinder can boost revenue while ensuring user trust and satisfaction. Furthermore, implementing stronger verification measures and safety features fosters a more secure and inclusive platform. These data-driven enhancements contribute to a sustainable, user-focused business model that strengthens Tinder’s market position and long-term success.


