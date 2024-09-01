# LipBuddy - Lip Reading Application

**Status**: Ongoing Project

---

### Introduction

LipBuddy is an advanced lip-reading application built upon the LipNet deep learning model. The primary objective of this project is to translate visual lip movements into text, enhancing accessibility for individuals with hearing impairments and offering potential applications in various fields like security, silent communication, and more.

This project is still in progress, and the current implementation is a full-stack application that takes video input, processes it using deep learning, and outputs the predicted text.

### Features

- **Video Input Processing**: Converts input videos to grayscale frames, focusing on lip movements.
- **Deep Learning Integration**: Utilizes a custom-built deep neural network for processing lip movements.
- **Real-time Predictions**: Provides real-time predictions of spoken words from lip movements.
- **Streamlit Integration**: The user interface is built with Streamlit, offering a smooth and interactive experience.

### Technical Overview

1. **Data Loading**: The application loads and processes video files, extracting frames and applying transformations to prepare the data for the neural network.

2. **Neural Network Architecture**:
    - **Convolutional Layers**: Three 3D convolutional layers to capture spatio-temporal features.
    - **Bidirectional LSTM**: Two Bidirectional LSTM layers to capture the temporal dependencies in the lip movements.
    - **Dense Layer**: The output layer generates predictions for each time step, corresponding to the characters in the vocabulary.

3. **Training Process**:
    - Custom loss function using Connectionist Temporal Classification (CTC) to handle variable-length sequences.
    - Learning rate scheduler and checkpoints to ensure efficient training.

4. **Inference and Prediction**: The trained model is used to predict the spoken text from new video inputs. The predictions are decoded and displayed in the application interface.

### Streamlit Application

The user interface allows users to:

- Select a video file for processing.
- View the raw video and the processed frames seen by the model.
- Obtain the predicted text from the lip movements in the video.
