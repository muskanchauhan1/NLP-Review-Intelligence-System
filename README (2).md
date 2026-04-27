# 🧠 NLP-Powered Business Review Intelligence System

![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=for-the-badge&logo=tensorflow)
![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?style=for-the-badge&logo=powerbi)
![Streamlit](https://img.shields.io/badge/Streamlit-Live%20App-red?style=for-the-badge&logo=streamlit)
![NLP](https://img.shields.io/badge/NLP-CNN%20%7C%20RNN%20%7C%20LDA%20%7C%20SVM-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

> **End-to-end NLP intelligence platform that automatically reads 393,000+ Amazon customer reviews, detects sentiment, predicts ratings, discovers hidden topics, and delivers business insights through a live web app and executive Power BI dashboard.**

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Live Demo](#-live-demo)
- [Architecture](#-architecture)
- [Screenshots](#-screenshots)
- [Tech Stack](#-tech-stack)
- [Models & Results](#-models--results)
- [Project Structure](#-project-structure)
- [How to Run](#-how-to-run)
- [Key Insights](#-key-insights)
- [Connect](#-connect)

---

## 🎯 Project Overview

A business receives thousands of customer reviews every day — nobody has time to read them all.

This system is the **machine that reads every single one**, understands feelings, finds hidden patterns, predicts star ratings, and hands a manager a clean dashboard report — **all automatically, zero humans needed.**

| What Goes In | What Comes Out |
|---|---|
| 393,579 raw Amazon reviews | Sentiment: Positive / Negative / Neutral |
| Unstructured messy text | Star rating prediction (1-5) |
| No labels, no manual work | 5 hidden topic clusters |
| One click | Live Power BI KPI dashboard |

---

## 🚀 Live Demo

> **Streamlit App** — Type any review → Get instant predictions from CNN, RNN, and SVM models simultaneously

<!-- ADD SCREENSHOT HERE -->
<!-- Replace the line below with your actual screenshot -->
<!-- ![Streamlit App](assets/screenshots/streamlit_demo.png) -->

```
📝 Input  : "This product is absolutely amazing, best purchase I ever made!"
😊 CNN    : Positive  (Confidence: 91.2%)
⭐ RNN    : 5 Stars
🎯 SVM    : Positive
```

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    RAW DATA INPUT                           │
│              Amazon Reviews CSV (393K rows)                 │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                  NLP PREPROCESSING                          │
│   Tokenization → Stopword Removal → Bigram/Trigram          │
│   TF-IDF → Padding → Sentiment Labelling                   │
└──────┬──────────────┬──────────────┬────────────────────────┘
       │              │              │
       ▼              ▼              ▼
┌──────────┐   ┌──────────┐   ┌──────────────────┐
│   CNN    │   │  LDA     │   │  RNN / LSTM      │
│Sentiment │   │  Topic   │   │  Rating          │
│83% Acc   │   │Modelling │   │  Predictor       │
│          │   │5 Topics  │   │  72% Acc         │
└──────────┘   └──────────┘   └──────────────────┘
       │                              │
       └──────────────┬───────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│             Word2Vec Embeddings + SVM Classifier            │
│          100-dim vectors · 80K vocab · LinearSVC            │
└──────────────────────┬──────────────────────────────────────┘
                       │
          ┌────────────┴────────────┐
          ▼                         ▼
┌──────────────────┐     ┌──────────────────────┐
│  Streamlit App   │     │   Power BI Dashboard  │
│  Live Predictions│     │   7 KPI Visuals       │
└──────────────────┘     └──────────────────────┘
```

---

## 📸 Screenshots

### 🔵 Streamlit Live App
<!-- ADD YOUR STREAMLIT SCREENSHOT HERE -->
<!-- 1. Take a screenshot of your Streamlit app with a prediction result -->
<!-- 2. Save it as: assets/screenshots/streamlit_app.png -->
<!-- 3. Uncomment the line below -->
<!-- ![Streamlit App](assets/screenshots/streamlit_app.png) -->

---

### 🟣 Power BI Dashboard
<!-- ADD YOUR POWER BI DASHBOARD SCREENSHOT HERE -->
<!-- 1. Take a screenshot of your full Power BI dashboard -->
<!-- 2. Save it as: assets/screenshots/powerbi_dashboard.png -->
<!-- 3. Uncomment the line below -->
<!-- ![Power BI Dashboard](assets/screenshots/powerbi_dashboard.png) -->

---

### 🟢 CNN Training Results
<!-- ADD YOUR COLAB CNN TRAINING OUTPUT SCREENSHOT HERE -->
<!-- 1. Screenshot the cell showing epoch accuracy results -->
<!-- 2. Save it as: assets/screenshots/cnn_training.png -->
<!-- 3. Uncomment the line below -->
<!-- ![CNN Training](assets/screenshots/cnn_training.png) -->

---

### 🟡 RNN Training Results
<!-- ADD YOUR COLAB RNN TRAINING OUTPUT SCREENSHOT HERE -->
<!-- 1. Screenshot the cell showing RNN epoch results -->
<!-- 2. Save it as: assets/screenshots/rnn_training.png -->
<!-- 3. Uncomment the line below -->
<!-- ![RNN Training](assets/screenshots/rnn_training.png) -->

---

### 🟠 Topic Modelling Output (LDA)
<!-- ADD YOUR LDA TOPICS SCREENSHOT HERE -->
<!-- 1. Screenshot the cell showing Top 5 Topics discovered -->
<!-- 2. Save it as: assets/screenshots/lda_topics.png -->
<!-- 3. Uncomment the line below -->
<!-- ![LDA Topics](assets/screenshots/lda_topics.png) -->

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| **Language** | Python 3.10 |
| **NLP** | NLTK · Gensim · Bigram/Trigram · TF-IDF |
| **Deep Learning** | TensorFlow · Keras · CNN (Conv1D) · Bidirectional LSTM |
| **Classical ML** | Scikit-learn · LinearSVC (SVM) · Word2Vec |
| **Topic Modelling** | Gensim LDA · LdaMulticore |
| **Embeddings** | Word2Vec (100-dim · 80K vocab) |
| **Visualisation** | Power BI · Streamlit · Matplotlib · Seaborn |
| **Deployment** | Streamlit · ngrok · Google Colab T4 GPU |
| **Storage** | Google Drive · Pickle · HDF5 |
| **Data** | Amazon Fine Food Reviews (Kaggle) |

---

## 📊 Models & Results

### Model 1 — CNN Sentiment Classifier

| Parameter | Value |
|---|---|
| Architecture | Embedding(20K, 128) → Conv1D(128, size=5) → GlobalMaxPooling → Dense(64) → Dropout(0.3) → Softmax(3) |
| Training data | 80,000 reviews |
| Epochs | 5 |
| Test accuracy | **83.12%** |
| Classes | Positive · Negative · Neutral |

---

### Model 2 — Bidirectional LSTM Rating Predictor

| Parameter | Value |
|---|---|
| Architecture | Embedding → BiLSTM(64) → BiLSTM(32) → Dense(64) → Dropout(0.3) → Softmax(5) |
| Training data | 80,000 reviews |
| Epochs | 5 (EarlyStopping) |
| Test accuracy | **72.61%** |
| Output | 1–5 star rating from text alone |

---

### Model 3 — LDA Topic Modelling

| Parameter | Value |
|---|---|
| Algorithm | LdaMulticore |
| Topics | 5 hidden clusters |
| Training data | 50,000 reviews |
| Passes | 5 |
| Features | Bigram + Trigram + BoW corpus |

---

### Model 4 — Word2Vec + SVM

| Parameter | Value |
|---|---|
| Embeddings | Word2Vec (vector_size=100, window=5) |
| Vocabulary | 80,000+ words |
| Classifier | LinearSVC |
| Input | Mean of word vectors per review |

---

## 📁 Project Structure

```
NLP-Review-Intelligence-System/
│
├── 📓 NLP_Review_Intelligence.ipynb   ← Main Colab notebook
│
├── 🐍 app.py                          ← Streamlit web app
│
├── 📊 assets/
│   └── screenshots/
│       ├── streamlit_app.png          ← ADD: Streamlit demo screenshot
│       ├── powerbi_dashboard.png      ← ADD: Power BI dashboard screenshot
│       ├── cnn_training.png           ← ADD: CNN training output screenshot
│       ├── rnn_training.png           ← ADD: RNN training output screenshot
│       └── lda_topics.png             ← ADD: LDA topics output screenshot
│
├── 📄 requirements.txt                ← Python dependencies
│
└── 📄 README.md                       ← This file
```

---

## ⚙️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/muskanchauhan1/NLP-Review-Intelligence-System.git
cd NLP-Review-Intelligence-System
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Download dataset
- Go to: https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews
- Download `Reviews.csv`
- Place it in the project root folder

### 4. Run the full notebook
- Open `NLP_Review_Intelligence.ipynb` in Google Colab
- Enable T4 GPU: `Runtime → Change runtime type → T4 GPU`
- Run all cells in order

### 5. Launch Streamlit app
```bash
streamlit run app.py
```

---

## 💡 Key Insights

From analysing 393,579 Amazon reviews:

| Insight | Value |
|---|---|
| 😊 Positive reviews | **77.94%** (306,760 reviews) |
| 😡 Negative reviews | **14.50%** (57,070 reviews) |
| 😐 Neutral reviews | **7.56%** (29,750 reviews) |
| ⭐ Average star rating | **4.18 / 5** |
| 📦 Dominant rating | **5 stars** (most common) |
| 🔍 Topics discovered | **5 business themes** |

### Business Impact
> Demonstrated how NLP automation replaces manual review analysis for 393K records — reducing analyst review time by **~95%** while delivering multi-dimensional intelligence (sentiment + rating + topic) simultaneously.

---

## 📋 Requirements

```
tensorflow>=2.12
keras
scikit-learn
gensim
nltk
pandas
numpy
streamlit
matplotlib
seaborn
pyngrok
```

---

## 🔗 Connect

| Platform | Link |
|---|---|
| 💼 LinkedIn | [muskanchauhan6065](https://linkedin.com/in/muskanchauhan6065/) |
| 🐙 GitHub | [muskanchauhan1](https://github.com/muskanchauhan1) |
| 📧 Email | muskanchauhan6065@gmail.com |

---

<div align="center">

**⭐ If this project helped you, please give it a star!**

*Built with ❤️ by Muskan Chauhan — CDAC 2025*

</div>
