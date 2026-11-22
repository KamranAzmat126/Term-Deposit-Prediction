# Term Deposit Subscription Prediction

A machine learning project that predicts whether a bank customer will subscribe to a term deposit following a direct marketing campaign.

## Project Overview

Banks use direct marketing campaigns to promote financial products such as term deposits. Contacting every customer can be costly, so identifying customers who are more likely to subscribe can help improve campaign efficiency.

This project applies classification algorithms to historical bank marketing data to predict the likelihood of a customer subscribing to a term deposit.

## Dataset

The project uses the Bank Marketing dataset.

- **Source:** [Bank Marketing Dataset – Kaggle](https://www.kaggle.com/datasets/ruthgn/bank-marketing-data-set)
- **Dataset size:** 41,188 records
- **Features:** 20 input variables
- **Target variable:** `y`
- **Prediction classes:** `yes` or `no`

The dataset contains customer information, campaign-related details and economic indicators.

The dataset is not included in this repository. Download it from Kaggle before running the notebook.

## Project Workflow

1. **Data exploration:** Examining the dataset, distributions and relationships between variables.
2. **Data preprocessing:** Preparing numerical and categorical features for machine learning.
3. **Feature transformation:** Applying `StandardScaler` to numerical features and `OneHotEncoder` to categorical features.
4. **Model development:** Training Logistic Regression and Random Forest classifiers.
5. **Hyperparameter tuning:** Applying GridSearchCV with five-fold cross-validation.
6. **Model evaluation:** Comparing performance using accuracy, precision, recall, F1-score and ROC-AUC.
7. **Interpretability:** Examining feature importance and discussing the business implications of the results.

## Machine Learning Models

The project evaluates two classification algorithms:

- Logistic Regression
- Random Forest Classifier

Both models use class weighting to help address the imbalance between subscription and non-subscription outcomes.

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

## Model Results

The following results are taken from the notebook's recorded test-set outputs.

| Model               | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---------------------|---------:|----------:|-------:|---------:|--------:|
| Logistic Regression | 0.83     | 0.36      | 0.65   | 0.47     | 0.80    |
| Tuned Random Forest | 0.86     | 0.42      | 0.62   | 0.50     | 0.81    |

The tuned Random Forest achieved the strongest F1-score and ROC-AUC among these results. Logistic Regression achieved slightly higher recall, identifying a larger proportion of customers who subscribed.

These results illustrate the trade-off between identifying potential subscribers and avoiding unnecessary marketing contacts.

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- Machine Learning
- Classification
- Data Preprocessing
- Model Evaluation

## How to Run the Project

### 1. Clone the repository

git clone https://github.com/KamranAzmat126/Term-Deposit-Prediction.git
cd Term-Deposit-Prediction

### Step 2: Install dependencies

pip install pandas matplotlib scikit-learn jupyter

### Step 3: Download the dataset

Download the CSV dataset from Kaggle using the link above.

### Step 4: Update the dataset path

The notebook currently contains a local Windows file path. Replace the existing dataset path in the notebook with the relative path.

### Step 5: Launch Jupyter Notebook

jupyter notebook

Open `Term_Deposit_Prediction.ipynb` and run the notebook cells.

