# Machine Learning and Evolutionary Computation

Two Jupyter notebooks from my computing degree at the University of Plymouth. Part 1 trains classifiers to predict climate model simulation failures. Part 2 uses a genetic algorithm to search for the minimum of a test function.

| Notebook | What it does | Tech |
|---|---|---|
| [Part 1: Machine Learning](Part-1-Machine-Learning.ipynb) | Trains and compares three classifiers on a climate model dataset | Python, pandas, scikit-learn, Matplotlib, seaborn |
| [Part 2: Evolutionary Computation](Part-2-Evolutionary-Computation.ipynb) | A genetic algorithm that searches for the minimum of Himmelblau's function | Python, NumPy, Matplotlib |

## Part 1: Machine Learning

The notebook trains a Random Forest, a support vector classifier and a neural network (a multi-layer perceptron) to predict whether a climate model simulation run fails. Each model is checked with confusion matrices, precision, recall, F1 score and 10-fold cross-validation.

On the test set, the neural network scored a macro F1 of 0.80. The Random Forest and the support vector classifier both scored 0.48, because they predicted a successful run every time. Only 46 of the 540 runs in the dataset failed.

## Part 2: Evolutionary Computation

The notebook plots 500 random samples of Himmelblau's function and the three-hump camel function. It then runs a genetic algorithm with NumPy on Himmelblau's function, using a population of 300 over 600 generations. The best result scored 0.03, where 0 is the lowest possible, and the notebook plots how the best score improves.

## Run it

```
pip install -r requirements.txt
jupyter notebook
```

Open either notebook. `pop_failures.dat` needs to stay in the same folder as the notebooks.

## Dataset

`pop_failures.dat` is the [Climate Model Simulation Crashes](https://doi.org/10.24432/C5HG71) dataset from the UCI Machine Learning Repository, shared under the CC BY 4.0 license. It was created by D. Lucas, R. Klein, J. Tannahill, D. Ivanova, S. Brandon, D. Domyancic and Y. Zhang in 2013.
