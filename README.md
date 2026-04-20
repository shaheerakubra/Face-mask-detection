# Face-mask-detection
😷 Face Mask Detection — Real-Time Computer Vision Classifier
A deep learning computer vision system that detects whether individuals are wearing face masks in real time using a webcam feed. Built using Convolutional Neural Networks (CNN) with Python, TensorFlow/Keras, and OpenCV.

📌 Overview
During and after the COVID-19 pandemic, mask compliance became a critical public health concern in schools, hospitals, and public spaces. This project automates mask detection using computer vision, enabling real-time monitoring without manual supervision.

✨ Features

🎥 Real-time detection via live webcam feed
🧠 CNN-based classifier trained to distinguish mask vs. no-mask
🟢🔴 Visual bounding box overlay — green for mask, red for no mask
⚡ Fast inference suitable for real-time use cases
🗂️ Trained on labeled image dataset with two classes: with_mask / without_mask


🛠️ Tech Stack
ToolPurposePythonCore programming languageTensorFlow / KerasDeep learning model trainingOpenCVReal-time video capture and face detectionNumPyArray and data manipulationMatplotlibTraining performance visualization

🧠 Model Architecture

Base: Convolutional Neural Network (CNN)
Input: 224x224 RGB image frames
Layers: Conv2D → MaxPooling → Flatten → Dense → Dropout → Softmax output
Output classes: with_mask | without_mask
Loss function: Binary cross-entropy
Optimizer: Adam


🏗️ How It Works
[Webcam Feed]
      |
  OpenCV captures frames
      |
  Face detected via Haar Cascade / DNN detector
      |
  Face region cropped and preprocessed (resize, normalize)
      |
  CNN Model predicts: with_mask / without_mask
      |
  Bounding box drawn on frame with label + confidence score
      |
[Live output displayed on screen]

🚀 Getting Started
Prerequisites

Python 3.x
pip

Install Dependencies
bashpip install tensorflow keras opencv-python numpy matplotlib
Run the Detector
bashpython detect_mask.py
This will open your webcam and begin real-time detection.
Train the Model Yourself
bashpython train_mask_detector.py

📂 Project Structure
face-mask-detection/
├── dataset/
│   ├── with_mask/            # Training images — masked faces
│   └── without_mask/         # Training images — unmasked faces
├── model/
│   └── mask_detector.model   # Saved trained model
├── train_mask_detector.py    # Model training script
├── detect_mask.py            # Real-time webcam detection script
├── plot_training.png         # Training accuracy/loss graph
└── README.md

📊 Training Results

Model was trained on a labeled dataset of masked and unmasked face images.
Training accuracy and loss curves are saved as plot_training.png.

(Formal evaluation metrics to be added — retraining in progress)

💡 Potential Use Cases

🏥 Hospital and clinic entry monitoring
🏫 School and university compliance checking
🏪 Retail store entry systems
🚇 Public transport monitoring


🙋‍♀️ Author
Shaheera Kubra

Email: shaheerakubra03@gmail.com
LinkedIn: linkedin.com/in/shaheera-kubra-6aa917229
