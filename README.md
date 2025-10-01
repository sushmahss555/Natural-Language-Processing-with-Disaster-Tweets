# 🌀 Natural Language Processing with Disaster Tweets (RNN Model)

This project is part of the weekly mini-project assignment.  
We participate in the [Kaggle competition: Natural Language Processing with Disaster Tweets](https://www.kaggle.com/c/nlp-getting-started), where the goal is to classify tweets as either disaster-related (`1`) or not disaster-related (`0`).

---

## 📌 Project Overview
- **Problem:** Given short text tweets, predict whether the text is about a real disaster.  
- **Approach:** Preprocess text, convert tweets into sequences using tokenization, and train a **Recurrent Neural Network (RNN)** for binary classification.  
- **Deliverables:**
  1. Jupyter Notebook with code, analysis, and discussion.  
  2. GitHub repository (this repo).  
  3. Kaggle leaderboard screenshot with submission score.  

---

## 📊 Dataset
- **train.csv** – contains tweets and labels (`target` = 0 or 1).  
- **test.csv** – contains tweets (labels not provided).  
- **sample_submission.csv** – example format for Kaggle submission.  

**Dataset Structure (train.csv):**
- `id` – unique identifier for each tweet  
- `text` – the actual tweet content  
- `target` – 1 = disaster, 0 = not disaster  

---

## 🔍 Exploratory Data Analysis (EDA)
- Checked dataset shape, missing values, and class balance.  
- Visualized label distribution (`target=0` vs `target=1`).  
- Token length analysis (average ~15 words per tweet).  
- Basic text cleaning (lowercasing, tokenization, padding).  

---

## 🏗️ Model Architecture

Three models were built and compared for this project:

### 1. **Simple RNN**
- **Embedding Layer** – maps words to dense vectors.  
- **Simple RNN Layer** – processes sequences step-by-step.  
- **Dropout** – prevents overfitting.  
- **Dense Layers** – fully connected layers for classification.  
- **Output Layer** – sigmoid activation for binary classification.

### 2. **LSTM**
- **Embedding Layer** – maps words to dense vectors.  
- **LSTM Layer** – captures long-term dependencies in sequences.  
- **Dropout** – prevents overfitting.  
- **Dense Layers** – fully connected layers for classification.  
- **Output Layer** – sigmoid activation for binary classification.

### 3. **Bidirectional LSTM**
- **Embedding Layer** – maps words to dense vectors.  
- **Bidirectional LSTM Layer** – reads sequences in both forward and backward directions to capture more context.  
- **Dropout** – prevents overfitting.  
- **Dense Layers** – fully connected layers for classification.  
- **Output Layer** – sigmoid activation for binary classification.

> All three models were trained on the same tokenized and padded dataset to compare performance.

