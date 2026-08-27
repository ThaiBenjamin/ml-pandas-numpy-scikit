# ML Foundations — Pandas, NumPy, Matplotlib, and Scikit-Learn

The groundwork before the projects. Notebooks working through the four core Python data
science libraries, each with a walkthrough notebook and a matching set of exercises I did
from a blank file afterward.

The libraries in the order they get used in a real workflow: NumPy for arrays and the math,
pandas for loading and cleaning the data, Matplotlib for seeing what's in it, and
scikit-learn for modelling it.

## What's here

| Notebook | Topic |
|---|---|
| `introduction-to-numpy.ipynb` | Arrays, datatypes, aggregation, reshaping, dot products, sorting |
| `numpy-exercises.ipynb` | NumPy practice problems |
| `introduction-to-pandas.ipynb` | Series and DataFrames, describing, viewing, selecting, manipulating |
| `pandas-exercises.ipynb` | Pandas practice problems |
| `Introduction to Matplotlib.ipynb` | pyplot vs. the OO API, subplots, plotting from DataFrames, styling |
| `matplotlib-exercises.ipynb` | Matplotlib practice problems |
| `introduction-to-scikit-learn.ipynb` | The full sklearn workflow, in seven sections |
| `scikit-learn-exercises.ipynb` | End-to-end classification and regression practice, plus pipelines |
| `example-notebook.ipynb` | A short worked heart disease example |

Sample datasets (`car-sales*.csv`, `heart-disease.csv`) and saved models (`.pkl`,
`.joblib`) are included so the notebooks run as-is.

## What each one covers

**NumPy** — Array creation and attributes, indexing and slicing into matrices, element-wise
arithmetic, aggregation with `sum`, `mean`, `std`, and `var`, reshaping and transposing, the
dot product (worked through a nut butter sales example), comparison operators, and sorting.
Plus turning an actual image into an array, to see that images really are just numbers.

**Pandas** — `describe()`, `info()`, and `value_counts()` for getting oriented, `.loc`
against `.iloc` for selection, filtering with boolean masks, `crosstab()` and `groupby()`,
applying functions to columns, handling missing data, and importing and exporting CSVs.

**Matplotlib** — Both the `pyplot` interface and the object-oriented
`fig, ax = plt.subplots()` method, and when each one is the right choice. Subplots, plotting
directly from DataFrames, and customizing with styles, colors, limits, and legends before
saving to file.

**Scikit-learn** — The complete workflow, which is the section that fed most directly into
the projects that followed:

1. Getting data ready — making everything numerical with `OneHotEncoder` and
   `ColumnTransformer`, and filling missing values two ways (pandas directly, and
   `SimpleImputer`)
2. Choosing an estimator — working through the sklearn algorithm cheat sheet for both
   regression and classification
3. Fitting and predicting — `fit()`, `predict()`, `predict_proba()`
4. Evaluating — `score()`, the `scoring` parameter, cross-validation, then classification
   metrics (accuracy, precision, recall, F1, confusion matrix, ROC/AUC) and regression
   metrics (R², MAE, MSE)
5. Improving a model — tuning by hand, then `RandomizedSearchCV`, then `GridSearchCV`
6. Saving and loading — exporting trained models with `pickle` and `joblib`
7. Pipelines — putting preprocessing and modelling into a single `Pipeline`

## Running it

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
jupyter notebook
```

## What I took from it

Doing each library twice — once following along, once from a blank exercises notebook — was
the part that made the difference. It's easy to read a `groupby()` and feel like you
understand it. It's a different thing to reach for it unprompted when you have a question
about the data. The exercise notebooks are where I found out which of the two I actually
had.

The order turned out to matter too. Learning NumPy first made pandas make sense, because a
DataFrame is arrays underneath, and learning both made scikit-learn make sense, because
`fit(X, y)` just wants numbers in the right shape. Coming at sklearn cold, the error
messages about shapes and dtypes would have been mysterious.

The most valuable single thing here is section 0 of the scikit-learn notebook: the
end-to-end workflow, front to back, before any of the details. Having the whole shape of the
process in mind first meant every later section was filling in a step I already knew the
purpose of. That skeleton — get data ready, pick a model, fit, evaluate, improve, save — is
exactly what I ran three more times in the projects below.

## Where this led

- [End-to-End Heart Disease Classification](https://github.com/ThaiBenjamin/end-to-end-heart-disease) — binary classification on clinical patient data
- [End-to-End Bulldozer Price Regression](https://github.com/ThaiBenjamin/end-to-end-bulldozer-price) — regression on a 400,000-row time series
- [End-to-End Dog Vision](https://github.com/ThaiBenjamin/end-to-end-dog-vision) — 120-class image classification with transfer learning
