# 📧 Email Spam Detector

This project builds a high-performance binary classifier to detect spam emails using machine learning. It uses the [UCI Spambase Dataset](https://archive.ics.uci.edu/dataset/94/spambase) and compares multiple models to find the most effective classifier.

---

## 🧠 Project Objective

To create a scalable, interpretable, and production-ready spam classifier using:
- Preprocessing pipelines
- Feature analysis
- Multiple models (Logistic Regression, Decision Tree)
- Ensemble techniques (Random Forest, XGBoost, Gradient Boosting, Voting, Stacking)
- Evaluation on hold-out test set

---

## 📂 Dataset Overview

- **Source:** UCI Machine Learning Repository  
- **Samples:** 4,601 email entries  
- **Features:** 57 numerical features (word/char frequency, capital letter patterns)  
- **Target:** `1 = Spam`, `0 = Ham`

---

## ⚙️ Models Compared

| Model              | Train Acc | Val Acc | Test Acc | RMSE    |
|-------------------|-----------|---------|----------|---------|
| LogisticRegression| ~93.1%    | ~92.9%  | –        | –       |
| DecisionTree       | ~92.8%   | ~93.3%  | –        | –       |
| Random Forest      | ~93.2%   | ~94.2%  | –        | –       |
| XGBoost            | ~97.6%   | ~95.9%  | –        | –       |
| Gradient Boosting  | ~97.1%   | ~95.6%  | –        | –       |
| Voting Ensemble    | ~95.6%   | ~95.9%  | –        | –       |
| ✅ Final Stacked Ensemble | **97.2%** | **96.4%** | **93.7%** | **0.25** |

---

## 🧪 Techniques Used

- ✔️ Stratified Train/Val/Test Split  
- ✔️ `RandomizedSearchCV` for hyperparameter tuning  
- ✔️ Learning Curve Visualization  
- ✔️ Confusion Matrix Heatmaps  
- ✔️ Ensemble Learning (Voting + Stacking Classifiers)  
- ✔️ RMSE and Accuracy on Final Test Set  
- ✔️ Reproducibility with fixed random seeds

---

## 📈 Visualization Samples

<p float="left">
  <img src="plots/logreg_confusion_matrix.png" width="300"/>
  <img src="plots/logreg_learning_curve.png" width="300"/>
</p>

<p float="left">
  <img src="plots/xgboost_learning_curve.png" width="300"/>
  <img src="plots/ensemble_confusion_matrix.png" width="300"/>
</p>

---

## 🧩 Final Architecture

```
Raw CSV ➡️ Pandas DataFrame ➡️ Preprocessing ➡️ Model Selection ➡️ Ensemble Voting/Stacking ➡️ Test Evaluation
```

---
## 🧃 Project Structure

```
├── spambase/
│   └── column\_names.py         # Feature name metadata
├── my\_debuggers.py             # Custom NaN checker & plot functions
├── email\_spam\_clf.ipynb        # Main Notebook
├── README.md
└── plots/
└── \*.png                   # Confusion Matrices and Learning Curves
````

---

## 📚 Future Improvements

* 🔍 Add ROC-AUC and threshold tuning
* 🧠 Feature importance from tree models
* 🕸 Deploy via Flask or FastAPI
* 🎯 Use NLP embeddings for semantic spam detection

---

## 🤝 Acknowledgements

* UCI Spambase Dataset
* Scikit-learn, XGBoost, Matplotlib, Seaborn

---
## 📜 License

[MIT License](./LICENSE)

```

---

Let me know if you want:
- `LICENSE` file
- GitHub Pages version (with charts embedded)
- Exportable PDF report version of the notebook

Also upload the `plots/` folder if you want those previews visible on GitHub.
```
