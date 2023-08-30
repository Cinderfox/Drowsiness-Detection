# Drowsiness Detection System

The Drowsiness Detection System is a Python program designed to monitor individuals' eye movements and detect signs of drowsiness. By analyzing the behavior of their eyes, the system can identify potential drowsy states and trigger alerts to ensure safety.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Eye Aspect Ratio](#eye-aspect-ratio)
- [Face Detection and Landmarks](#face-detection-and-landmarks)
- [Alert Mechanism](#alert-mechanism)
- [Requirements](#requirements)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Drowsiness Detection System showcases the application of computer vision techniques to real-world safety concerns. By continuously monitoring eye movement patterns, the program can recognize when an individual's eyes show signs of fatigue or drowsiness.

## Features

The Drowsiness Detection System offers several key features:

- Eye Aspect Ratio Calculation: The program calculates the Eye Aspect Ratio (EAR) to determine the degree of eye closure, a crucial indicator of drowsiness.
- Real-time Monitoring: The system monitors individuals' eye movements in real-time through a camera feed.
- Alert Mechanism: When the EAR falls below a certain threshold for a specified duration, the system triggers an alert to notify the individual.

## Installation

To set up the Drowsiness Detection System on your system, follow these steps:

1. Ensure that you have Python 3.x installed.
2. Install the required libraries using the commands:
   - `pip install scipy`
   - `pip install imutils`
   - `pip install dlib`
   - `pip install opencv-python`
   - `pip install pygame`

## Usage

Using the Drowsiness Detection System is simple:

1. Run the program using a Python interpreter: `python drowsiness_detection.py`.
2. Ensure that the camera is properly configured and capturing the individual's face.

## How It Works

### Eye Aspect Ratio

The system calculates the Eye Aspect Ratio (EAR) using the formula:

EAR = (A + B) / (2 * C)

Where:
- A: Euclidean distance between the two vertical eye landmarks
- B: Euclidean distance between the two horizontal eye landmarks
- C: Euclidean distance between the two horizontal eye landmarks

### Face Detection and Landmarks

1. Face Detection: The system employs the `dlib` library for frontal face detection. Detected faces are then analyzed for eye movement patterns.
2. Landmarks Prediction: The program predicts 68 facial landmarks using the "shape_predictor_68_face_landmarks.dat" model.

### Alert Mechanism

1. Continuous Monitoring: The program continuously tracks the EAR and updates its value in real-time.
2. Drowsiness Detection: If the calculated EAR falls below a certain threshold (`thresh`), the program starts counting the number of frames where the EAR remains below the threshold.
3. Alert Trigger: If the number of frames with low EAR exceeds a specified limit (`frame_check`), the program triggers an alert by displaying warning text and playing an alarm sound.

## Requirements

- Python 3.x
- Libraries: scipy, imutils, dlib, opencv-python, pygame

## Contributing

Contributions to the Drowsiness Detection System are welcome! If you have ideas to enhance the program's accuracy, optimize its performance, or add new features, feel free to submit a pull request.

## License

This program is open-source and distributed under the MIT License.

Feel free to customize this README to provide comprehensive insights into the Drowsiness Detection System. The goal is to offer clear instructions and valuable information to users and potential contributors.
