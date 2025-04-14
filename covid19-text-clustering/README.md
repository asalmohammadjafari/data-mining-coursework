# 🧠 COVID-19 Research Clustering and Topic Modeling

## Overview

This project analyzes 10,000 COVID-19 research papers to:
- Group similar papers using clustering.
- Extract key topics for each group using topic modeling.

The goal is to make the overwhelming volume of research more accessible through automation.

## Pipeline

### 🧹 Preprocessing
- **Language Filtering**: Remove non-English texts (`langdetect`)
- **Tokenization & Lemmatization**: Using `en_core_sci_lg` from SciSpaCy
- **Cleaning**: Remove stopwords and punctuation

### 📊 Feature Engineering
- **TF-IDF** vectorization
- **PCA** for dimensionality reduction (95% variance retained)

### 📌 Clustering
- **K-Means**, **Hierarchical**, and **DBSCAN**
- Evaluated using:
  - Silhouette Score
  - Calinski-Harabasz
  - Davies-Bouldin

### 📈 Visualization
- **t-SNE** to view clusters in 2D

### 🗂 Topic Modeling
- **LDA**, compared with **NMF** and **LSA**

## 🔧 Requirements

```bash
pip install pandas nltk spacy sklearn gensim matplotlib seaborn langdetect scispacy
python -m spacy download en_core_sci_lg
