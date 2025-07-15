# 📊 Personalized Credit Card Offer Recommendation System

## ✅ Project Overview
A machine learning–powered system designed to recommend personalized credit card offers to users based on their transaction behavior, demographics, and product preferences. This project simulates a real-world personalization engine similar to what companies like Crayon Data implement in the fintech and banking sectors.

**Type:** Data Science + Machine Learning + Flask Web App  
**Tech Stack:** Python (pandas, NumPy, scikit-learn, Surprise), Flask, HTML/CSS, SQLite (optional)  
**Goal:** Recommend top 5 offers per user, optimizing for relevance and personalization.

---

## 🔥 Why This Project?
Crayon Data’s platform maya.ai focuses on hyper‑personalization in banking and fintech. This project directly reflects that use case by focusing on credit card offer recommendations using both collaborative filtering and content‑based personalization methods.

---

## ⚙️ System Components

### 1️⃣ Data Collection & Preparation
- **Datasets Used:**
  - UCI Credit Card Dataset (demographics, transaction history)
  - Simulated Offer Acceptance Data (offer_id, user_id, acceptance flag)
- **Data Cleaning:**
  - Handled missing values and outliers
  - Created features like RFM (Recency, Frequency, Monetary Value) and category preferences

### 2️⃣ Modeling Approach
#### ➤ Hybrid Recommendation System
- **Collaborative Filtering:**
  - Implemented using Surprise’s SVD algorithm
  - Built a user–offer interaction matrix based on past offer acceptances
  - Tuned hyperparameters for best Precision@5
- **Content‑Based Filtering:**
  - Created user profiles using demographic and transaction category features
  - Used cosine similarity to match users with offers based on feature vectors
- **Hybrid Method:**
  - Combined scores from both systems using a weighted average
  - Optimized hybrid weights through grid search

**Evaluation Metrics:**  
- Precision@5  
- Recall@5  
- Normalized Discounted Cumulative Gain (NDCG@5)  
- Coverage and novelty scores to avoid repetitive recommendations

### 3️⃣ Flask‑Based Web Application
- Developed a Flask web app for user interaction.
- **Features:**
  - Input user ID → Display top 5 recommended credit card offers.
  - Simple HTML/CSS layout with Bootstrap.
  - Backend logic connects with the recommendation engine via modular Python scripts.

### 4️⃣ Deployment
- Packaged as a Docker container for consistent deployment.
- Tested locally and prepared for deployment via Heroku or AWS Elastic Beanstalk.

---

## 📈 Project Outcomes
- Achieved up to **68% Precision@5** on validation sets.
- Demonstrated effective personalization using both collaborative and content‑based signals.
- Built a deployable, lightweight web interface suitable for real‑world integration.

---

## ✅ Key Learnings & Takeaways
- Practical experience combining machine learning models with Flask backend services.
- Hands‑on exposure to recommendation systems relevant to the fintech sector.
- Deployed a full machine learning pipeline from data collection to model serving.

---

## 💻 Next Steps (For Scaling)
1. Integrate real‑time user feedback loops to refine recommendations.  
2. Connect with a production‑grade database (e.g., PostgreSQL).  
3. Add authentication and user session management.  
4. Deploy to cloud environments with CI/CD pipelines.
