# Face Landmark Detection & Data Capture

This project is a real-time face landmark detection application built using Python, OpenCV, and Google's MediaPipe framework. It captures video from the webcam, detects facial landmarks (including irises), visualizes the face mesh, and allows users to save the landmark data to a JSON file.

## Features

- **Real-time Detection**: Utilizes MediaPipe Face Mesh for high-fidelity face landmark detection.
- **Visual Feedback**: Draws tessellation, contours, and iris connections on the video feed.
- **Status Indicator**: Displays on-screen text indicating whether a face is currently detected.
- **Data Capture**: Allows saving the 3D coordinates (x, y, z) of the detected face landmarks to a JSON file (`face_signature.json`) for potential use in authentication or analysis.

## Prerequisites

Ensure you have Python installed on your system. You will also need the following Python libraries:

- `opencv-python`
- `mediapipe`

## Installation

1.  Clone this repository or download the source code.
2.  Install the required dependencies using pip:

    ```bash
    pip install opencv-python mediapipe
    ```

## Usage

1.  Navigate to the project directory.
2.  Run the application:

    ```bash
    python app.py
    ```

3.  **Interacting with the App**:
    - The webcam feed will open, showing the face mesh overlay.
    - **Press 's'**: Save the current face landmarks to `face_signature.json`. A message will be printed to the console confirming the save.
    - **Press 'q'**: Quit the application and close the window.

## Output

- **face_signature.json**: This file is generated when you press 's'. It contains a list of lists, where each inner list represents the `[x, y, z]` coordinates of a specific facial landmark.

## Code Structure

- **app.py**: The main script that initializes the camera, processes frames with MediaPipe, handles user input, and renders the visualization.
