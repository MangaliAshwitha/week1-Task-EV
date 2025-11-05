Problem Statement:
Modern transportation faces significant challenges such as road accidents due to human error, inefficient energy usage, and traffic congestion. 
Electric Vehicles (EVs), while offering an eco-friendly solution, still depend on human input for safe and efficient navigation.
To achieve true intelligent mobility, there is a need for an autonomous driving system capable of perceiving, learning, and making real-time driving decisions.

## 🧠 Self-Driving Car Model (Behavioral Cloning)

This repository contains a trained deep learning model (model.h5) for a self-driving car simulation project based on behavioral cloning.

## 🚗 Overview

The model is a Convolutional Neural Network (CNN) trained to predict steering angles from images captured by a car’s front-facing camera.
It learns to mimic human driving behavior by mapping road images → steering commands.

## 🧩 Model Details

Framework: TensorFlow / Keras

Type: CNN for regression (steering prediction)

Input: Preprocessed road images (200×66, RGB → YUV)

Output: Continuous steering angle

## ⚙️ Usage

To load and use the model in your Python script:

from tensorflow.keras.models import load_model
model = load_model("model.h5")

# Example prediction (image should be preprocessed)
steering_angle = float(model.predict(image))
