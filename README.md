
# 🧠 Parkinson’s Disease Detection from Speech using Deep Learning

## 📋 Overview

This project detects **Parkinson's Disease** from voice recordings using a trained deep learning model based on **MFCC (Mel Frequency Cepstral Coefficients)** features. A **Keras model** is used to classify whether the uploaded speech sample indicates a healthy individual or one with Parkinson’s. The application is deployed using **Streamlit** for an intuitive web interface.

---

## ✅ Features

- 🎙 Upload a `.wav` audio file and get a real-time prediction
- 🔍 Extract MFCC features using Librosa
- 🧠 Pre-trained Keras model (CNN/LSTM/Hybrid)
- 📈 Visualize MFCC spectrogram in the app
- 🧪 Confidence score with prediction result

---

## 🛠 Tools & Technologies Used

- **Python**
- **TensorFlow / Keras**
- **Librosa**
- **NumPy**
- **Matplotlib**
- **Streamlit**

---

## 🚀 How It Works

1. User uploads a `.wav` audio file.
2. MFCC features are extracted using `librosa`.
3. Features are padded or trimmed to match model input size.
4. Model predicts whether the speaker has Parkinson’s or not.
5. Results and spectrogram are displayed in Streamlit.

---

## 📁 File Structure

```
parkinsons-detector/
├── app.py                  # Streamlit web app with model and feature extraction
├── parkinson_model.h5      # Pre-trained model (place here)
├── temp_audio.wav          # Temporary audio file (generated at runtime)
├── README.md               # Project documentation (this file)
```

---

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/parkinsons-detector.git
cd parkinsons-detector

# Create virtual environment (optional)
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt
```

---

## 🧠 Model Details

- Input: 40 MFCC coefficients over 150 time steps (reshaped to 1 x 40 x 150)
- Output: Probability of "Healthy" or "Parkinson’s"
- Model: Trained CNN/LSTM hybrid (details in training script)

---

## 🧪 Usage

Run the Streamlit application:

```bash
streamlit run app.py
```

Upload a **WAV** file (speech sample) and view:

- MFCC Spectrogram
- Disease Prediction (Healthy / Parkinson’s)
- Confidence Score

---

## 🔍 Sample Prediction

```
Prediction: Parkinson's
Confidence: 0.94
⚠️ High risk of Parkinson's detected. Consult a doctor.
```

---

## 🧾 Requirements (requirements.txt)

```txt
streamlit
numpy
librosa
matplotlib
tensorflow
```

---

## 🧠 Dataset & Training

- Dataset used: [UCI Parkinson's Telemonitoring Voice Dataset](https://archive.ics.uci.edu/ml/datasets/parkinsons+telemonitoring)
- MFCC features extracted with Librosa
- Trained on spectrogram slices using CNN/LSTM hybrid architecture

---

## 📌 Future Improvements

- 🎙 Add real-time audio recording in the app
- 📊 Add voice signal pre-processing and augmentation
- 🔁 Model retraining with larger datasets
- 🤖 Deploy with Flask/FastAPI backend for mobile use

---

## 🙌 Author

Developed by **Akash**  
Machine Learning Engineer | 2025

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Contributions

Feel free to fork, contribute, or open issues.
