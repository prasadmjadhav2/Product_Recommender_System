# 🛍️ Frido Product Recommendation System

## 📌 1. What Problem Were We Solving?

**Problem Statement:**

Develop a **Personalized Product Recommendation System** for **Frido**, an e-commerce platform that sells ergonomic and comfort-focused products such as insoles, cushions, and pillows.

**Key Challenges:**

- Help users find similar products using product descriptions.
- Recommend top-rated products.
- Suggest budget-friendly alternatives.
- Personalize recommendations based on user preferences (e.g., category, price range, rating).
- Segment products into meaningful clusters based on pricing and quality.

---

## 🧠 2. What Approach Did We Use?

### 🤖 Agentic AI-Powered Approach

The AI Agent was designed to:

- Understand product metadata: category, type, name, rating, price.
- Analyze user preferences and return smart, personalized product suggestions.
- Use multiple recommendation strategies for different scenarios:

#### ✅ Strategies:

1. **Content-Based Filtering:**
   - Use **TF-IDF Vectorization** + **Cosine Similarity** to find similar products based on description.

2. **Rating-Based Filtering:**
   - Recommend highly-rated products above a specified threshold (e.g., rating ≥ 4.7).

3. **Price-Based Filtering:**
   - Suggest budget-friendly options while maintaining quality.

4. **Cluster-Based Filtering:**
   - Segment products using **K-Means Clustering** on price and rating.
   - Grouped into:
     - Cluster 0: Premium high-rated products
     - Cluster 1: Mid-priced average-rated products
     - Cluster 2: Budget products with lower ratings

5. **Personalized Filtering:**
   - Combine user preferences (category, price, rating) using a **custom weighted scoring function**.

---

## 📊 Machine Learning Techniques Used

| Technique                 | Description |
|--------------------------|-------------|
| **Content-Based Filtering** | Product similarity via TF-IDF + Cosine Similarity |
| **Clustering**              | Group products using KMeans for analysis |
| **Price Prediction**        | Estimate product price with **Random Forest Regressor** |
| **Feature Engineering**     | Text concatenation for combined similarity scoring |
| **Normalization & Scoring**| Weighted ranking based on user preferences |

---

## 📈 3. Results Achieved

### ✅ Functional Highlights:

- **Similar Product Search:**
  - Example: User searches “Gel Cloud” → Finds similar insoles.

- **Top-Rated Recommendations:**
  - Returns best-rated products (e.g., 4.7+ rating).

- **Budget-Friendly Picks:**
  - Filter products under ₹1000 with high ratings.

- **Product Segmentation:**
  - 3 clusters by **price & rating**:
    - Cluster 0: High-rated, premium
    - Cluster 1: Average-rated, mid-range
    - Cluster 2: Budget, lower ratings

- **Personalized Recommendations:**
  - Example: `"category='Cushions', price<=2000"` → Returns ranked list by preference score.

### 📊 Visualizations:

- 📈 Price distribution by category
- ⭐ Rating distribution
- 💰 Price vs Rating scatter (with cluster coloring)
- 📦 Product count by category

---

## 🎯 Summary Table

| Feature                     | Technique Used                       | Benefit                                  |
|----------------------------|--------------------------------------|------------------------------------------|
| Personalized Recommendations | Weighted scoring + preference filter | Customized output for users              |
| Similar Product Search      | TF-IDF + Cosine Similarity           | Suggests accurate alternatives           |
| Product Grouping            | KMeans Clustering                    | Understand product segments              |
| Price Prediction            | Random Forest Regressor              | Estimate prices for unseen products      |
| Visual Insights             | Matplotlib / Seaborn                 | Trend understanding for business teams   |

---

## 🔮 Future Improvements

- 👥 **User-Based Collaborative Filtering:** Recommend based on similar user behavior.
- 🧠 **Deep Learning Embeddings:** Use **BERT** for better semantic product similarity.
- 🔄 **Feedback Loop:** Learn from user clicks and purchases to improve results.
- 🌐 **Streamlit Web App:** Deploy an interactive UI for real-world testing.
- 🧪 **A/B Testing:** Evaluate multiple recommendation strategies for effectiveness.

---

## ✅ Conclusion

This project demonstrates how to build a **smart AI-powered recommendation engine** for an e-commerce business like **Frido**, using the `frido_dataset.csv`.

It combines **content understanding**, **clustering**, **personalization**, and **visual insights**—paving the way for a production-ready, scalable solution that can drive better user experience and business value.

---
