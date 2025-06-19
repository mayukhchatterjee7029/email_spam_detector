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
| Random Forest      | ~93.2%   | ~94.2%  | –        | 24.08   |
| XGBoost            | ~97.6%   | ~95.9%  | –        | –       |
| Gradient Boosting  | ~97.1%   | ~95.6%  | –        | 20.85   |
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
- ✔️ Custom evaluation modules used [Repo link](https://github.com/mayukhchatterjee7029/my_debuggers)

---

## 🧩 Final Architecture

```
Imports ➡️ Preprocessing ➡️ Model Selection ➡️ Ensemble Voting/Stacking ➡️ Test Evaluation
```

---
## 🧃 Project Structure

```
├── spambase/
    ├── spambase.data           # database
│   └── column\_names.py         # Feature name metadata
├── email\_spam\_clf.ipynb        # Main Notebook
└── README.md
```

---
## 📌 Requirements

* Python 3.8+
* scikit-learn
* pandas, seaborn, matplotlib
* xgboost

Install via:

```bash
pip install numpy pandas matplotlib scipy scikit-learn seaborn xgboost
```

---
## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [UCI Machine Learning Repository](https://archive.ics.uci.edu/) for providing the `Spambase Dataset`
- `Scikit-learn` community for excellent machine learning tools
- Contributors and maintainers of all open-source libraries used in this project

---

⭐ If you found this project helpful, please consider giving it a star!
