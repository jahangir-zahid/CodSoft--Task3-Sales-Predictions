# 📈 Sales Prediction Using Python

A machine learning project that predicts product sales based on advertising expenditure across TV, Radio, and Newspaper channels. Built as **Task 4** of the CodSoft Data Science Internship.

---

## 📌 Project Overview

Sales prediction involves forecasting the amount of a product that customers will purchase, taking into account various factors such as advertising expenditure and platform selection. This project uses regression techniques to build a model that accurately estimates sales based on ad spending across different media channels.

---

## 📁 Dataset

- **File:** `advertising.csv`
- **Shape:** 200 rows × 4 columns
- **No missing values** ✅

| Column | Description |
|---|---|
| `TV` | Money spent on TV advertising (in $000) |
| `Radio` | Money spent on Radio advertising (in $000) |
| `Newspaper` | Money spent on Newspaper advertising (in $000) |
| `Sales` | Product sales units ⭐ **(Target Variable)** |

### 📊 Dataset Statistics

| Feature | Min | Max | Mean |
|---|---|---|---|
| TV | 0.7 | 296.4 | 147.04 |
| Radio | 0.0 | 49.6 | 23.26 |
| Newspaper | 0.3 | 114.0 | 30.55 |
| Sales | 1.6 | 27.0 | 15.13 |

---

## 🛠️ Technologies Used

- **Python 3**
- **Pandas** – Data manipulation
- **NumPy** – Numerical operations
- **Matplotlib & Seaborn** – Data visualization
- **Scikit-learn** – Machine learning models & evaluation

---

## ⚙️ Installation & Setup

1. **Clone the repository**
```bash
git clone https://github.com/jahangir-zahid/CodSoft-Task4-SalesPrediction.git
cd CodSoft-Task4-SalesPrediction
```

2. **Install required libraries**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. **Run the script**
```bash
python sales_prediction.py
```

---

## 🔄 Project Workflow

```
STEP 1 : Load Dataset
       ↓
STEP 2 : Data Quality Check
   → No missing values found
   → All features are numeric
       ↓
STEP 3 : Exploratory Data Analysis (EDA)
   → Scatter plots with trend lines
   → Sales distribution
   → Correlation heatmap
   → Avg spend by channel
       ↓
STEP 4 : Prepare Data
   → Features : TV, Radio, Newspaper
   → Target   : Sales
   → Split    : 80% Train / 20% Test
       ↓
STEP 5 : Train 3 Regression Models
   → Linear Regression
   → Random Forest Regressor
   → Gradient Boosting Regressor
       ↓
STEP 6 : Evaluate & Compare Models
   → MAE, RMSE, R² Score, CV R²
       ↓
STEP 7 : Predict Sales for New Budgets
```

---

## 🤖 Models Used & Results

| Model | MAE | RMSE | R² Score | CV R² (5-fold) |
|---|---|---|---|---|
| Linear Regression | 1.2748 | 1.7052 | 0.9059 | 0.8954 |
| Random Forest | 0.9180 | 1.1989 | 0.9535 | 0.9417 |
| **Gradient Boosting** ✅ | **0.8301** | **1.1204** | **0.9594** | **0.9386** |

> 🏆 **Gradient Boosting** performed best with **R² Score of 0.9594** — meaning the model explains **95.9% of sales variation!**

### 📐 Metrics Explained

| Metric | Meaning |
|---|---|
| **MAE** | Mean Absolute Error — average prediction error, lower is better |
| **RMSE** | Root Mean Squared Error — penalizes large errors, lower is better |
| **R²** | How well model explains sales variance, higher is better (max = 1.0) |
| **CV R²** | Average R² across 5 folds — confirms model consistency |

---

## 📦 Sample Sales Predictions

| TV ($000) | Radio ($000) | Newspaper ($000) | Predicted Sales |
|---|---|---|---|
| 200 | 40 | 30 | **20.28** |
| 150 | 20 | 15 | **13.83** |
| 50 | 10 | 5 | **10.02** |
| 100 | 30 | 20 | **14.23** |

---

## 📊 Output Charts

### 1. EDA Analysis (`eda_sales.png`) — 6 Plots
- TV vs Sales scatter with trend line
- Radio vs Sales scatter with trend line
- Newspaper vs Sales scatter with trend line
- Sales distribution histogram
- Correlation heatmap
- Average ad spend by channel

### 2. Model Results (`model_results_sales.png`) — 3 Plots
- Actual vs Predicted sales scatter
- R² Score comparison across models
- Feature importance (Random Forest)

---

## 💡 Key Findings

- **TV advertising** has the strongest impact on Sales — highest feature importance
- **Radio** has a moderate positive effect on sales
- **Newspaper** has the weakest influence among the three channels
- Businesses should **prioritize TV ad spend** to maximize sales
- A **R² of 0.9594** confirms the model is highly accurate and reliable

---

## 📂 Project Structure

```
CodSoft-Task4-SalesPrediction/
│
├── advertising.csv              # Dataset
├── sales_prediction.py          # Main Python script
├── eda_sales.png                # EDA visualization (6 plots)
├── model_results_sales.png      # Model evaluation charts
└── README.md                    # Project documentation
```

---

## 🙋‍♂️ Author

**Jahangir Ali**
- GitHub: [@jahangir-zahid](https://github.com/jahangir-zahid)
- LinkedIn: [Jahangir Ali](https://www.linkedin.com/in/jahangir-ali-51b8a036b/)

---

---

⭐ If you found this project helpful, please give it a star!
