# Solar Flare Prediction with Decision Trees

This project applies machine learning to solar flare data in order to predict flare-related outcomes from structured observational features. The notebook loads solar flare data from an ARFF file, prepares feature and target values, and evaluates a decision tree classifier using repeated 10-fold cross-validation.

## Project Overview

The goal of this project is to explore whether structured measurements of solar active regions can be used to predict future flare activity. The dataset contains observations of sunspot and region characteristics, along with flare-related target outputs.

This notebook uses a decision tree classifier and evaluates its performance with repeated cross-validation.

## What the Code Does

The notebook performs the following steps:

1. Loads the solar flare dataset from an ARFF file
2. Converts the data into a Pandas DataFrame
3. Extracts feature values and target values
4. Builds a decision tree classifier
5. Evaluates the classifier using 10-fold cross-validation
6. Repeats the cross-validation process multiple times and reports:
   - average accuracy
   - average standard deviation across runs

## Dataset

The dataset contains observations from active regions on the Sun.

Input features include properties such as:
- modified Zurich class
- largest spot size
- spot distribution
- activity
- evolution
- previous flare activity
- complexity indicators
- area-related measurements

The flare-related outputs describe future flare production by the region.

## Methods Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Decision Tree Classification
- 10-fold Cross-Validation

## Model

The notebook uses:

- `DecisionTreeClassifier(max_depth=2)`

This keeps the model relatively simple and interpretable while testing whether the solar-region features contain useful predictive information.

## Evaluation

Model performance is measured using repeated 10-fold cross-validation with accuracy as the scoring metric.

The notebook reports:
- mean accuracy across runs
- average standard deviation across runs

This provides a more stable estimate of model performance than relying on a single train/test split.

## Repository Contents

- `solar_flare_prediction.ipynb` — main notebook containing the model workflow
- `solar_flare_data.arff` — dataset used for training and evaluation

## Notes

This project was completed as part of a machine learning course and is being presented here as a portfolio example of:
- structured data analysis
- scientific machine learning
- classification workflows
- cross-validation and model evaluation

## Possible Improvements

Some natural next steps for this project would be:

- compare the decision tree against other classifiers such as random forests, SVMs, or neural networks
- perform more detailed feature preprocessing and encoding
- evaluate additional metrics beyond accuracy
- add visualizations of the tree and feature importance
- cleanly separate preprocessing, training, and evaluation into reusable functions

## How to Run

1. Clone the repository
2. Make sure the dataset file is in the same folder as the notebook
3. Install the required Python packages
4. Open the notebook and run all cells

Example package installation:

```bash
pip install numpy pandas scipy scikit-learn matplotlib
