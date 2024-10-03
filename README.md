## **Title**: Price Prediction Using Product Description
Project as a part of Applied Data Science (16-791) at Carnegie Mellon University

### **Course**: Applied Data Science (Spring 2020)

---

### **Executive Summary**
- **Platform**: Mercari, an online marketplace with over 5 million users and monthly transactions totaling $100 million.
- **Problem**: Sellers often struggle to set appropriate prices for their items, leading to overvaluation or undervaluation.
- **Objective**: To predict optimal product prices using machine learning based on product descriptions and other related features.
- **Solution**: A Ridge Regression model that explains 45% of the price variation, with 50% of predictions within 30% of actual prices.

---

### **Data Description**
- Dataset: 1.4 million product listings from Mercari (Japan and the US).
- **Key features**:
  - `train_id`, `name`, `item_condition_id`, `category_name`, `brand_name`, `price`, `shipping`, `item_description`.
  - The price prediction is primarily influenced by the brand, condition, and description.

---

### **Feature Engineering and Preprocessing**
- **Text Preprocessing**:
  - Removed special characters and stop words.
  - Converted text to lowercase and performed lemmatization.
- **Numerical Features**: MinMaxScaler was applied to normalize numerical features.

### **Modeling Approaches**
- **Linear Regression**: Baseline model with 16.9% R-squared, indicating basic learning.
- **Ridge Regression**: Best performing model with 37.1% R-squared and RMSLE of 0.39.
- **Other Models**:
  - **LightGBM and XGBoost**: R-squared between 34.8% and 36.7%, but not as interpretable as Ridge.
  
---

### **Performance Metrics**
- **RMSLE**: Focused on relative error, helpful in dealing with a wide range of product prices.
- **R-Squared**: Final model captures 45% of the variance in prices.

---

### **Challenges and Risks**
- **Outliers**: High-price items skewing results.
- **Over/Underestimation**: Addressed with cross-validation.
- **Language Barrier**: Dataset only includes English, problematic for non-English platforms.
- **Bundled Items**: Misleading price predictions due to multiple items in a listing.

---

### **Future Recommendations**
- **PySpark**: Use for handling large datasets and high-dimensional text features.
- **Deep Learning**: Potentially more effective for handling unstructured text data.

### **References**
- Various references including academic papers on Bag-of-Words models, overfitting, and price prediction using machine learning.

---
