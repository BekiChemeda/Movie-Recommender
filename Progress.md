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



---

# Day 2 – November 21, 2025

## What I Learned

Today I tried to explain cosine similarity without mentioning its formula. On my second day, I learned about cosine similarity **in depth**. I used videos from **StatQuest** and **Data Mentor**, which really helped me understand the concept clearly.  

Lemme explain it a little:

Let's say we are finding the similarity between **"Good Morning"** and **"Good"**.  

First, let's count each word in both phrases:

| No | Good Morning | Good |
|----|--------------|------|
| Good | 1 | 1 |
| Morning | 1 | 0 |

After counting how many times each word appears, we can visualize it:  
- Let **X-axis = Morning**, **Y-axis = Good**  
- Plot a dot based on the table data, starting from (0,0)  
- Draw a line to each point: Good (1,1) and Morning (1,0)  

The angle between these two lines is **45°**, and **cos(45°) = 0.71**, which is the similarity between them.  

- If we compare **Good Morning vs Good Morning**, the angle = 0 → similarity = 1  
- If we compare **Good Morning vs Eating Lunch**, the angle = 90° → similarity = 0  

But as you notice, with more than 3 words, it becomes impossible to draw.  

So we use the general **cosine similarity formula**:

Cosine similarity = (Σ_i A_i B_i) / (√(Σ_i A_i^2) · √(Σ_i B_i^2))

Where:
- Σ_i A_i B_i = sum over i of A_i times B_i (dot product)
- √(Σ_i A_i^2) = magnitude of A
- √(Σ_i B_i^2) = magnitude of B

Where:  
- \(A_i\) and \(B_i\) are the word counts (or features) of the two vectors.  

**Example with "Good Morning" and "Good":**

- \(A = [1, 1]\) (Good Morning)  
- \(B = [1, 0]\) (Good)  

Cosine similarity = ((1 * 1) + (1 * 0)) / (sqrt(1^2 + 1^2) * sqrt(1^2 + 0^2)) = 1 / (sqrt(2) * 1) ≈ 0.707 ≈ 0.71

---

Now that I understand the basic formula, tomorrow I will try to **implement it in Python**.  
But before that, I will **choose a dataset** and explore it before starting to play with cosine similarity.

---

# Day 3 - November 23, 2025
## What I learned

For the past days I have been exploring different datasets for building my movie recommender system. I finally settled on the **MovieLens 100K dataset** because it is well-structured and widely used in recommender system research and more than that it wasn't this much huge to be computed. I tried the large datasets like 1M and above and they were too large when we try to change them into a user-item matrix. 

After Downloading the dataset, I explored it a bit to make myself familiar with its structure. Then I started implementing cosine similarity in Python using NumPy. I created two sample vectors and calculated the cosine similarity between them using the formula I learned earlier. Actually I didn't use the formula directly, instead I used NumPy's built-in functions to compute the dot product and magnitudes, which made the implementation easier and more efficient. I didn't use the formula directly, doesn't mean knowing the formula is not important, actually it is very important to understand the concept behind it. 

So Yesterday I tried to implement collaborative filtering using cosine similarity in two ways: user based Collaborative Filtering and item(movie) based collaborative Filtering. 

Just to explain; the user-based collaborative filtering recommends movies to a user based on the preferences of similar users. For example, if User A and User B have similar tastes, and User A liked Movie X, then Movie X can be recommended to User B. While item-based collaborative filtering recommends movies similar to those a user has liked in the past. For example, if a user liked Movie Y, and Movie Z is similar to Movie Y, then Movie Z can be recommended to that user.

The link for both implementations  can be found below.
- [For Item based](https://github.com/BekiChemeda/Movie-Recommender/blob/main/Collaborative%20Filtering/Cosine%20Similarity/cosine-similarity-Item-based-recommender-sy.ipynb)
-  [For User based ](https://github.com/bekichemeda/Movie-recommender/Cosine-Filtering/Cosine-Similarity.ipynb)
