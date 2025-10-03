# 📌 Sentiment Analysis on IMDB Reviews with LSTM  

This project implements **sentiment analysis** on the **IMDB 50K Movie Reviews Dataset** using a **Long Short-Term Memory (LSTM)** network in **TensorFlow/Keras**.  
The model classifies reviews as **positive** or **negative** based on the review text.  

---

## 📂 Dataset  
- **Source**: [IMDB 50K Movie Reviews Dataset](https://ai.stanford.edu/~amaas/data/sentiment/)  
- **Size**: 50,000 movie reviews (balanced: 25k positive, 25k negative)  
- **Format**: Plain text reviews with binary sentiment labels (positive/negative).  

---

## ⚙️ Project Workflow  

1. **Data Preprocessing**
   - Loaded IMDB dataset.  
   - Tokenized and padded text sequences.  
   - Converted reviews into numerical format suitable for LSTM.  

2. **Model Architecture**
   - **Embedding Layer**: Converts words into dense vectors.  
   - **LSTM Layer**: Captures sequential dependencies in reviews.  
   - **Dense Layer**: Fully connected for binary classification.  
   - **Sigmoid Activation**: Outputs probability (positive vs negative).  

3. **Training**
   - Loss Function: **Binary Crossentropy**  
   - Optimizer: **Adam**  
   - Metric: **Accuracy**  
   - Early stopping used to prevent overfitting.  

4. **Evaluation**
   - Tested on the hold-out test set (25,000 reviews).  
   - Achieved **~85–88% accuracy** (depending on hyperparameters).  

---

## 📊 Model Summary  

| Layer (type)      | Output Shape        | Param #   |
|-------------------|---------------------|-----------|
| Embedding         | (None, 200, 128)    | 640,000   |
| LSTM              | (None, 128)         | 131,584   |
| Dense             | (None, 1)           | 129       |

*Example with vocab size = 5000, embedding_dim = 128, input_length = 200.*  

---

## 🚀 How to Run  

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Sentiment-Analysis-IMDB-LSTM.git
   cd Sentiment-Analysis-IMDB-LSTM
