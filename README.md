# 🎬 Movie Success Prediction
> *Can data predict a blockbuster before a single frame is shot?*

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?style=for-the-badge&logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📌 Overview

A Machine Learning project that predicts whether a movie will be a **Hit** or a **Flop** based on pre-release features like budget, cast popularity, director score, critic reviews, marketing spend, and more.

Three classification algorithms are trained, compared, and tuned to find the best-performing model.

---

## 📂 Project Structure

```
Movie-Success-Prediction/
│
├── Movie_Success_Prediction_.ipynb   # Main Jupyter Notebook (full pipeline)
├── README.md                         # Project documentation
└── outputs/                          # All visualizations & results
    ├── class_distribution.png
    ├── correlation_heatmap.png
    ├── feature_distributions.png
    ├── genre_success_rate.png
    ├── feature_coefficients.png
    ├── confusion_matrix_nb.png
    ├── roc_curves.png
    └── prediction_results.png
```

---

## 🎯 Objective

Classify movies as **Hit (1)** or **Flop (0)** using supervised machine learning — before the movie is even released.

---

## 📊 Dataset

A **realistic synthetic dataset of 1000 movies** was generated using domain-informed weights to simulate real-world movie data.

| Feature | Description |
|---|---|
| `Budget_M` | Production budget (in million $) |
| `Runtime_min` | Movie duration (minutes) |
| `Cast_Popularity` | Star power score (1–10) |
| `Director_Score` | Director's past success rate (1–10) |
| `Marketing_M` | Marketing spend (in million $) |
| `Num_Screens` | Number of theater screens |
| `Critic_Score` | Critic review score (1–10) |
| `Sequel` | Whether the movie is a sequel (0/1) |
| `Genre` | Movie genre (Action, Drama, Horror, etc.) |
| `Language` | Language of the movie |
| `Release_Season` | Season of release |
| `Success` | **Target** — Hit (1) or Flop (0) |

---

## 🤖 Models Used

| Model | Description |
|---|---|
| 🔵 Naïve Bayes | Gaussian NB — probabilistic baseline |
| 🟢 Logistic Regression | Linear classifier with regularization |
| 🔴 SVM (RBF Kernel) | Non-linear support vector classifier |

---

## 🔁 ML Pipeline

```
Data Generation → EDA → Preprocessing → Train/Test Split
→ Feature Scaling → Model Training → Evaluation
→ Hyperparameter Tuning (GridSearchCV) → Final Comparison
```

---

## 📈 Output Visualizations

### 🎯 Class Distribution: Hit vs Flop
![Class Distribution](outputs/class_distribution.png)

---

### 🔥 Feature Correlation Heatmap
![Correlation Heatmap](outputs/correlation_heatmap.png)

---

### 📊 Feature Distributions: Hit vs Flop
![Feature Distributions](outputs/feature_distributions.png)

---

### 🎭 Success Rate by Genre
![Genre Success Rate](outputs/genre_success_rate.png)

---

### 📌 Logistic Regression — Feature Coefficients
![Feature Coefficients](outputs/feature_coefficients.png)

> Budget, Cast Popularity & Critic Score are the strongest predictors of movie success.

---

### 🔵 Confusion Matrix — Naïve Bayes
![Confusion Matrix NB](outputs/confusion_matrix_nb.png)

---

### 📉 ROC Curves — All Models
![ROC Curves](outputs/roc_curves.png)

| Model | AUC Score |
|---|---|
| 🔵 Naïve Bayes | 0.857 |
| 🟢 Logistic Regression | **0.864** ✅ |
| 🔴 SVM (RBF) | 0.859 |

---

### 🎬 Live Prediction — New Movie
![Prediction Results](outputs/prediction_results.png)

> Action | English | Summer | Budget $150M | All 3 models predicted: **🎉 HIT** with ~95–98% confidence!

---

## 💡 Key Insights

- 📌 **Budget alone doesn't make a hit** — Cast Popularity & Critic Score are stronger signals
- 📌 **Logistic Regression** achieved the best ROC-AUC of **0.864**
- 📌 **Romance & Horror** genres showed the highest success rates (78.1% & 75.8%)
- 📌 **Num_Screens** showed a slight negative coefficient — wide releases don't guarantee success
- 📌 All 3 models predicted the hypothetical $150M Action movie as a **HIT** with 95–98% confidence

---

## 🛠️ Tech Stack

- **Language:** Python 3.10+
- **Libraries:** NumPy, Pandas, Matplotlib, Seaborn, Scikit-Learn
- **Environment:** Jupyter Notebook

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/luckylucky110507/Movie-Success-Prediction.git

# 2. Navigate into the folder
cd Movie-Success-Prediction

# 3. Install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn jupyter

# 4. Launch the notebook
jupyter notebook Movie_Success_Prediction_.ipynb
```

---

[![GitHub](https://img.shields.io/badge/GitHub-luckylucky110507-black?style=flat&logo=github)](https://github.com/luckylucky110507)

---

> *"Data doesn't lie. Hollywood sometimes does."* 🎥
