Problem Statement:
Modern transportation faces significant challenges such as road accidents due to human error, inefficient energy usage, and traffic congestion. 
Electric Vehicles (EVs), while offering an eco-friendly solution, still depend on human input for safe and efficient navigation.
To achieve true intelligent mobility, there is a need for an autonomous driving system capable of perceiving, learning, and making real-time driving decisions.


## deployment link of chatbot
https://huggingface.co/spaces/MangaliAshwitha/EVchatbot

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
## Technologies Used

Python – Core programming language

TensorFlow / Keras – Deep learning framework for CNN model

Flask & SocketIO – Real-time communication between simulator and model

OpenCV & NumPy – Image preprocessing and numerical operations

Udacity Self-Driving Car Simulator – For data collection and testing

## Model Details

Framework: TensorFlow / Keras

Model Type: Convolutional Neural Network (CNN) for regression

Input: Preprocessed road images (200×66, YUV color space)

Output: Continuous steering angle prediction

Preprocessing Steps:

Crop unnecessary parts of the image (sky and hood).

Convert RGB → YUV color space.

Apply Gaussian blur.

Resize to 200×66 pixels.

Normalize pixel values (divide by 255).


## Files Included

model.h5 – Trained deep learning model

drive.py – Flask-SocketIO server for real-time control

driving_log.csv – Collected driving dataset (images + telemetry data)

##  Results

The car successfully navigates the simulated track without human input.

Smooth steering and throttle control observed.

Plots of steering distribution and throttle vs speed confirm realistic driving patterns.

##  Future Scope

Integration with real EVs for hardware testing.

Addition of lane detection, obstacle avoidance, and traffic sign recognition.

Optimization for low-power embedded systems in electric vehicles.

👩‍💻 Contributors

Project by: Mangali Ashwitha
Department of Information Technology
JNTUH-University college of engineering jagitial
