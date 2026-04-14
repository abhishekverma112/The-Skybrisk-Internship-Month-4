# 🎬 Content-Based Movie Recommendation System

## 🚀 Project Overview

This project builds a **Content-Based Movie Recommendation System** using Natural Language Processing (NLP) techniques.
The system recommends movies similar to a given movie based on features like **overview, genres, keywords, cast, and crew**.

Unlike collaborative filtering, this approach does **not depend on user data**, making it effective for **cold-start problems**.

---

## 🎯 Objective

To develop a recommendation engine that:

* Analyzes movie content
* Converts textual data into numerical vectors
* Uses similarity measures to recommend top similar movies

---

## 📂 Dataset

* TMDB 5000 Movie Dataset (Kaggle)
* Files used:

  * `tmdb_5000_movies.csv`
  * `tmdb_5000_credits.csv`

---

## 🛠️ Tech Stack

* **Programming Language:** Python
* **Libraries:**

  * Pandas, NumPy
  * Scikit-learn
  * NLTK
  * Matplotlib, Seaborn
  * WordCloud

---

## ⚙️ Project Workflow

### 1️⃣ Data Collection & Merging

* Loaded movies and credits datasets
* Merged datasets on movie title

---

### 2️⃣ Data Cleaning

* Removed null values
* Selected important columns:

  * movie_id, title, overview, genres, keywords, cast, crew

---

### 3️⃣ Feature Engineering

* Extracted:

  * Genres
  * Keywords
  * Top 3 Cast Members
  * Director (from crew)
* Combined all features into a single **tags column**

---

### 4️⃣ Text Preprocessing

* Converted text to lowercase
* Removed spaces between words
* Applied **stemming** using PorterStemmer

---

### 5️⃣ Vectorization

* Used **CountVectorizer**
* Converted text into numerical feature vectors (Bag of Words model)

---

### 6️⃣ Similarity Calculation

* Applied **Cosine Similarity**
* Created similarity matrix between all movies

---

### 7️⃣ Recommendation System

* Built a function:

  ```python
  recommend(movie_name)
  ```
* Returns top 5 similar movies

---

## 📊 Data Visualization

Performed Exploratory Data Analysis (EDA) using:

* 📈 Line Chart → Movies released per year
* 📊 Bar Chart → Top genres
* 📦 Box Plot → Runtime distribution
* 📉 Histogram → Ratings distribution
* ☁️ WordCloud → Frequent keywords

---

## 🧪 Example

```python
recommend("Batman Begins")
```

### Output:

```
The Dark Knight
Batman
Batman Returns
Batman Forever
Batman & Robin
```

---

## 💾 Model Saving

* Saved processed data and similarity matrix using `pickle`
* Files:

  * `movies.pkl`
  * `similarity.pkl`

---

## 🌐 Future Improvements

* Build a **Streamlit web app**
* Add **movie posters using TMDB API**
* Implement **hybrid recommendation system**
* Use **TF-IDF or Deep Learning models**

---

## 📌 Key Insights

* Most movies belong to **Action & Drama genres**
* Majority of movies released after **2000**
* Ratings generally range between **5 to 7**
* Average runtime is around **90–120 minutes**

---

## 🎯 Conclusion

This project demonstrates how **NLP and cosine similarity** can be effectively used to build a scalable recommendation system.
It is a strong foundation for building advanced systems like **Netflix or Amazon Prime recommendations**.

---

## 🙌 Acknowledgment

Dataset sourced from **Kaggle - TMDB 5000 Movie Dataset**

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and feel free to contribute!

---
