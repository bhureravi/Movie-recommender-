# 🎬 Movie Recommender System

Welcome to the Movie Recommender System! This is a machine learning-powered web application that suggests movies based on your interests. If you love a specific movie, this system will find and recommend 5 similar movies, complete with their official posters!

## 💡 What is this project?

This project uses **Content-Based Filtering** to recommend movies. Instead of tracking what other users click on, it looks at the actual "content" or DNA of the movies themselves. 

By analyzing thousands of movies from the TMDB 5000 Movies dataset, the system looks for patterns in:
* **Genres:** (e.g., Action, Sci-Fi, Comedy)
* **Keywords:** (e.g., "space travel", "time machine")
* **Cast:** The top 3 actors
* **Crew:** The director
* **Overview:** The plot summary

## 🧠 How it Works (Under the Hood)

1. **Data Preprocessing:** We combine the plot, genres, cast, and director into one giant block of text (called "tags") for every single movie.
2. **Vectorization:** Using `CountVectorizer`, we convert these text tags into mathematical vectors (a matrix of numbers) with a maximum of 5000 features.
3. **Cosine Similarity:** To find similar movies, we calculate the mathematical angle (cosine distance) between these vectors. Movies that are similar will have vectors that point in the same direction!
4. **API Integration:** We use the official TMDB API to fetch high-quality posters for the recommended movies in real-time.

## 🛠️ Tech Stack

* **Python:** The core programming language.
* **Pandas & NumPy:** For cleaning and manipulating the dataset.
* **Scikit-Learn:** For text vectorization and cosine similarity calculations.
* **Streamlit:** For building the interactive web application UI.
* **TMDB API:** For dynamically fetching movie posters.

---

## 🚀 How to Run the Project Locally

Follow these steps to get the app running on your own machine!

### 1. Clone the Repository
```bash
git clone [https://github.com/Amay06/Movie-Recommender.git](https://github.com/Amay06/Movie-Recommender.git)
cd Movie-Recommender