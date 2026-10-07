# Sentiment Analysis using Machine Learning

## 📌 Project Overview

This project is part of my **OIBSIP Data Analytics Internship**.

The main objective of this project is to build a **Sentiment Analysis model** that classifies text into three categories:

* 😊 Positive
* 😐 Neutral
* 😞 Negative

The project uses Natural Language Processing (NLP) techniques and machine learning algorithms to analyze text and predict its sentiment.

## 🎯 Objectives

* Load and explore a sentiment dataset
* Analyze the distribution of positive, negative, and neutral sentiments
* Clean and preprocess text data
* Convert text into numerical features using **TF-IDF**
* Train machine learning models
* Compare model performance
* Analyze incorrect predictions
* Test the model on new sentences

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Scikit-learn
* Matplotlib
* Seaborn
* WordCloud
* Google Colab / Jupyter Notebook

## 📂 Dataset

The dataset contains text sentences along with their corresponding sentiment labels.

### Columns

| Column      | Description                    |
| ----------- | ------------------------------ |
| `text`      | Text or sentence to analyze    |
| `sentiment` | Positive, Negative, or Neutral |

The dataset used in this project contains **60 samples**, with 20 samples for each sentiment class.

## 🔄 Project Workflow

### 1. Data Loading

The dataset is loaded using Pandas and inspected for:

* Number of rows and columns
* Data types
* Missing values
* Sentiment distribution

### 2. Text Preprocessing

The text data is cleaned using:

* Lowercase conversion
* Punctuation removal
* Number removal
* Stopword removal
* Lemmatization

### 3. TF-IDF

**TF-IDF (Term Frequency-Inverse Document Frequency)** is used to convert text into numerical features that machine learning models can understand.

### 4. Train-Test Split

The dataset is divided into:

* **80% Training data**
* **20% Testing data**

### 5. Machine Learning Models

Two classification algorithms are used:

1. **Multinomial Naive Bayes**
2. **Logistic Regression**

### 6. Model Evaluation

The models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

### 7. Visualization

The project includes:

* Sentiment distribution chart
* Model performance comparison
* Confusion matrices
* Positive sentiment WordCloud
* Negative sentiment WordCloud
* Neutral sentiment WordCloud

### 8. Error Analysis

Five misclassified examples are examined to understand why the models made incorrect predictions.

## 📊 Results

The performance of Naive Bayes and Logistic Regression is compared using accuracy, precision, recall, and F1-score.

The model with the better evaluation performance can be selected as the preferred model for this dataset.

> **Note:** The dataset contains only 60 samples, so the model results may vary significantly with different train-test splits. A larger dataset would provide more reliable results.

## 💡 Applications

Sentiment analysis can be used in:

* Customer review analysis
* Product feedback
* Social media monitoring
* Survey analysis
* Brand reputation monitoring
* Customer service
* Public opinion analysis

## 📁 Project Structure

```text
Sentiment-Analysis/
│
├── sentiment_analysis.ipynb
├── sentiment_analysis_dataset.csv
└── README.md
```

## ▶️ How to Run

1. Open the notebook in **Google Colab**.
2. Upload `sentiment_analysis_dataset.csv`.
3. Run the code cells from top to bottom.
4. View the graphs and model evaluation results.
5. Test the model with your own sentences.

## 📝 Conclusion

This project demonstrates how Natural Language Processing and machine learning can be used to classify text into positive, negative, and neutral sentiments.

TF-IDF was used for feature extraction, while Naive Bayes and Logistic Regression were used for classification. The project also includes visualization, model comparison, and error analysis.

Overall, sentiment analysis is a useful technique for extracting meaningful insights from large amounts of text data.

## 👩‍💻 Author

**Antra Raj**

Data Analytics Intern — **Oasis Infobyte (OIBSIP)**
