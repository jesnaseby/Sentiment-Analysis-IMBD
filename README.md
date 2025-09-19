# 🎬 End-to-End Movie Review Sentiment Analysis  

## 📌 Introduction  
Sentiment analysis is a key task in **Natural Language Processing (NLP)** that classifies text as *positive* or *negative*.  
In this project, we use the **IMDb Movie Reviews Dataset**, a benchmark dataset containing **50,000 highly polarized reviews** (25,000 training, 25,000 testing).  

The objective is to build an **end-to-end deep learning pipeline** that predicts the sentiment of a review. We leverage **Recurrent Neural Networks (RNNs)** to capture sequential dependencies in text and improve sentiment classification.  

---

## 📊 Dataset  
- **Source:** [IMDb 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)  
- **Size:** 50,000 reviews (balanced: 25K positive, 25K negative)  
- **Format:** CSV with two columns:  
  - `review`: The movie review text  
  - `sentiment`: Label (`positive` or `negative`)  

---

## ⚙️ Project Workflow  

### 1. Data Preprocessing  
- Clean reviews (remove HTML tags, punctuation, stopwords)  
- Tokenization and padding sequences  
- Encode sentiment labels into binary (0 = negative, 1 = positive)  

### 2. Model Architecture  
- **Embedding layer** for word representation  
- **Recurrent layers (RNN )** to capture context  
- **Dense output layer** with sigmoid activation  

### 3. Training Setup  
- Optimizer: `Adam`  
- Loss: `binary_crossentropy`  
- Epochs: 20 (early stopping suggested)  
- Batch size: 32  

### 4. Evaluation  
- Metrics: Accuracy, Loss  
- Train/validation split for monitoring overfitting  

---

## 📈 Results  

### Training Progress (20 Epochs)
- Best **validation accuracy**: ~87%  
- Best **test accuracy**: **87.0%**  
- Final test loss: ~0.33  

```text
Test Accuracy: 0.8697
Test Loss: 0.3308
