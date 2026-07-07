# Distributed Hyperparameter Optimization Using Ray Tune

A machine learning project that demonstrates **distributed hyperparameter optimization** using **Ray Tune** on an **XGBoost classifier** trained on the Titanic dataset. The project compares the performance of the default XGBoost model, traditional Grid Search, and Ray Tune's scalable distributed search to identify the best-performing hyperparameters efficiently.

---

## Project Overview

Hyperparameter tuning is one of the most computationally expensive stages of machine learning. This project explores how **Ray Tune** can significantly simplify and scale the search process by running multiple trials in parallel.

The notebook includes:

- Data loading and preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering
- Data preprocessing pipeline
- Baseline XGBoost model
- Hyperparameter tuning using GridSearchCV
- Distributed hyperparameter optimization using Ray Tune
- Performance comparison of different approaches

---

## Dataset

This project uses the **Titanic - Machine Learning from Disaster** dataset.

Target Variable:

- **Survived**

Features include:

- Passenger Class
- Sex
- Age
- Fare
- Embarked
- Family Size (engineered feature)
- SibSp
- Parch

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Ray Tune

---

## Project Workflow

```
Data Collection
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Feature Engineering
        │
        ▼
Data Preprocessing Pipeline
        │
        ▼
Baseline XGBoost Model
        │
        ├──────────────► GridSearchCV
        │
        └──────────────► Ray Tune
                           │
                           ▼
               Best Hyperparameters
                           │
                           ▼
                 Final Model Evaluation
```

---

## Hyperparameter Optimization

### Baseline Model

An XGBoost classifier is first trained using default parameters to establish a performance benchmark.

---

### Grid Search

The notebook performs an exhaustive search over parameters such as:

- `max_depth`
- `n_estimators`
- `learning_rate`
- `gamma`

using **GridSearchCV**.

---

### Ray Tune

The project then performs distributed optimization using **Ray Tune**.

Hyperparameters explored include:

- `max_depth`
- `n_estimators`
- `learning_rate`
- `gamma`

Ray Tune automatically executes hundreds of trials and returns the configuration that maximizes cross-validation accuracy.

---

## Model Evaluation

The models are evaluated using:

- Cross Validation
- Accuracy
- F1 Score

Comparison includes:

- Default XGBoost
- Grid Search Optimized XGBoost
- Ray Tune Optimized XGBoost

---

## Repository Structure

```
.
├── xgboostAndRaytune2.ipynb
├── README.md
└── requirements.txt
```
---

## Key Learning Outcomes

- Building end-to-end ML pipelines
- Feature engineering for structured datasets
- XGBoost model training
- Hyperparameter optimization techniques
- Distributed tuning with Ray Tune
- Comparing traditional and distributed search strategies

---

## Future Improvements

- Bayesian Optimization
- Optuna integration
- HyperOpt comparison
- MLflow experiment tracking
- Distributed training on multiple nodes
- Model deployment

---

## References

- Ray Tune Documentation: https://docs.ray.io/en/latest/tune/
- XGBoost Documentation: https://xgboost.readthedocs.io/
- Scikit-learn Documentation: https://scikit-learn.org/
