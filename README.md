# Movie-Recommender-System

# 🎬 Movie Recommender System

A content-based movie recommendation system that suggests **top 5 similar movies** based on user selection.

---

## 🚀 Features

* Select a movie using a dropdown (search-enabled)
* Get **top 5 similar movie recommendations**
* Simple and interactive UI built with Streamlit
* Fast recommendations using precomputed similarity matrix

---

## 🧠 How It Works

This system uses **content-based filtering**:

### 1. Data Preprocessing

* Datasets used:

  * TMDB 5000 Movies
  * TMDB 5000 Credits
* Merged both datasets on movie title
* Selected important features:

  * genres
  * keywords
  * overview
  * cast
  * crew

---

### 2. Feature Engineering

* Combined all selected features into a single text column
* Cleaned data (removed spaces, formatting issues)
* Converted text data into a structured format

---

### 3. Vectorization

* Used **CountVectorizer** to convert text into numerical vectors

---

### 4. Similarity Calculation

* Used **cosine similarity** to measure similarity between movies
* Generated a similarity matrix for all movies

---

### 5. Recommendation Logic

* When user selects a movie:

  * Find its index
  * Retrieve similarity scores
  * Sort and return **top 5 most similar movies**

---

## 🖥️ Application UI

* User selects a movie from a dropdown (with search)
* Clicks on **"Recommend"**
* System displays **top 5 similar movies**

---

## 🛠 Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* Streamlit

---

## 📂 Project Structure

* `app.py` → Streamlit application
* `movies.pkl` → Processed movie data
* `movie_dict.pkl` → Movie dictionary
* `similarity.pkl` → Similarity matrix (not uploaded due to size limit)
* `movie_recommender_system.ipynb` → Model building

---

## ⚠️ Important Note

The file `similarity.pkl` is not uploaded due to GitHub file size limits (>100MB).

To run this project:

1. Open the Jupyter Notebook
2. Run all cells to generate `similarity.pkl`
3. Then run the Streamlit app

---

## ▶️ Run Locally

```bash
pip install -r requirements.txt
streamlit run app.py
```

---

## 📌 Future Improvements

* Add movie posters using TMDB API
* Display ratings and movie overview
* Deploy the application online
* Improve recommendation quality using advanced NLP

---

## 👤 Author

Akshat Mehta
