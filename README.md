# Clustering & Classification of BBC News Dataset

## Overview
A voluntary project I did for the Course "Data Science: Foundations" at TU Dresden. The project aims to showcase different approaches in the data science pipeline we discussed during the semester.  This project explores clustering and classification of news articles from the BBC dataset. The goal was to group similar articles based on textual content and subsequently classify unseen data into these clusters using a Support Vector Machine and a Random Forest Classifier. Additional approaches have been added separately as legacy code to showcase alternative Methods that have been discarded.

---

##  Technologies Used

- **Python 3.11**
- **scikit-learn**, **scipy**
- **pandas**, **numpy**
- **Regex**, **nltk**
- **matplotlib**, **seaborn**
- **UMAP**, **PCA**, **t-SNE**
- **Spectral Clustering**
- **Support Vector Machine**
- **Random Forest Classifier**
- **SBERT (Sentence-BERT)** for embeddings

## Additional Technologies Used
- TF-IDF Vectorizer
- KMeans, Elbow Method, Silhouette Score
- DBSCAN, HDBSCAN
- k-Neighbors Graph, Connected Components

---

##  Approach Summary

1. **Data Loading & Exploration**
   - Loaded and explored the BBC News dataset with pre-labeled topics.
2. **Preprocessing**
   - lowercasing, removing punctuation, tokenized, removed stopwords and lemmatized.
3. **Text Embedding**
   - Embedded documents using a lightweight `SentenceTransformer` (SBERT).
4. **Dimensionality Reduction**
   - Applied PCA to reduce embedding dimensionality for clustering while ensuring to retain enough variance.
5. **Cosine Similarity Matrix**
   - Created and scaled to prepare for Clustering.
6. **Clustering**
   - Performed clustering using Spectral Clustering.
   - Evaluated clustering quality with V-Measure as Ground Truth is available.
   - Showcasing Clusters using t-SNE and UMAP.
7. **Classification**
   - Trained a Support Vector Machine and a Random Forest Classifier on the clustered training data.
   - Evaluated model performance on the test set.
8. **Experimentation**
   - Included multiple other approaches for transparency.

---

## Key Results

| Step              | Method                | Result/Notes                         |
|-------------------|------------------------|--------------------------------------|
| Dimensionality Reduction | PCA | Reduced the number of dimensions by ~50% while still retaining ~96% of the variance |
| Clustering        | Spectral Clustering (k=5) | Reasonable separation of topics, V-Measure of 0.75  |
| Classification    | SVM & Random Forest          | Good performance on test split, Average F1 Score of 0.946 & 0.944 respectively |
| Visualization     | 2D projection of clusters | Meaningful separation visible with some overlap of individual datapoints|



