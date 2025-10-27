# 📝 Mid Term Project 
**Name:** Biswajit Gorai  
**Roll No.:** MA24M009  
**Title:** Development of an RNN-Transducer (RNN-T) ASR Model using PyTorch  

---

## 📁 1. Dataset and Preprocessing  

- **Dataset:** LibriSpeech (100-hour subset)  
- **Purpose:** Automatic Speech Recognition (ASR) for English speech  
- **Preprocessing Steps:**  
  - Audio resampled to **16 kHz**  
  - Converted to **log-Mel spectrograms** as acoustic input features  
  - Text transcripts normalized and tokenized into integer sequences  
  - Final processed fields: `input_features` and `labels`

---

## ⚙️ 2. Model Architecture  

The RNN-T ASR model consists of three main components:

1. **Encoder (Acoustic Model):**  
   - Built using a **Conformer** or **BiLSTM** stack  
   - Converts input spectrograms into high-level acoustic representations  

2. **Prediction Network (Decoder):**  
   - An RNN-based network that predicts the next token conditioned on the previous output sequence  

3. **Joint Network:**  
   - Combines encoder and decoder outputs to generate posterior probabilities over the vocabulary  

> Implemented entirely in **PyTorch**, ensuring modularity and easy experimentation with encoder–decoder configurations.

---

## 🧮 3. Training Configuration  

| Parameter | Value |
|------------|--------|
| Dataset | LibriSpeech (100h) |
| Batch Size | 8 (train), 1 (eval) |
| Optimizer | AdamW |
| Learning Rate | 1e-4 |
| Loss Function | RNN-T Loss |
| Framework | PyTorch |
| Evaluation Metric | Word Error Rate (WER) |

Training was performed with gradient clipping and dynamic batching to handle variable-length inputs efficiently.

---



## ✅ 4. Conclusion  

This project demonstrates the **development of an end-to-end RNN-T ASR model** using **PyTorch** and the **LibriSpeech 100-hour dataset**.  
It covers all stages — data preprocessing, model design, training, and evaluation.  
Despite limited training iterations, the model showed effective speech–text mapping.  
Future work includes experimenting with larger encoders and beam se
