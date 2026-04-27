<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=1A3A5C&height=200&section=header&text=NLP%20Review%20Intelligence%20System&fontSize=36&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=End-to-End%20NLP%20Pipeline%20%7C%20CNN%20%C2%B7%20RNN%20%C2%B7%20LDA%20%C2%B7%20SVM%20%C2%B7%20Power%20BI%20%C2%B7%20Streamlit&descAlignY=55&descSize=16&descColor=D6EAF8"/>

<br/>

[![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://tensorflow.org)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com)
[![Streamlit](https://img.shields.io/badge/Streamlit-Live%20App-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io)
[![NLP](https://img.shields.io/badge/NLP-CNN%20%7C%20RNN%20%7C%20LDA%20%7C%20SVM-27AE60?style=for-the-badge&logo=google&logoColor=white)]()
[![Status](https://img.shields.io/badge/Status-✅%20Complete-brightgreen?style=for-the-badge)]()
[![Dataset](https://img.shields.io/badge/Dataset-393K%20Reviews-8E44AD?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews)

<br/>

> ### 🧠 *"A machine that reads 393,000 customer reviews, understands feelings, finds hidden patterns, predicts star ratings — and hands a manager a clean dashboard. All automatically. Zero humans needed."*

<br/>

[![GitHub stars](https://img.shields.io/github/stars/muskanchauhan1/NLP-Review-Intelligence-System?style=social)](https://github.com/muskanchauhan1/NLP-Review-Intelligence-System/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/muskanchauhan1/NLP-Review-Intelligence-System?style=social)](https://github.com/muskanchauhan1/NLP-Review-Intelligence-System/network)

</div>

---

## 📌 Table of Contents

| # | Section |
|---|---|
| 1 | [🎯 Project Overview](#-project-overview) |
| 2 | [📸 Live Screenshots](#-live-screenshots) |
| 3 | [🏗️ Architecture](#-architecture) |
| 4 | [📊 Models & Results](#-models--results) |
| 5 | [🛠️ Tech Stack](#-tech-stack) |
| 6 | [💡 Key Business Insights](#-key-business-insights) |
| 7 | [📁 Project Structure](#-project-structure) |
| 8 | [⚙️ How to Run](#-how-to-run) |
| 9 | [🔗 Connect](#-connect) |

---

## 🎯 Project Overview

<table>
<tr>
<td width="50%">

### The Problem
A business receives **thousands of customer reviews every day.**

Nobody has time to read them all. Manual analysis takes hours and misses patterns hidden across hundreds of thousands of records.

</td>
<td width="50%">

### The Solution
An **end-to-end NLP intelligence system** that:
- 📖 Reads all 393,579 reviews automatically
- 😊 Detects sentiment (CNN — 83% accuracy)
- ⭐ Predicts star ratings (RNN — 72% accuracy)
- 🔍 Finds 5 hidden business themes (LDA)
- 📊 Delivers live Power BI KPI dashboard

</td>
</tr>
</table>

<div align="center">

| Input | Process | Output |
|---|---|---|
| 393,579 raw Amazon reviews | CNN · RNN · LDA · SVM · Word2Vec | Sentiment + Rating + Topics |
| Unstructured messy text | Bigram/Trigram · TF-IDF · Embeddings | Power BI Dashboard |
| No labels · No manual work | End-to-end automated pipeline | Live Streamlit web app |

</div>

---

## 📸 Live Screenshots

### 🟣 Power BI Executive Dashboard
> *7 live KPI visuals — 393K reviews analysed, 77.94% positive sentiment, 4.18 avg rating*

![Power BI Dashboard](assets/screenshots/powerbi_dashboard.png)

<div align="center">

*Built with: Donut Chart · Stacked Bar · KPI Cards · Topic Cluster · Star Rating Distribution · Sample Reviews Table*

</div>

---

### 🔴 Streamlit Live Prediction App
> *Type any review → Instant predictions from CNN, RNN, and SVM simultaneously*

![Streamlit App](assets/screenshots/streamlit_app.png)

<div align="center">

```
📝 Input   : "this product is very amazing but i broke while i used it"
😊 CNN     : Positive   (Confidence: 48.5%)
⭐ RNN     : 5 Stars    (Predicted: 5 out of 5)
🎯 SVM     : Positive   (Support Vector Machine)
🧹 Cleaned : product amazing broke used
```

</div>

---

## 🏗️ Architecture

```
╔══════════════════════════════════════════════════════════════╗
║              RAW DATA — Amazon Reviews CSV                   ║
║                    393,579 records                           ║
╚══════════════════════════╦═══════════════════════════════════╝
                           ║
                           ▼
╔══════════════════════════════════════════════════════════════╗
║                   NLP PREPROCESSING                          ║
║  Lowercase → Remove HTML → Tokenize → Remove Stopwords      ║
║  Bigram/Trigram Extraction → TF-IDF → Padding → Labels      ║
╚══════╦══════════════════╦══════════════════╦════════════════╝
       ║                  ║                  ║
       ▼                  ▼                  ▼
╔═════════════╗   ╔══════════════╗   ╔══════════════════╗
║    CNN      ║   ║     LDA      ║   ║  Bidirectional   ║
║  Sentiment  ║   ║   Topic      ║   ║  LSTM Rating     ║
║  Classifier ║   ║  Modelling   ║   ║  Predictor       ║
║  83% Acc ✅ ║   ║  5 Topics ✅ ║   ║  72% Acc ✅      ║
╚═════════════╝   ╚══════════════╝   ╚══════════════════╝
       ║                                      ║
       ╚══════════════╦═══════════════════════╝
                      ║
                      ▼
╔══════════════════════════════════════════════════════════════╗
║           Word2Vec Embeddings + LinearSVM Classifier         ║
║           100-dim vectors · 80K+ vocab · Semantic NLP        ║
╚══════════════════════╦═══════════════════════════════════════╝
                       ║
          ╔════════════╩════════════╗
          ║                         ║
          ▼                         ▼
╔══════════════════╗     ╔═══════════════════════╗
║  Streamlit App   ║     ║  Power BI Dashboard   ║
║  Live Predictions║     ║  7 KPI Visuals        ║
║  CNN+RNN+SVM     ║     ║  Business Insights    ║
╚══════════════════╝     ╚═══════════════════════╝
```

---

## 📊 Models & Results

<div align="center">

### 🏆 Performance Summary

| Model | Task | Architecture | Accuracy |
|---|---|---|---|
| **CNN** | Sentiment Classification | Embedding → Conv1D(128) → GlobalMaxPooling → Dense → Dropout → Softmax(3) | **83.12%** ✅ |
| **Bidirectional LSTM** | Rating Prediction | Embedding → BiLSTM(64) → BiLSTM(32) → Dense → Dropout → Softmax(5) | **72.61%** ✅ |
| **LDA** | Topic Modelling | LdaMulticore · 5 topics · 5 passes · Bigram/Trigram features | **5 themes** ✅ |
| **Word2Vec + SVM** | Sentiment Classification | 100-dim embeddings · 80K vocab · LinearSVC | **Semantic** ✅ |

</div>

---

### Model 1 — CNN Sentiment Classifier

```
Input Text (100 tokens)
       ↓
Embedding Layer (20,000 words → 128 dimensions)
       ↓
Conv1D (128 filters, kernel size=5) — finds local word patterns
       ↓
GlobalMaxPooling1D — picks strongest signal per filter
       ↓
Dense(64, relu) → Dropout(0.3) → Softmax(3)
       ↓
Output: Positive | Negative | Neutral
```

**Training:** 5 epochs · 80K reviews · T4 GPU · **Test Accuracy: 83.12%**

---

### Model 2 — Bidirectional LSTM Rating Predictor

```
Input Text (100 tokens)
       ↓
Embedding Layer (128 dimensions)
       ↓
Bidirectional LSTM(64) — reads forward AND backward
       ↓
Bidirectional LSTM(32) — deeper sequential understanding
       ↓
Dense(64, relu) → Dropout(0.3) → Softmax(5)
       ↓
Output: 1 ⭐ | 2 ⭐⭐ | 3 ⭐⭐⭐ | 4 ⭐⭐⭐⭐ | 5 ⭐⭐⭐⭐⭐
```

**Training:** 5 epochs · EarlyStopping · **Test Accuracy: 72.61%**

---

### Model 3 — LDA Topic Modelling

```
Cleaned Reviews → Tokenized Lists
       ↓
Dictionary (vocab map) + Bigram/Trigram features
       ↓
Bag-of-Words corpus (50K reviews)
       ↓
LdaMulticore (5 topics · 5 passes · 2 workers)
       ↓
Each review → Dominant topic assigned
```

**Discovered themes:** Product Quality · Delivery · Taste/Flavour · Value for Money · Customer Service

---

### Model 4 — Word2Vec + LinearSVM

```
Cleaned Reviews → Split into word tokens
       ↓
Word2Vec (vector_size=100, window=5, min_count=2)
       ↓
Each review = mean of all word vectors → 100-dim vector
       ↓
LinearSVC classifier
       ↓
Output: Positive | Negative | Neutral
```

**Insight:** "terrible" and "awful" land close on the vector map — SVM understands semantic similarity

---

## 🛠️ Tech Stack

<div align="center">

| Category | Technologies |
|---|---|
| **Language** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) |
| **NLP** | NLTK · Gensim · Bigram · Trigram · TF-IDF · Word2Vec |
| **Deep Learning** | ![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white) · Keras · CNN (Conv1D) · Bidirectional LSTM |
| **Classical ML** | Scikit-learn · LinearSVC · SVM · K-Means |
| **Topic Model** | Gensim LDA · LdaMulticore |
| **BI & Viz** | ![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=flat&logo=powerbi&logoColor=black) · Streamlit · Matplotlib · Seaborn |
| **Deployment** | Streamlit · ngrok · Google Colab T4 GPU |
| **Storage** | Google Drive · Pickle · HDF5 (.h5) |
| **Data** | Amazon Fine Food Reviews (Kaggle · 568K records) |

</div>

---

## 💡 Key Business Insights

<div align="center">

```
╔═══════════════════════════════════════════════════════════╗
║              DASHBOARD INSIGHTS AT A GLANCE               ║
╠═══════════════════╦═══════════════════════════════════════╣
║  Total Reviews    ║  393,579                              ║
║  😊 Positive      ║  77.94%  (306,760 reviews)            ║
║  😡 Negative      ║  14.50%  ( 57,070 reviews)            ║
║  😐 Neutral       ║   7.56%  ( 29,750 reviews)            ║
║  ⭐ Avg Rating    ║  4.18 / 5                             ║
║  📦 Top Rating    ║  5 Stars (dominant — 300K+ reviews)   ║
║  🔍 Topics Found  ║  5 hidden business themes             ║
╚═══════════════════╩═══════════════════════════════════════╝
```

### 🚀 Business Impact

> Replacing manual review analysis for 393K records — reducing analyst review time by **~95%** while delivering **multi-dimensional customer intelligence** (sentiment + rating + topic) simultaneously in **under 3 seconds per query.**

</div>

---

## 📁 Project Structure

```
📦 NLP-Review-Intelligence-System/
│
├── 📓 NLP_Review_Intelligence.ipynb    ← Main Google Colab notebook
│   ├── Stage 1: Data Loading & EDA
│   ├── Stage 2: NLP Preprocessing
│   ├── Stage 3: CNN Sentiment Model
│   ├── Stage 4: LDA Topic Modelling
│   ├── Stage 5: RNN Rating Predictor
│   └── Stage 6: Word2Vec + SVM
│
├── 🐍 app.py                           ← Streamlit web application
│
├── 📊 assets/
│   └── screenshots/
│       ├── powerbi_dashboard.png       ← Power BI dashboard
│       └── streamlit_app.png           ← Live Streamlit demo
│
├── 📄 requirements.txt                 ← Python dependencies
│
└── 📄 README.md                        ← You are here!
```

---

## ⚙️ How to Run

### Step 1 — Clone the repository
```bash
git clone https://github.com/muskanchauhan1/NLP-Review-Intelligence-System.git
cd NLP-Review-Intelligence-System
```

### Step 2 — Install dependencies
```bash
pip install -r requirements.txt
```

### Step 3 — Download dataset
```
1. Go to: https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews
2. Download Reviews.csv
3. Upload to Google Drive
```

### Step 4 — Run the notebook
```
1. Open NLP_Review_Intelligence.ipynb in Google Colab
2. Runtime → Change runtime type → T4 GPU
3. Mount Google Drive
4. Run all cells in order (takes ~30 mins first time)
```

### Step 5 — Launch Streamlit app
```bash
pip install streamlit pyngrok
streamlit run app.py
```

### Requirements
```
tensorflow>=2.12
keras
scikit-learn
gensim
nltk
pandas
numpy
streamlit
pyngrok
matplotlib
seaborn
```

---

## 🔗 Connect

<div align="center">

| | |
|---|---|
| 💼 **LinkedIn** | [linkedin.com/in/muskanchauhan6065](https://linkedin.com/in/muskanchauhan6065/) |
| 🐙 **GitHub** | [github.com/muskanchauhan1](https://github.com/muskanchauhan1) |
| 📧 **Email** | muskanchauhan6065@gmail.com |

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=waving&color=1A3A5C&height=120&section=footer&text=Built%20with%20❤️%20by%20Muskan%20Chauhan%20%7C%20CDAC%202025&fontSize=16&fontColor=D6EAF8&animation=fadeIn"/>

**⭐ If this project helped you, please give it a star!**

</div>
