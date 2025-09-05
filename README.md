# Sentiment Analysis using Logistic Regression

This project demonstrates how to build a sentiment analysis model that classifies customer reviews into **positive** and **negative** categories using machine learning.

##<img width="512" height="512" alt="image" src="https://github.com/user-attachments/assets/4cfda26f-077a-4fa5-a6d8-9dcfd8a68018" /> Summary 
  Firstly,the data is loaded in **mdata** and then the preprocessing applies. In preprocessig we use **corpus** array to hold all the filtered words from the reviews column.
  
  This filtered words are obtained from **re** module to clear out all the special characters and symbols , then we convert it to lower and split it.
  
  The most important part is  _Feature-Scaling_ using **TF-IDF** which enhance the ability of the model to distinguish b/w positive and negative sentiment . Then the                  **LogisticRegression model** is trained .

  Also there is one point to notice that considerebly affects the  **outcome** . The _CountVectorizer()_ gives like **14 False Negative** and **71 False Positive** in contusion      matrix , which clarifies that the model is gonna be affected due to the _False Positive_ result . And since **Tf-IDF** out performs the _Fasle Positive_ result by minimizing it    to **6** so _TF-IDF_ is used for vectorizing purpose.

---

## 📂 Project Structure

- `Sentiment_analysis_Logistic.ipynb`  
  Jupyter notebook containing the full workflow: preprocessing, feature extraction, model training, and evaluation.

- `TestReviews.csv`  
  Test dataset with sample reviews and sentiment labels.

---

## ⚙️ Workflow

1. **Data Preparation**
   - Load training data from text files.
   - It has assigned labels:  
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
   - Metrics used: Accuracy, Confusion Matrix.  

---

## 📊 Example Results

- **Accuracy:** ~85–90% (depending on parameter tuning)  
- The model correctly identifies positive and negative reviews with good balance.  

---

