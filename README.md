# Black Friday Purchase Predictor — XGBoost + Streamlit

> An end-to-end Machine Learning project that predicts customer purchase amounts during Black Friday sales, combining in-depth EDA, XGBoost regression modeling, and a real-time Streamlit web application.

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)](https://github.com/Shubham1919284/black-friday-purchase-prediction)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-FF4B4B?style=flat&logo=streamlit&logoColor=white)](https://github.com/Shubham1919284/black-friday-purchase-prediction)
[![XGBoost](https://img.shields.io/badge/XGBoost-Regression-189AB4?style=flat)](https://github.com/Shubham1919284/black-friday-purchase-prediction)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Pipeline-F7931E?style=flat&logo=scikitlearn&logoColor=white)](https://github.com/Shubham1919284/black-friday-purchase-prediction)
[![Status](https://img.shields.io/badge/Status-Completed-28a745?style=flat)](https://github.com/Shubham1919284/black-friday-purchase-prediction)

---

## App Preview

> Enter customer demographics and product details — get an instant predicted purchase amount.

![App Screenshot](https://github.com/Shubham1919284/black-friday-purchase-prediction/blob/main/app_preview.png)

---

## Project Objective

Black Friday sales generate massive transaction volumes. This project uses historical purchase data to build a regression model that predicts how much a customer is likely to spend — based on who they are and what they are buying.

The end-to-end pipeline covers:
- Exploratory Data Analysis and Feature Engineering
- Training and comparing multiple regression models
- Deploying the best model as an interactive Streamlit web app

---

## Model Performance

| Model | R² Score | RMSE |
|-------|----------|------|
| Linear Regression | — | — |
| Ridge Regression | — | — |
| Lasso Regression | — | — |
| Random Forest | — | — |
| **XGBoost (Best)** | **0.6712** | **2878.57** |

> XGBoost outperformed all other models and was selected for deployment.

---

## Tech Stack

| Layer | Tools |
|-------|-------|
| Language | Python 3.8+ |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | XGBoost, Scikit-Learn |
| Deployment | Streamlit |
| Model Persistence | Joblib |

---

## Project Structure

```text
black-friday-purchase-prediction/
│
├── app.py                                          # Streamlit web application
├── BlackFriday EDA And Feature Engineering.ipynb   # EDA, feature engineering & model training
├── purchase_prediction_model_xgb.pkl               # Serialized XGBoost model
├── train.csv                                       # Training dataset (features + target)
├── test.csv                                        # Test dataset (features only)
└── README.md                                       # Project documentation
```

---

## Dataset

The dataset contains retail sales transactions with the following features:

**Customer Demographics**
- `Gender`, `Age`, `Marital_Status`, `Occupation`
- `City_Category`, `Stay_In_Current_City_Years`

**Product Details**
- `Product_Category_1`, `Product_Category_2`, `Product_Category_3`

**Target Variable**
- `Purchase` — amount spent (in INR)

> Source: [Black Friday Dataset — Kaggle](https://www.kaggle.com/datasets/mehdidag/black-friday)  
> Total Records: 550,000+

---

## Getting Started

**1. Clone the repository**

```bash
git clone https://github.com/Shubham1919284/black-friday-purchase-prediction.git
cd black-friday-purchase-prediction
```

**2. Install dependencies**

```bash
pip install streamlit numpy pandas xgboost scikit-learn joblib matplotlib seaborn
```

**3. Run the Streamlit app**

```bash
streamlit run app.py
```

**4. Open in browser**

```
http://localhost:8501
```

---

## How It Works

1. User inputs customer details (gender, age, city, occupation) and product categories via the Streamlit UI
2. Inputs are encoded and preprocessed to match the training pipeline
3. The pre-trained XGBoost model (`purchase_prediction_model_xgb.pkl`) generates a real-time prediction
4. Predicted purchase amount is displayed instantly on screen

---

## Future Enhancements

- [ ] Add SHAP-based feature importance visualization for model explainability
- [ ] Extend to classification (high / medium / low spender segmentation)
- [ ] Deploy on Streamlit Cloud for public access
- [ ] Add a data upload feature so users can run batch predictions via CSV

---

## Author

**Shubham Kumar Jha**  
B.Tech CSE (Data Science) — Gulzar Group of Institutes, PTU

[![Email](https://img.shields.io/badge/Email-sk1919284@gmail.com-D44638?style=flat&logo=gmail&logoColor=white)](mailto:sk1919284@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-shubham--kumar--jha-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/shubham-kumar-jha-1a2b3c)
[![GitHub](https://img.shields.io/badge/GitHub-Shubham1919284-181717?style=flat&logo=github&logoColor=white)](https://github.com/Shubham1919284)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-4CAF50?style=flat&logo=googlechrome&logoColor=white)](https://shubham1919284.github.io/Portfolio/)

---

*Open-source and free to use for educational and portfolio purposes. Attribution appreciated.*
