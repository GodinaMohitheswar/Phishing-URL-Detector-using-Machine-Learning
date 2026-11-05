# Phishing URL Detector Using Machine Learning

## Overview

Phishing attacks are a common cybersecurity threat in which attackers use fraudulent URLs to trick users into visiting malicious websites and revealing sensitive information.

This project implements a Machine Learning-based Phishing URL Detection system using the Random Forest Classifier. It analyzes selected URL-related features and predicts whether a given URL is potentially phishing or legitimate.

## Objectives

- Detect potentially malicious phishing URLs.
- Apply machine learning techniques to cybersecurity.
- Analyze URL characteristics to identify suspicious patterns.
- Demonstrate the use of Random Forest classification for phishing detection.

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Jupyter Notebook
- Machine Learning

## Machine Learning Algorithm

**Random Forest Classifier**

Random Forest is an ensemble learning algorithm that combines multiple decision trees to perform classification.

In this project, the classifier is trained using selected URL features to distinguish phishing URLs from legitimate URLs.

## Dataset and Features

The project uses a dataset named `dataset_phishing.csv`.

The following 12 features are selected for model training:

1. length_url
2. length_hostname
3. nb_dots
4. nb_hyphens
5. nb_at
6. nb_qm
7. nb_and
8. nb_or
9. ip
10. web_traffic
11. google_index
12. page_rank

The target column is `status`, which identifies URLs as phishing or legitimate.

## Project Workflow

1. Load the phishing URL dataset using Pandas.
2. Remove missing values.
3. Convert the target labels into numerical values.
4. Select relevant URL features.
5. Split the dataset into training and testing sets (70:30).
6. Train the Random Forest Classifier.
7. Evaluate the model using accuracy and classification metrics.
8. Accept URL input and generate a phishing or legitimate prediction.

## Model Performance

The notebook reports the following evaluation result:

| Metric | Result |
|---|---:|
| Accuracy | 94.37% |
| Precision (macro average) | 0.94 |
| Recall (macro average) | 0.94 |
| F1-score (macro average) | 0.94 |

*Note: These are the reported test-set results from the notebook. They should not be interpreted as guaranteed real-world detection performance.*

## Sample Predictions

**Example 1:**

Input:
`https://www.google.com`

Output:
`Legitimate`

**Example 2:**

Input:
`http://secure-login-update.com`

Output:
`Phishing`

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/GodinaMohitheswar/Phishing-URL-Detector-using-Machine-Learning.git
```

### 2. Navigate to the project directory

```bash
cd Phishing-URL-Detector-using-Machine-Learning
```

### 3. Install the required libraries

```bash
pip install pandas scikit-learn jupyter
```

### 4. Prepare the dataset

Place `dataset_phishing.csv` in the location expected by the notebook. If running outside Google Colab, update the dataset file path accordingly.

### 5. Run the Jupyter Notebook

```bash
jupyter notebook
```

Open the notebook:

`Phishing URL Detector using Machine Learning.ipynb`

Run the notebook cells to train the model and test URL predictions.

## Future Improvements

- Improve URL feature extraction for real-world URLs.
- Replace placeholder features with actual feature extraction.
- Improve prediction consistency between training and inference.
- Evaluate the model on independent datasets.
- Explore additional machine learning algorithms.
- Develop a web-based interface for URL detection.
