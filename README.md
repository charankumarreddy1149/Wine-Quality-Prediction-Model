 Wine Quality Prediction Project

This project uses machine learning to predict the quality of red wine based on its chemical properties. The model is trained to classify a wine as either "good" or "bad" based on a few key characteristics, offering a simple and interactive way to test the predictive power of machine learning.

The unique aspect of this project is its focus on **instance selection**, a preprocessing technique that trains the model on a small, representative subset of the data to improve training efficiency.

 Goal

To build an interactive command-line tool that takes user-provided chemical properties of a red wine and predicts whether its quality is likely to be **"Good"** (score $\\geq 7$) or **"Bad"** (score $\< 7$).

How It Works

1.  **Data Loading**: The script downloads the Wine Quality dataset from the UCI Machine Learning Repository.
2.  **Instance Selection**: Instead of training on the entire dataset of over 1,500 rows, the project uses **K-Means clustering** to identify a small number of **"representative" rows** (cluster centroids). The model is then trained on this efficient, condensed dataset. This significantly reduces training time without a major loss in accuracy.
3.  **Model Training**: A **Random Forest Classifier** is trained on the selected representative data points.
4.  **Interactive Prediction**: The script prompts the user to enter 11 specific chemical properties. The trained model then uses this input to make a real-time prediction.

Prerequisites

  * Python 3.x
  * The following Python libraries:
      * `pandas`
      * `scikit-learn`
      * `numpy`

Installation

You can install the required libraries using `pip`:

```bash
pip install pandas scikit-learn numpy
```

Usage

1.  Save the provided Python code as `wine_predictor.py`.
2.  Run the script from your terminal:

<!-- end list -->

```bash
python wine_predictor.py
```

3.  Follow the on-screen prompts to enter the 11 chemical properties of the wine. The program will provide a prediction and ask if you'd like to make another.

## 🔬 The 11 Chemical Properties

The model requires the following inputs to make a prediction.

1.  `fixed acidity`
2.  `volatile acidity`
3.  `citric acid`
4.  `residual sugar`
5.  `chlorides`
6.  `free sulfur dioxide`
7.  `total sulfur dioxide`
8.  `density`
9.  `pH`
10. `sulphates`
11. `alcohol`

## 📊 Dataset

The project uses the **Wine Quality Dataset**, a publicly available dataset on the UCI Machine Learning Repository. It contains physicochemical data on red and white wines, with an associated quality score.

  * **Dataset Link**: `https://archive.ics.uci.edu/dataset/186/wine+quality`

## 🛡️ License

This project is open-source and available under the MIT License.
