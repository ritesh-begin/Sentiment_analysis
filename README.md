# Sentiment Analysis using Logistic Regression

This project demonstrates how to build a sentiment analysis model that classifies customer reviews into **positive** and **negative** categories using machine learning.

---

## 📂 Project Structure

- `Sentiment_analysis_Logistic.ipynb`  
  Jupyter notebook containing the full workflow: preprocessing, feature extraction, model training, and evaluation.

- `TestReviews.csv`  
  Test dataset with sample reviews and sentiment labels.

- `TrainingDataPositive.txt` / `TrainingDataNegative.txt`  
  Training data files containing positive and negative reviews used to build the model.

---

## ⚙️ Workflow

1. **Data Preparation**
   - Load training data from text files.
   - Assign labels:  
     - `1` → Positive  
     - `0` → Negative  

2. **Preprocessing**
   - Convert text to lowercase  
   - Remove special characters and numbers  
   - Remove stopwords (keeping negations like *not*)  
   - Apply stemming  

3. **Feature Extraction**
   - Transform reviews into numerical vectors using **TF-IDF** or **CountVectorizer**.  

4. **Model Training**
   - Use **Logistic Regression** to classify reviews.  
   - Balanced class weights to handle uneven data distribution.  

5. **Evaluation**
   - Tested on `TestReviews.csv`.  
   - Metrics used: Accuracy, Confusion Matrix, Precision, Recall, F1-score.  

---

## 📊 Example Results

- **Accuracy:** ~85–90% (depending on parameter tuning)  
- The model correctly identifies positive and negative reviews with good balance.  

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/sentiment-analysis-logistic.git
   cd sentiment-analysis-logistic

