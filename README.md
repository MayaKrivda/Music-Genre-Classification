# Music Genre Classification

## Overview
This repository contains the code and data used to classify music genres based on song lyrics. The project utilizes various machine learning models to predict the genre of a song given its lyrics.

Main file: `Genre_Classification.ipynb`

## Data
Dataset: https://raw.githubusercontent.com/kitsamho/songlyrics_univeral_sentence_encoder/master/Lyric_data/lyrics.csv'
The dataset consists of song lyrics along with the corresponding artist, song title, and genre.
With total,
- **Number of entries:** 3,288 songs
- **Number of unique genres:** 9
- **Number of unique artists:** 123

## Data Preprocessing
1. **Data Cleaning:**
   - Removed unnecessary columns.
   - Addressed missing song titles and corrected erroneous song titles.
   - Removed songs with instrumental lyrics and duplicates.
   - Applied label encoding to genres.
2. **Text Processing:**
   - Removed punctuation, non-English words, and stopwords.
   - Lemmatized the remaining words.
3. **Filtering:**
   - Removed genres with fewer occurrences to focus on more prominent genres.

Resulting in a final dataset:
- **Number of entries after cleaning:** 2,434 songs
- **Number of unique genres after filtering:** 7

## Used Models
1. **Random Forest Classifier**
2. **Logistic Regression**
3. **Linear Support Vector Classifier (LinearSVC)**
4. **Multinomial Naive Bayes**

## Feature Extraction
- Used TF-IDF Vectorization to convert the processed lyrics into numerical features for model training.

## Model Evaluation
- Models were evaluated using cross-validation and classification metrics such as accuracy, precision, recall, and F1-score.

## Results
The best-performing model was the Logistic Regression, with highest accuracy of 0.632, and lowest of 0.577.

## Conclusion
The Logistic Regression model shows strong performance in classifying genres like **Rock**, **R&B/Soul**, **Metal**, and **Punk**, with a high number of correct predictions. However, it struggles with **Hip-Hop/Rap** and **Alternative**, often confusing them with similar genres, suggesting difficulty in capturing subtle differences in lyrical content.

While models like Logistic Regression and Naive Bayes do not account for word order, others like Random Forests and LinearSVC also demonstrate limitations in this context. To improve accuracy, especially for challenging genre distinctions, further feature engineering or more advanced models that consider word order and context should be explored.




