Sign Language Detection Using Mediapipe and LSTM

Project Overview

This project is designed for real-time sign language recognition using Mediapipe for pose and landmark detection and an LSTM neural network for classifying hand gestures. The project covers data collection, keypoint extraction, model training, and real-time gesture detection, with customizable settings for different sign languages or gestures.

Table of Contents

Dependencies

Dataset Creation

Model Training

Real-Time Detection

Usage

Dependencies

This project requires the following packages:

python
Copy code
!pip install tensorflow opencv-python mediapipe numpy matplotlib sklearn

Dataset Creation

Pose and Landmark Detection: Utilizes Mediapipe's Holistic model to capture landmarks on the face, hands, and body.

Keypoint Extraction: Extracts the landmark keypoints and saves them as .npy files.

Organize Data: Save each set of keypoints in organized directories by gesture type, creating a dataset for model training.

Model Training:

LSTM Neural Network: A three-layered LSTM network processes the sequences of keypoints to classify gestures.

Model Compilation and Training: The model is compiled with categorical cross-entropy as the loss function and trained over multiple epochs with TensorBoard logging.

Saving the Model: Trained weights are saved for use in real-time gesture detection.

Real-Time Detection

Prediction Pipeline: The LSTM model is used alongside OpenCV to:
Capture live video feed from a webcam.
Detect hand gestures and classify them based on model predictions.
Display predicted actions on the screen with real-time feedback.

Usage

Configure Data Paths and Actions: Define your gesture labels and data paths for storing training data.

Train the Model: Follow the steps in the notebook to train the model on your gestures.

Run Detection: Launch the webcam detection loop to recognize gestures in real-time.

Acknowledgments

This project leverages Google Mediapipe for landmark detection and TensorFlow for LSTM model implementation.

