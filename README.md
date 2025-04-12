# 🎬 Movie Recommendation System: A Content-Based Approach from a Business Perspective

![Movie Recommendation Banner]https://github.com/Jamestown34/Movie-Recommendation/blob/main/images/Screenshot%20(41).png <!-- 🔁 Replace with your image URL -->

## 📌 Introduction

### 💡 Project Description

In today's fast-paced entertainment landscape, user retention and engagement are critical business goals. Platforms like **Netflix**, **Amazon Prime**, and **Disney+** heavily depend on intelligent recommendation systems to keep users engaged and boost subscriptions.

This project addresses a real-world business need for **personalized movie recommendations** by building a **Content-Based Recommendation System** using genre and plot overview data.

> **🧠 Business Problem:**  
> "How can we improve user engagement and retention on streaming platforms using intelligent movie recommendations?"

---

## 🧰 Tools & Technologies

- `Python`
- `TMDB API`
- `Pandas`
- `Scikit-learn` (TF-IDF & Cosine Similarity)
- `Gradio` (Web App Interface)

---

## 🎯 Problem Statement

Without effective recommendations, users struggle to find content they enjoy — leading to high churn and low engagement.

We solve this problem by using **text similarity on genres and overviews** to recommend movies that align with the user's preferences.

---

## 🛠️ Project Objectives

- ✅ Fetch and clean movie data using TMDB API  
- ✅ Use TF-IDF + Cosine Similarity to build the recommender  
- ✅ Deploy with a simple web interface via Gradio  
- ✅ Show how this can drive **real business value**

---

## 📊 The Data

We collected up to **1000 movies** using the [TMDB API](https://www.themoviedb.org/documentation/api).  
Key features extracted:

- 🎬 Title  
- 📝 Overview  
- 🧩 Genres  
- 📊 Popularity  
- 🌟 Ratings  
- 🗓️ Release Date  

---

## 🔧 Methodology

### 1️⃣ Data Collection

Registered for a TMDB API Key and used Python's `requests` library to extract movie data. We retrieved popular movies using the `/discover/movie` and `/genre/movie/list` endpoints.

---

### 2️⃣ Data Cleaning & Preprocessing

![Data Cleaning](https://your-second-image-link.com) <!-- 🔁 Replace with actual image URL -->

- Filled missing overviews → `"No overview available"`  
- Filled unknown release dates → `"Unknown"`  
- Mapped genre IDs to genre names  
- Converted list of genres → space-separated string (e.g., `"Action Comedy"`)  
- Created `combined_text = overview + genres` for vectorization  

---

### 3️⃣ Model Selection: TF-IDF + Cosine Similarity

- Used `TfidfVectorizer()` from `scikit-learn` to vectorize the combined text  
- Used `cosine_similarity()` to compute the distance between vectors  
- Returned **Top 5 similar movies** based on cosine similarity  

📈 **Why This Model?**

- ✅ Lightweight & fast  
- ✅ Ideal for content-based text similarity  
- ✅ Doesn't need a GPU or large dataset  
- ✅ Easily deployable in real-time

---

### 4️⃣ Web App Interface with Gradio

To make the system interactive, we built a simple UI using **Gradio**.

![Gradio UI](https://your-third-image-link.com) <!-- 🔁 Replace with actual image URL -->

Users can:

- 🔍 Enter a movie name  
- 🤖 Receive 5 similar movies based on overview + genre similarity  

#### 🧪 Example Output

> **User Search:** Maze Runner  
> **Recommendations:**  
> 1. Maze Runner: The Death Cure  
> 2. Maze Runner: The Scorch Trials  
> 3. Tomorrow Before After  
> 4. Comis Chaos  
> 5. Deva  

---

## ✅ Results & Business Value

🎯 This model is a proof-of-concept that shows how **AI-driven recommendations** can drive:

- 📈 Increased user watch time  
- 💰 More subscriptions  
- 🔁 Reduced churn  
- 🤝 Improved customer experience  

---

## 🚀 Next Steps

- 🔄 Combine with Collaborative Filtering (Hybrid Model)  
- 🧠 Use deep learning-based embeddings for better text representation  
- 🌍 Scale up to multi-language, multi-platform movie suggestions  

---

## 🧠 Lessons Learned

This project illustrates how even simple machine learning models like TF-IDF and Cosine Similarity can be deployed effectively to solve **real business problems** in media and entertainment.

![Business Outcome](https://your-last-image-link.com) <!-- 🔁 Replace with actual image URL -->

---

## 🤝 Acknowledgements

Thanks to [The Movie Database (TMDB)](https://www.themoviedb.org/) for their incredible open API and data.

---

> 💡 Feel free to fork this repo, explore the code, or reach out if you're working on similar projects!
