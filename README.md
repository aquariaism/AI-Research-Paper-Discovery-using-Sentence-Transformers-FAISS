#  AI Research Paper Discovery using Sentence Transformers & FAISS

An end-to-end **Deep Learning and Natural Language Processing (NLP)** project that enables semantic search and intelligent discovery of AI research papers.

Unlike traditional keyword-based search systems, this project understands the contextual meaning of research papers using **Sentence Transformers**, allowing users to retrieve relevant papers through natural language queries.

---

##  Project Overview

Finding relevant research papers from thousands of publications can be time-consuming using traditional keyword search.

This project builds an intelligent **AI-powered Research Paper Discovery System** that:

-  Searches research papers using natural language
-  Understands semantic meaning using Deep Learning embeddings
-  Performs fast similarity search using FAISS
-  Groups similar papers using K-Means Clustering
-  Explores research trends through data visualization

---

##  Features

- Research paper preprocessing and cleaning
- Exploratory Data Analysis (EDA)
- NLP text preprocessing using SpaCy
- Sentence embeddings using Sentence Transformers
- Semantic paper search
- FAISS Vector Database
- K-Means clustering of research papers
- Cluster visualization
- Research trend analysis

---

#  Dataset

**Dataset:** ML-ArXiv-Papers

The dataset contains more than **117,000 Machine Learning research papers** with:

- Research Paper Title
- Research Paper Abstract

---

#  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SpaCy
- Sentence Transformers
- FAISS
- Scikit-learn
- K-Means Clustering

---

#  Project Workflow

## 1️ Data Loading

- Imported the ML-ArXiv Papers dataset
- Converted the dataset into a Pandas DataFrame

---

## 2️ Data Preprocessing

Performed several preprocessing steps:

- Removed unwanted columns
- Removed duplicate papers
- Removed missing values
- Reset DataFrame index
- Combined Title + Abstract into a single text column

---

## 3️ Exploratory Data Analysis

Analyzed the dataset using various visualizations.

### Visualizations

- Distribution of Title Length
- Distribution of Abstract Length
- Top 20 Keywords in Research Paper Titles

These analyses helped understand the structure and characteristics of the dataset.

---

## 4️ Text Preprocessing

Using **SpaCy**, the text was cleaned by:

- Lowercase conversion
- Removing punctuation
- Removing stopwords
- Lemmatization
- Removing unnecessary tokens

---

## 5️ Deep Learning Embeddings

Instead of using TF-IDF or Bag-of-Words, this project uses

**Sentence Transformer**

```
all-MiniLM-L6-v2
```

to generate dense semantic embeddings.

Each research paper is converted into a

```
384-dimensional vector
```

that captures its contextual meaning.

---

## 6️ FAISS Semantic Search

A FAISS vector index was created using the generated embeddings.

This enables extremely fast similarity search across thousands of research papers.

Users can search papers using natural language such as:

```
Deep learning for medical image classification
```

instead of exact keyword matching.

---

## 7️ Research Paper Recommendation

The query is converted into an embedding and compared against the FAISS index.

The system returns the most semantically similar research papers along with:

- Title
- Abstract Preview

---

## 8️ Research Paper Clustering

To discover hidden research domains,

K-Means Clustering was applied on the generated embeddings.

The algorithm grouped similar papers into multiple semantic clusters.

Each cluster represents a different research area within Machine Learning.

---

#  Key Findings

### Research Paper Characteristics

- Most paper titles are concise.
- Abstracts contain significantly richer contextual information.

### Research Trends

Frequently occurring keywords include:

- Deep Learning
- Neural Networks
- Machine Learning
- Classification
- Detection
- Prediction
- Optimization

### Semantic Search

Sentence Transformers successfully retrieved contextually related papers even when exact keywords were absent.

### Clustering

K-Means grouped semantically similar research papers into meaningful research communities.

---

#  Sample Search Query

```
Deep Learning for Medical Image Classification
```

Example Output:

- Deep learning for neuroimaging
- Lung nodule detection using deep learning
- CNN-based medical diagnosis
- Medical image segmentation

---

#  Project Structure

```
AI-Research-Paper-Discovery/
│
├── AI_Research_Paper_Discovery.ipynb
├── README.md
└── requirements.txt
```

---

#  Installation

Clone the repository

```bash
git clone https://github.com/your-username/AI-Research-Paper-Discovery.git
```

Install dependencies

```bash
pip install pandas numpy matplotlib seaborn spacy
pip install sentence-transformers faiss-cpu scikit-learn datasets
```

Download SpaCy model

```bash
python -m spacy download en_core_web_sm
```

Run the notebook

```bash
jupyter notebook
```

---

#  Future Improvements

- AI-powered paper summarization using LLMs
- Interactive Streamlit web application
- Author-based search
- Paper recommendation dashboard
- Citation network visualization
- Research trend forecasting

---

#  Learning Outcomes

Through this project, I gained hands-on experience in:

- Deep Learning for NLP
- Sentence Embeddings
- Vector Databases (FAISS)
- Semantic Search Systems
- Unsupervised Learning (K-Means)
- Research Paper Recommendation Systems
- Exploratory Data Analysis


