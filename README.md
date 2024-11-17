# Home Security System

This project implements a smart home security system utilizing ESP32-CAM for image capturing and facial recognition for monitoring and authentication. The system is designed to recognize faces entering the house, providing an additional layer of security.

---

## Features

- **Image Capture**: The ESP32-CAM, programmed using Arduino, captures images of individuals entering the house.
- **Web Interface**: A built-in HTML webpage allows users to manually capture, reset, or rotate images.
- **Local Storage**: Captured images are stored locally for further processing.
- **Facial Recognition**: Python scripts utilize the `numpy` and `face_recognition` libraries to analyze captured images.
- **Residual Networks Algorithm**: The system employs a ResNet-based deep learning algorithm for accurate facial recognition.
- **Output**: The system determines whether the face is recognized or not based on a pre-existing database.

---

## Components Used

1. **ESP32-CAM**: Used for capturing images.
2. **FTDI Programmer**: For programming the ESP32-CAM.
3. **Arduino IDE**: To program the ESP32-CAM and embed the HTML code for the web interface.
4. **Python**: For image processing and facial recognition.
   - Libraries: `numpy`, `face_recognition`
5. **Residual Networks**: For deep-learning-based facial recognition.

---

## How It Works

1. **Setup and Capture**:
   - The ESP32-CAM is connected and programmed via the FTDI Programmer using Arduino IDE.
   - The Arduino code includes embedded HTML to create a local webpage for controlling the camera (capture/reset/rotate functionality).
2. **Image Storage**:
   - Images captured by the ESP32-CAM are stored locally for further processing.
3. **Facial Recognition**:
   - Using Python, the images are analyzed using the `face_recognition` library.
   - A Residual Networks (ResNet) algorithm is employed for accurate facial feature extraction and comparison.
4. **Decision**:
   - The system compares the extracted facial features with the database.
   - It outputs whether the face is "Recognized" or "Not Recognized."

