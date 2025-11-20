# Movie Recommender System

## Why I Created This Project
I believe the best way to truly learn something is by **building it myself**. That’s why I created this repository: to build a **Movie Recommender System** while learning **Machine Learning** and **Recommender Systems** step by step.

I started this project on **November 19, 2025**. At this point, I only have a basic understanding of machine learning concepts and know that recommender systems are widely used on platforms like Netflix, YouTube, and Amazon.

This repo is my **learning journey**. I aim to:
- Learn **Collaborative Filtering**, **Content-Based Filtering**, and **Hybrid models**.
- Document **daily progress, challenges, and solutions** in this file so others can learn from my experience.
- Gradually build a **fully functional hybrid recommender system** that predicts and suggests movies.

Even if I miss some days, I will continue documenting and coding as consistently as possible.

---

# Day 1  
## What I Did Today

Today I explored the **Introduction to Recommender Systems**.  
I learned that there are **three main categories** of recommender systems, and I tried to understand each of them in depth. I used **Krish Naik’s YouTube channel**, which I found very helpful and will continue using as a learning resource.

### 1. Collaborative Filtering
As the name suggests, this method works based on **collaboration between users**.  
The idea is that some users tend to like similar types of movies.  
So if:
- User A and User B have similar taste  
- User A has watched and liked Movie X  
- User B hasn’t watched Movie X  

Then Movie X is a good recommendation for User B.

### 2. Content-Based Recommendations
Recommends items based on the **content/features** of items the user has liked before.  
(Example: genres, descriptions, tags.)

### 3. Hybrid Systems
A combination of both Collaborative Filtering and Content-Based Filtering.

---

## What I Learned Today

- **Recommender Systems are not always ML models.**  
  Many of them rely on **mathematical techniques**, not training a machine learning model.

- We can create a user–movie rating matrix:  
  - Users in rows  
  - Movies in columns  
  - Cells contain the user’s rating for that movie

- We can compute **cosine similarity** between users to measure how similar their tastes are.  
  - If two users have a high similarity score, and one user likes a movie the other hasn’t seen, it becomes a strong candidate for recommendation.

- **Key concepts introduced today:**
  - Cosine similarity  
  - Weighted average  
  - Correlation  
