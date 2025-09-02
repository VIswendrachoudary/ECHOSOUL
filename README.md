# 🧠 EchoSoul – Live Voice + Face Emotion Detection

EchoSoul is a **multi-modal emotion recognition system** that combines **voice analysis** and **facial expression detection** in real-time.  
It uses **Streamlit** for the interface, **DeepFace** for facial emotion detection, and a trained ML model (MFCC features) for voice emotion classification.  

---

## ✨ Features

- 🎤 **Voice Emotion Detection** – Uses MFCC features and ML classifier.
- 📸 **Face Emotion Detection** – Powered by [DeepFace](https://github.com/serengil/deepface).
- 🧠 **Fusion Logic** – Combines voice + face predictions with confidence weighting.
- 📊 **Real-time Dashboard** – Displays live camera feed, current emotions, and emotion history.
- ⚡ **Interactive Controls** – Start/stop recording, clear history, monitor stats.

---

## 🚀 Getting Started

### 1️⃣ Clone the repo
```bash
git clone https://github.com/yourusername/echosoul.git
cd echosoul
2️⃣ Install dependencies
bash
Copy code
pip install -r requirements.txt
If DeepFace fails, install with:

bash
Copy code
pip install deepface tf-keras
3️⃣ Run the app
bash
Copy code
streamlit run app.py
📂 Project Structure
bash
Copy code
echosoul/
│── app.py                # Main Streamlit application
│── models/
│   └── voice_model.pkl   # Pre-trained voice emotion model
│── requirements.txt      # Dependencies
│── README.md             # Documentation
⚙️ Configuration
Audio

Sample Rate: 22050 Hz

Channels: 1 (mono)

MFCC Features: 40

Fusion Logic

If both agree → high confidence

If mismatch → weighted by confidence

If only one available → fallback

📊 Output Dashboard
📹 Live Video + Detected Emotions (face, voice, fused)

🎭 Emotion Cards with emojis

📈 Statistics – recent emotion counts, agreement rate, total analyses

📌 Requirements
Python 3.8+

Streamlit

OpenCV

Librosa

PyAudio

DeepFace

Plotly

NumPy / SciPy

scikit-learn

Install all dependencies with:

bash
Copy code
pip install -r requirements.txt
🛠️ Troubleshooting
PyAudio install issues
On Windows, use:

bash
Copy code
pip install pipwin
pipwin install pyaudio
Camera not detected
Try changing index in cv2.VideoCapture(0) → cv2.VideoCapture(1 or 2).



🙌 Acknowledgments
DeepFace for face emotion recognition

Streamlit for interactive UI

Librosa for audio feature extraction
