## **IBM Watson Recommendations - README**
### **Project Overview**
This project focuses on building a **recommendation system** for IBM Watson articles using **interaction-based data**. The goal is to **predict relevant articles for users** based on their past interactions, leveraging **rank-based, collaborative filtering, and matrix factorization techniques**.

---

## **📌 Project Components**
### **🔹 Part I: Exploratory Data Analysis (EDA)**
- Analyzed user-article interactions.
- Identified the **most popular articles** and **most active users**.
- Removed duplicate articles and ensured data consistency.

### **🔹 Part II: Rank-Based Recommendations**
- Implemented a **popularity-based recommendation system**.
- Recommended articles based on **the highest number of interactions**.
- Strength: **Works well for new users**.
- Limitation: **Does not provide personalized recommendations**.

### **🔹 Part III: User-User Collaborative Filtering**
- Built a **user-item interaction matrix**.
- Found **similar users** using the **dot product similarity** method.
- Recommended articles based on what **similar users have engaged with**.
- Strength: **Provides personalized recommendations**.
- Limitation: **Fails for new users (Cold Start Problem)**.

### **🔹 Part IV: Improved Collaborative Filtering (Non-Mandatory part of the Project)**
- Enhanced user-user filtering by ranking **users with the most interactions first**.
- Prioritized articles that had **higher interaction counts**.
- Strength: **Reduces random selection bias**.
- Limitation: **Still limited by sparse user interactions**.

### **🔹 Part V: Matrix Factorization with SVD**
- Applied **Singular Value Decomposition (SVD)** to predict article interactions.
- Used **training and test sets** to measure accuracy.
- Observed **higher accuracy with more latent features** but **risked overfitting**.
- Identified **cold start issues**, where **only 20 out of 682 test users had valid recommendations**.

---

## **📊 Model Performance Evaluation**
We tested **how well the recommendation system performed** using the following methods:

1. **Offline Metrics**
   - **Precision & Recall**: Measured how well recommendations matched real user interactions.
   - **F1-Score**: Balanced precision and recall to evaluate accuracy.
   - **NDCG (Normalized Discounted Cumulative Gain)**: Ensured that the most relevant articles were ranked higher.

2. **A/B Testing (Live User Engagement)**
   - **Compared the existing system vs. new recommendation models**.
   - Measured **Click-Through Rate (CTR)** and **User Engagement Time**.
   - Evaluated user **satisfaction surveys** to get qualitative feedback.

---

## **🚀 Key Challenges & Solutions**
### **❌ Cold Start Problem**
- **Issue**: Users with no history cannot receive recommendations.
- **Solution**: Use **rank-based recommendations** for new users.

### **❌ Sparse User-Item Matrix**
- **Issue**: Many articles are interacted with only a few times.
- **Solution**: Use **matrix factorization (SVD)** to generalize patterns.

### **❌ Class Imbalance**
- **Issue**: Some articles receive **too many** interactions while others get **none**.
- **Solution**: Implemented **data resampling** and **class weighting**.

---

## **💡 How to Run the Notebook**
1. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
2. **Run the Jupyter Notebook**:
   ```bash
   jupyter notebook Tiisetso_Masalesa_Recommendations_with_IBM.ipynb
   ```
3. **Follow each section** to see the recommendation models in action.

---

## **📌 Future Improvements**
- **Hybrid Recommendations**: Combine **collaborative filtering + content-based filtering**.
- **Deep Learning Approaches**: Use **Neural Collaborative Filtering (NCF)** for better personalization.
- **Improve Diversity**: Introduce **exploration-based recommendations**.

---

## **✅ Conclusion**
- The **rank-based method is best for new users**.
- The **user-user collaborative filtering works well but has limitations**.
- The **SVD approach improves recommendations** but suffers from cold start issues.
- **A/B testing and offline metrics confirm performance improvements**.

---

### **📧 Author**
📌 **Tiisetso Masalesa**  
📌 **Project: IBM Watson Recommendations**  
📌 **Version: 1.0**  
📌 **Date: [21-02-2025]**  

---
