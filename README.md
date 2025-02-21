# IBM Article Recommendation System

## Project Overview
This project implements a recommendation system for IBM's article-sharing platform, leveraging different techniques to suggest relevant content to users based on their interactions. The project includes multiple approaches:

1. **Rank-Based Recommendations** - Uses the most popular articles as recommendations.
2. **User-User Collaborative Filtering** - Finds similar users and recommends articles based on shared interactions.
3. **Matrix Factorization with SVD** - Uses Singular Value Decomposition (SVD) to predict user-article interactions.

## Files Included
- `Recommendations_with_IBM.ipynb`: Jupyter Notebook containing the full implementation.
- `requirements.txt`: Required dependencies for running the project.
- `README.txt`: Instructions and project description.

## Installation & Setup
Ensure you have Python installed (preferably version 3.7 or higher). Then, install dependencies:

## How to Run
1. Open the Jupyter Notebook:
2. Run each cell sequentially to explore the data, build recommendation models, and evaluate the results.

## Methodology
### **1. Data Exploration**
- Analyzed user-article interactions.
- Identified the most popular articles and the most engaged users.

### **2. Rank-Based Recommendations**
- Recommended articles based on their overall popularity (most views).
- Used for **new users** (cold start problem).

### **3. User-User Collaborative Filtering**
- Found **similar users** based on article interactions.
- Recommended articles based on what similar users interacted with.

### **4. Matrix Factorization (SVD)**
- Applied **Singular Value Decomposition (SVD)** to reduce dimensionality.
- Predicted missing user-article interactions.
- Evaluated SVD performance across different **latent feature sizes**.

## Evaluation & Findings
### **1. Effectiveness of SVD**
- Accuracy increased initially but **did not improve consistently** with more latent features.
- The model struggled with users having limited interactions (**cold start problem**).

### **2. Cold Start Problem**
- Many users in the test set had **no prior interactions**, making collaborative filtering ineffective.
- Used **rank-based recommendations** as a fallback method.

### **3. Best Practices for Future Improvements**
- **A/B Testing**: Compare user engagement using our recommendation model vs. a baseline.
- **Hybrid Recommendations**: Combine rank-based, collaborative filtering, and content-based methods.
- **User Personalization**: Integrate NLP to analyze article content for better matches.

## Results & Conclusion
- **SVD performed well for existing users** but struggled with new users.
- **A hybrid approach** would improve personalization by addressing cold start problems.
- **Future Work**: Implement reinforcement learning or deep learning models for enhanced recommendations.

## Contributors
- **Tiisetso Masalesa**

For questions or feedback, feel free to reach out!
