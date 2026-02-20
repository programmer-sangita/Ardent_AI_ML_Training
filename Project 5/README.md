# 😊 Real-Time Emotion Detection System

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenCV-4.x-green?style=for-the-badge&logo=opencv&logoColor=white"/>
  <img src="https://img.shields.io/badge/Keras-TensorFlow-red?style=for-the-badge&logo=keras&logoColor=white"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge"/>
</p>

<p align="center">
  A real-time facial emotion recognition system built with OpenCV and a custom-trained deep learning model — no third-party APIs required.
</p>

---

## 🎯 Overview

This project uses a **Convolutional Neural Network (CNN)** trained on grayscale facial images to detect and classify human emotions in real time via webcam. Face detection is powered by OpenCV's Haar Cascade classifier, and emotion classification is handled by a custom `.hdf5` Keras model — making the entire pipeline lightweight, fast, and fully offline.

---

## 🧠 Detected Emotions

| Label     | Emoji |
|-----------|-------|
| Angry     | 😠    |
| Disgust   | 🤢    |
| Fear      | 😨    |
| Happy     | 😄    |
| Sad       | 😢    |
| Surprise  | 😲    |
| Neutral   | 😐    |

---

## 🗂️ Project Structure

```
emotion-detection/
│
├── emotion_detection.py               # Main script for real-time detection
├── emotion_model.hdf5                 # Pre-trained CNN model
├── haarcascade_frontalface_default.xml  # Haar cascade for face detection
└── README.md
```

---

## ⚙️ How It Works

1. **Face Detection** — OpenCV's Haar Cascade scans each webcam frame and locates face regions.
2. **Preprocessing** — Detected faces are converted to grayscale, resized to `64×64` pixels, and normalized to `[0, 1]`.
3. **Emotion Prediction** — The preprocessed face is fed into the CNN model which outputs a probability distribution across 7 emotion classes.
4. **Visualization** — A bounding box and the predicted emotion label are drawn directly on the live video feed.

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Webcam

### Installation

```bash
# Clone the repository
git clone https://github.com/programmer-sangita/emotion-detection.git
cd emotion-detection

# Install required packages
pip install opencv-python numpy tensorflow keras
```

### Run

```bash
python emotion_detection.py
```

> Press **`q`** to quit the application.

---

## 📦 Dependencies

| Package      | Purpose                          |
|--------------|----------------------------------|
| `opencv-python` | Webcam capture & face detection |
| `numpy`      | Array operations & preprocessing |
| `keras`      | Loading & running the CNN model  |
| `tensorflow` | Backend for Keras                |

---

## 🖥️ Platform Compatibility

| Platform | Status |
|----------|--------|
| macOS    | ✅ Supported (`cv2.CAP_AVFOUNDATION`) |
| Windows  | ✅ Supported (change capture backend if needed) |
| Linux    | ✅ Supported |

> **macOS Note:** This script uses `cv2.CAP_AVFOUNDATION` for camera access, which is the recommended backend on macOS.

---

## 📸 Demo

> Real-time detection draws a **green bounding box** around detected faces and displays the predicted emotion label above the box.

---

## 🔮 Future Improvements

- [ ] Add confidence score display alongside the emotion label
- [ ] Support multi-face detection in a single frame
- [ ] Export emotion logs to CSV for analysis
- [ ] Build a Streamlit or Flask web interface
- [ ] Train on a larger, more diverse dataset for improved accuracy

---

## 👩‍💻 About the Author

**Sangita** — Passionate about AI, computer vision, and building real-world ML applications.

<p>
  <a href="https://github.com/programmer-sangita">
    <img src="https://img.shields.io/badge/GitHub-programmer--sangita-181717?style=for-the-badge&logo=github"/>
  </a>
  &nbsp;
  <a href="https://github.com/programmer-sangita/portfolio">
    <img src="https://img.shields.io/badge/Portfolio-Visit-blueviolet?style=for-the-badge&logo=githubpages"/>
  </a>
</p>

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/programmer-sangita">Sangita</a>
</p>
