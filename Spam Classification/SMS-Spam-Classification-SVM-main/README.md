# 📱 Spam Classification


<p align="center">
  <strong>Machine Learning • Natural Language Processing • Text Classification</strong>
</p>

<p align="center">
  <a href="#-overview">Overview</a> •
  <a href="#-workflow">Workflow</a> •
  <a href="#-technologies">Technologies</a> •
  <a href="#-model">Model</a> •
  <a href="#-evaluation">Evaluation</a> •
  <a href="#-installation">Installation</a>
</p>

---

## 📌 Overview

This project develops a machine learning model to automatically classify SMS messages as either **Spam** or **Ham (legitimate)**.

The project applies **Natural Language Processing (NLP)** techniques to transform raw SMS text into numerical features using **TF-IDF (Term Frequency–Inverse Document Frequency)** and then uses a **Linear Support Vector Machine (SVM)** classifier for prediction.

The complete workflow includes data preparation, exploratory data analysis, text preprocessing, feature extraction, model training, hyperparameter tuning, cross-validation, and performance evaluation.

---

## 🎯 Objectives

The main objectives of this project are to:

* Analyze the SMS Spam Collection dataset.
* Explore the distribution of Spam and Ham messages.
* Preprocess and clean textual SMS data.
* Convert text into numerical features using TF-IDF.
* Train a Linear Support Vector Machine classifier.
* Optimize model hyperparameters using GridSearchCV.
* Evaluate the model using multiple classification metrics.
* Build a model capable of predicting whether a new SMS is Spam or Ham.

---

## 📊 Dataset

The project uses the **SMS Spam Collection Dataset**.

**Dataset source:** Kaggle — SMS Spam Collection Dataset

The dataset contains SMS messages labeled as:

| Label  | Description                         |
| ------ | ----------------------------------- |
| `ham`  | Legitimate SMS message              |
| `spam` | Unwanted/promotional/fraudulent SMS |

### Dataset Summary

* **Total messages:** 5,572
* **Ham messages:** 4,825
* **Spam messages:** 747
* **Missing values:** 0
* **Duplicate records:** 403

The dataset contains two primary variables used in this project:

* `label` — target class
* `message` — SMS text

---

## 🔬 Machine Learning Workflow

```text
                    SMS Dataset
                         │
                         ▼
                Data Loading & Cleaning
                         │
                         ▼
                  Exploratory Analysis
                         │
                         ▼
                 Text Preprocessing
                         │
                         ▼
                  TF-IDF Vectorization
                         │
                         ▼
                  Train/Test Split
                         │
                         ▼
                Linear SVM Classifier
                         │
                         ▼
                 Hyperparameter Tuning
                         │
                         ▼
                  Cross-Validation
                         │
                         ▼
                Model Evaluation
                         │
                         ▼
                  Spam / Ham Prediction
```

---

## 🧹 Data Preprocessing

The text-processing workflow includes Natural Language Processing techniques such as:

* Lowercasing text
* Removing unwanted characters
* Removing stopwords
* Text normalization
* Lemmatization

The processed text is then converted into numerical features using TF-IDF.

---

## 🔢 Feature Engineering — TF-IDF

  ![Data Analysis]

**TF-IDF** is used to represent SMS messages numerically based on the importance of words within the dataset.

The vectorizer is configured to consider:

* Unigrams
* Bigrams
* Up to 5,000 features

This allows the model to capture both individual words and short word combinations that may be useful for distinguishing Spam from Ham messages.

---

## 🤖 Machine Learning Model

### Linear Support Vector Machine

The main classification algorithm used in this project is:

```text
LinearSVC
```

The model is combined with TF-IDF using a machine-learning pipeline:

```text
Raw SMS
   ↓
TF-IDF Vectorizer
   ↓
LinearSVC
   ↓
Prediction
```

### Hyperparameter Optimization

`GridSearchCV` is used to search for an appropriate value of the SVM `C` parameter.

The model is evaluated using **5-fold cross-validation** during hyperparameter tuning.

---

## 📈 Model Evaluation

The model evaluation includes:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-score**
* **Confusion Matrix**
* **Cross-validation score**

These metrics provide a more complete understanding of classification performance, particularly because the dataset contains substantially more Ham messages than Spam messages.

---

## 📸 Results / Visualizations


 
  





## 🛠️ Technologies

| Technology       | Purpose                     |
| ---------------- | --------------------------- |
| Python           | Programming language        |
| Pandas           | Data manipulation           |
| NumPy            | Numerical computing         |
| Matplotlib       | Data visualization          |
| Seaborn          | Statistical visualization   |
| NLTK             | Natural Language Processing |
| Scikit-learn     | Machine Learning            |
| WordCloud        | Text visualization          |
| Jupyter Notebook | Development environment     |
| Google Colab     | Notebook execution          |

---

## 📂 Project Structure

```text
SMS-Spam-Classification-SVM/
│
├── 📓 SMS_Spam_SVM.ipynb
├── 📄 README.md
├── 📄 requirements.txt
├── 📄 .gitignore
│
├── 📁 images/
│   ├── profile.jpg
│   ├── results.png
│   └── confusion_matrix.png
│
└── 📁 data/
    └── README.md
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/SMS-Spam-Classification-SVM.git
```

Move into the project directory:

```bash
cd SMS-Spam-Classification-SVM
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---

## ▶️ How to Run

### Option 1 — Jupyter Notebook

```bash
jupyter notebook SMS_Spam_SVM.ipynb
```

### Option 2 — Google Colab

Upload `SMS_Spam_SVM.ipynb` to Google Colab and run the notebook cells sequentially.

The dataset should be downloaded separately from the original source and supplied according to the notebook's data-loading instructions.

---

## 📚 Project Highlights

### 🔹 Natural Language Processing

Applied text preprocessing techniques to prepare raw SMS messages for machine learning.

### 🔹 Feature Extraction

Used TF-IDF with unigram and bigram features to transform text into numerical representations.

### 🔹 Machine Learning

Implemented a Linear Support Vector Machine for Spam/Ham classification.

### 🔹 Model Optimization

Used GridSearchCV with 5-fold cross-validation for hyperparameter optimization.

### 🔹 Performance Analysis

Evaluated the classifier using accuracy, precision, recall, F1-score, confusion matrix, and cross-validation.

---

## 🚀 Future Improvements

Potential improvements for this project include:

* Testing additional machine learning algorithms such as Logistic Regression and Naive Bayes.
* Comparing different NLP feature-extraction techniques.
* Performing more extensive hyperparameter optimization.
* Addressing class imbalance using appropriate techniques.
* Deploying the trained model as a web application.
* Building an API for real-time SMS classification.
* Experimenting with modern NLP/deep-learning models.

---

## 👨‍💻 About Me



<p align="center">
  <strong>Muntasir Ahammed</strong><br>
  Undergraduate Student | Information and Communication Technology in BUP<br>
  Interested in Data Science, Machine Learning & AI
</p>

### Connect With Me

#ahammednabil123@gmail.com

---

## 📜 License

This project is intended for educational and portfolio purposes.

Please refer to the original dataset source for the dataset's licensing and usage conditions.

---

<p align="center">
  ⭐ If you found this project useful, consider giving the repository a star!
</p>

<p align="center">
  <i>Built with Python,NLP & Machine Learning</i>
</p>
