# 📓 ML Foundations — Pandas, NumPy, Matplotlib & Scikit-Learn

The groundwork before the projects — notebooks working through the four core Python data science libraries, each with a walkthrough notebook and a matching set of practice exercises.

![Python](https://img.shields.io/badge/Python-3-3776AB?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plotting-11557C?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

---

## 📚 What I Was Learning

The tools every machine learning project sits on top of. Before building anything end-to-end, I worked through each library on its own — first following along with an introduction notebook, then doing a separate exercises notebook from scratch to make sure it actually stuck.

The libraries in the order they get used in a real workflow:

**NumPy** → arrays and the math → **Pandas** → loading and cleaning the data → **Matplotlib** → seeing what's in it → **Scikit-Learn** → modelling it

---

## 🗂️ What's Here

| Notebook | Topic |
|----------|-------|
| `introduction-to-numpy.ipynb` | Arrays, datatypes, aggregation, reshaping, dot products, sorting |
| `numpy-exercises.ipynb` | NumPy practice problems |
| `introduction-to-pandas.ipynb` | Series & DataFrames, describing, viewing/selecting, manipulating data |
| `pandas-exercises.ipynb` | Pandas practice problems |
| `Introduction to Matplotlib.ipynb` | The pyplot vs. OO API, subplots, plotting from DataFrames, styling |
| `matplotlib-exercises.ipynb` | Matplotlib practice problems |
| `introduction-to-scikit-learn.ipynb` | The full sklearn workflow, in 7 sections (see below) |
| `scikit-learn-exercises.ipynb` | End-to-end classification and regression practice, plus pipelines |
| `example-notebook.ipynb` | A short worked heart disease example |

Sample datasets (`car-sales*.csv`, `heart-disease.csv`) and saved models (`.pkl`, `.joblib`) are included so the notebooks run as-is.

---

## 🔑 Key Things Practiced

**NumPy** — Array creation and attributes, indexing and slicing into matrices, element-wise arithmetic, aggregation (`sum`, `mean`, `std`, `var`), reshaping and transposing, the dot product (worked through a nut butter sales example), comparison operators, and sorting. Plus turning an actual image into a NumPy array to see that images really are just numbers.

**Pandas** — `describe()`, `info()`, and `value_counts()` for getting oriented, `.loc` vs. `.iloc` for selection, filtering with boolean masks, `crosstab()` and `groupby()`, applying functions to columns, handling missing data, and importing/exporting CSVs.

**Matplotlib** — Both the `pyplot` interface and the object-oriented `fig, ax = plt.subplots()` method (and when to use which), subplots, plotting directly from DataFrames, and customizing plots with styles, colors, limits, and legends before saving them to file.

**Scikit-Learn** — The complete workflow, which is the section that most directly fed into the projects that followed:

1. **Getting data ready** — Making everything numerical with `OneHotEncoder` / `ColumnTransformer`, and filling missing values two ways (pandas directly, and `SimpleImputer`)
2. **Choosing an estimator** — Working through the sklearn algorithm cheat sheet for both regression and classification problems
3. **Fitting and predicting** — `fit()`, `predict()`, and `predict_proba()`
4. **Evaluating** — `score()`, the `scoring` parameter, and cross-validation; classification metrics (accuracy, precision, recall, F1, confusion matrix, ROC/AUC) and regression metrics (R², MAE, MSE)
5. **Improving a model** — Tuning hyperparameters by hand, then with `RandomizedSearchCV`, then with `GridSearchCV`
6. **Saving and loading** — Exporting trained models with `pickle` and `joblib`
7. **Pipelines** — Putting preprocessing and modelling into a single `Pipeline`

---

## 🚀 Running It

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
jupyter notebook
```

---

## 💡 What It Taught Me

Doing each library twice — once following along, once from a blank exercises notebook — was the part that made the difference. It's easy to read a `groupby()` and feel like you understand it; it's a different thing to reach for it unprompted when you have a question about the data. The exercise notebooks are where I found out which of the two I actually had.

The order also turned out to matter. Learning NumPy first made Pandas make sense, because a DataFrame is arrays underneath, and learning both made scikit-learn make sense, because `fit(X, y)` just wants numbers in the right shape. Coming at sklearn cold, the error messages about shapes and dtypes would have been mysterious.

The most valuable single thing here is section 0 of the scikit-learn notebook — the end-to-end workflow, front to back, before any of the details. Having the whole shape of the process in mind first meant every later section was filling in a step I already knew the purpose of. That skeleton (get data ready → pick a model → fit → evaluate → improve → save) is exactly what I ran three more times in the projects below.

---

## 🔗 Where This Led

- [End-to-End Heart Disease Classification](https://github.com/ThaiBenjamin/end-to-end-heart-disease) — binary classification on clinical patient data
- [End-to-End Bulldozer Price Regression](https://github.com/ThaiBenjamin/end-to-end-bulldozer-price) — regression on a 400,000-row time series dataset
- [End-to-End Dog Vision](https://github.com/ThaiBenjamin/end-to-end-dog-vision) — 120-class image classification with transfer learning
