# 🏡 Machine Learning – Real Estate Price Prediction

This project uses **machine learning** to predict real estate prices in Bangalore using **linear regression** and other models. It demonstrates key data science techniques like **data cleaning**, **feature engineering**, **outlier removal**, **model selection**, and **hyperparameter tuning** — all within a clean and well-commented Jupyter Notebook.

![](images/real_estate_logo_new.png)

---

## 💡 Project Overview

The goal of this project is to predict home prices based on various features such as location, square footage, and number of bedrooms. The dataset is sourced from Kaggle and focuses on properties in **Bangalore, India**.

The workflow includes:
- Identifying and removing outliers
- Handling inconsistent property listings (e.g., 2BHK priced more than 3BHK)
- Feature selection and transformation
- Model training and evaluation using **GridSearchCV** and **K-Fold Cross Validation**
- Deploying the best-performing model (Linear Regression)

---

## 🚀 Features

- 🧹 Data cleaning and handling of inconsistent listings
- 📉 Outlier detection and removal using domain logic
- ⚙️ Model building with Linear Regression, Lasso, and Decision Tree
- 🔁 GridSearchCV and K-Fold for model tuning
- 📈 Visualization of model results and insights
- 🖥️ Jupyter Notebook for interactive development

---

## 🛠️ Technologies Used

- 🐍 **Python**
- 📊 **Pandas & NumPy** – Data manipulation and transformation
- 📉 **Matplotlib** – Data visualization
- ⚙️ **Scikit-Learn** – Machine learning models and tuning
- 🧠 **GridSearchCV & KFold** – Hyperparameter optimization
- 🧾 **Jupyter Notebook** – IDE and experimentation environment

---

## 📁 Project Structure

```
real-estate-price-prediction/
│
├── data/                     # Bangalore home prices dataset
├── images/                   # Project visualizations and logos
├── model/                    # Saved ML model (optional)
├── RealEstatePricePrediction.ipynb  # Main notebook
├── README.md                 # You're reading it!
```

---

## 📊 Data Insights

### ⚠️ Inconsistent Pricing Detected

Some 2BHK homes were priced **higher than 3BHKs** in the same location and with similar area. To fix this, we built a **BHK-level pricing dictionary** to identify and remove such anomalies:

```python
{
    '1': { 'mean': 4000, 'std': 2000, 'count': 34 },
    '2': { 'mean': 4300, 'std': 2300, 'count': 22 }
}
```

We removed 2BHK properties where `price_per_sqft < mean price of 1BHK`.

---

### 📉 Before and After Outlier Removal

#### Rajaji Nagar
![](images/scatter_before_rj.png)
![](images/scatter_after_rj.png)

#### Hebbal
![](images/scatter_before_heb.png)
![](images/scatter_after_heb.png)

---

## 🧠 Model Building & Evaluation

- Trained multiple models:
  - **Linear Regression**
  - **Lasso Regression**
  - **Decision Tree Regressor**
- Used `GridSearchCV` and `K-Fold Cross Validation` to evaluate performance
- ✅ **Linear Regression** yielded the best performance

---

## 🔮 Predictions Example

![](images/predictions.PNG)

---

## 🙌 Credits & Resources

- 📚 Inspired by the excellent tutorials from the [Codebasics YouTube Channel](https://www.youtube.com/c/codebasics)
- 🧠 Dataset Source: [Kaggle – Bangalore Home Prices](https://www.kaggle.com/)
