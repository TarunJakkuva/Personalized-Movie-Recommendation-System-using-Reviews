# Personalized-Movie-Recommendation-System-using-Reviews

# Semantic Movie Recommendation System

An AI-powered personalized movie recommendation system built using the TMDb API, NLP-based review analysis, and semantic similarity search.

This project fetches real-time movie reviews and metadata from TMDb, processes review text using Natural Language Processing (NLP), and generates personalized movie recommendations based on semantic similarity and user preferences.

---

# Features

* Fetch real-time movie data from TMDb API
* Fetch and analyze user reviews
* Genre mapping and metadata enrichment
* NLP preprocessing pipeline
* Semantic similarity-based recommendations
* Personalized recommendation engine
* Explainable recommendations
* Scalable architecture for future AI integration

---

# Project Architecture

```text
TMDb API
   ↓
Movie Metadata + Reviews
   ↓
Data Cleaning & NLP Preprocessing
   ↓
Text Embeddings / Feature Extraction
   ↓
Similarity Engine
   ↓
Personalized Recommendations
   ↓
Frontend / User Interface
```

---

# Tech Stack

| Component              | Technology                           |
| ---------------------- | ------------------------------------ |
| Programming Language   | Python                               |
| API                    | TMDb API                             |
| Data Processing        | Pandas                               |
| NLP                    | NLTK                                 |
| HTTP Requests          | Requests                             |
| Retry Handling         | Tenacity                             |
| ML / Similarity        | Scikit-learn / Sentence Transformers |
| Frontend (Optional)    | Streamlit                            |
| Vector Search (Future) | FAISS                                |

---

# Dataset Source

Movie data and reviews are fetched in real-time using:

## TMDb API

[https://www.themoviedb.org/documentation/api](https://www.themoviedb.org/documentation/api)

---

# Current Workflow

## 1. Fetch Popular Movies

The system retrieves popular movie data including:

* Movie title
* Overview
* Ratings
* Genres
* Popularity
* Release date

---

## 2. Fetch Genres

Genre IDs are mapped into readable genre names.

Example:

```python
[28, 53] → ["Action", "Thriller"]
```

---

## 3. Fetch Reviews

The system collects real-time user reviews for movies using the TMDb reviews endpoint.

---

## 4. NLP Preprocessing

Review text is cleaned and processed using:

* Lowercasing
* URL removal
* Stopword removal
* Tokenization
* Lemmatization

---

## 5. Recommendation Engine

The recommendation system compares semantic similarity between:

* Movie reviews
* Movie descriptions
* User preferences

Future versions will include:

* Transformer embeddings
* Vector similarity search
* Hybrid recommendation models

---

# Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/movie-recommendation-system.git

cd movie-recommendation-system
```

---

# Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Create Environment Variables

Create a `.env` file:

```env
TMDB_API_KEY=your_tmdb_api_key
```

---

# Run Project

```bash
python app.py
```

---

# Example API Endpoints Used

## Search Movies

```bash
https://api.themoviedb.org/3/search/movie
```

## Fetch Popular Movies

```bash
https://api.themoviedb.org/3/movie/popular
```

## Fetch Reviews

```bash
https://api.themoviedb.org/3/movie/{movie_id}/reviews
```

---

# Future Improvements

* Sentence Transformer embeddings
* FAISS vector search
* Streamlit frontend
* User authentication
* Recommendation explainability
* Sentiment analysis
* Mood-based recommendations
* Conversational AI interface
* Hybrid collaborative filtering

---

# Example Recommendation Logic

If a user enjoys:

* Interstellar
* Blade Runner 2049

The system identifies themes such as:

* philosophical sci-fi
* emotional storytelling
* atmospheric cinematography

And recommends:

* Arrival
* Ex Machina
* Moon

---

# Folder Structure

```text
project/
│
├── app.py
├── fetch_movies.py
├── reviews.py
├── preprocessing.py
├── recommender.py
├── utils.py
├── requirements.txt
├── .env
└── README.md
```

---

# NLP Pipeline

The preprocessing pipeline currently includes:

```python
- Lowercasing
- HTML removal
- URL removal
- Tokenization
- Stopword removal
- Lemmatization
```

---

# Example Output

```text
Recommended because reviews emphasize:
- emotional sci-fi themes
- philosophical storytelling
- atmospheric worldbuilding
```

---

# Learning Outcomes

This project demonstrates:

* API integration
* Real-time data pipelines
* NLP preprocessing
* Recommendation systems
* Semantic search
* Data engineering workflows
* AI-powered personalization

---

# Acknowledgements

* TMDb API
* NLTK
* Scikit-learn
* Sentence Transformers

---

# Disclaimer

This project uses TMDb API but is not endorsed or certified by TMDb.

---

# Project Notebook

The initial notebook implementation includes:

* API setup
* Movie fetching
* Genre mapping
* Review collection
* NLP preprocessing

See uploaded notebook content for implementation details. 
