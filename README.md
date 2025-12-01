# 🔍 Fake News Detection – Backend API  
A production-ready Machine Learning API built using Flask, designed to classify news text as **Fake** or **Real**.  
The backend powers the React-based web application and is deployed using Render.

---

## 🚀 Live API Endpoint  
Base URL  
https://fakenews-detection-backend.onrender.com

Prediction Endpoint  
POST /predict  
Content-Type: application/json  
Body → { "text": "your news here" }

Example Response  
{ "result": "fake" }

---

## 🧠 Machine Learning Model  
The backend uses a text classification model trained on a combined dataset of more than **54,000 labelled samples**.

Model Pipeline  
1. Text cleaning and normalization  
2. TF-IDF vectorization (20,000 max features)  
3. Multinomial Naive Bayes classifier  
4. Evaluation using accuracy, precision, recall and F1-score  
5. Model exported as  
   • model.pkl  
   • tfidf.pkl  

Training Script  
The full training pipeline is provided inside `train_model.py`, allowing future retraining with updated datasets.

---

## 📁 Project Structure  
api.py – Flask application and prediction route  
model.pkl – Trained ML model  
tfidf.pkl – TF-IDF vectorizer  
train_model.py – Script to retrain the model  
dataset_final.csv – Final merged dataset  
requirements.txt – Dependencies  
README.md – Documentation  

---

## ⚙️ Local Development  
Install dependencies  
pip install -r requirements.txt

Run the backend  
python api.py

Default Local URL  
http://127.0.0.1:5000

---

## 🌐 Deployment (Render)  
The backend is deployed as a free Render Web Service with:  
Build Command → pip install -r requirements.txt  
Start Command → python api.py  

The live API URL is used in the React frontend via the environment variable  
REACT_APP_API_URL

---

## 👨‍💻 Author  
Sanjay Kumar Tummala  
Machine Learning • Networking • Web Application Development  
