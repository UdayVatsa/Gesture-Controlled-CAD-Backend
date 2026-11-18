# Gesture-Controlled CAD – Python Backend

Python backend for a gesture-controlled 3D CAD modelling application, developed as part of a team project.

The backend uses webcam input and computer vision to track hand movements, recognize gestures, and transmit tracking data to the frontend in real time.

## Features

- **Real-time Webcam Capture:** Captures video frames using OpenCV.
- **Frame Processing:** Handles image conversion, frame flipping, and preprocessing.
- **Hand Tracking:** Uses MediaPipe to detect and track 21 hand landmarks.
- **Gesture Recognition:** Recognizes gestures such as open palm, fist, pinch, and peace sign.
- **Cursor Smoothing:** Reduces unwanted cursor movement and hand jitter.
- **Gesture Stabilization:** Uses frame-based thresholds to prevent accidental gesture transitions.
- **Real-time Communication:** Sends gesture states and cursor coordinates through FastAPI WebSockets.

## Tech Stack

- Python
- OpenCV
- MediaPipe
- FastAPI
- WebSockets
- Uvicorn

## Project Structure

```text
Gesture-Controlled-CAD-Backend/
├── main.py
├── tracking/
│   ├── __init__.py
│   ├── hand_tracker.py
│   └── gesture_recognizer.py
├── requirements.txt
└── README.md
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/UdayVatsa/Gesture-Controlled-CAD-Backend.git
cd Gesture-Controlled-CAD-Backend
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**macOS/Linux**
```bash
source venv/bin/activate
```

**Windows**
```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the backend

```bash
python main.py
```

The FastAPI server runs at `http://localhost:8000`, with the WebSocket endpoint available at:

```text
ws://localhost:8000/ws/tracking
```

## Original Team Project

This backend was developed as part of the following collaborative project:

[Gesture-Controlled 3D CAD Application](https://github.com/AlishLaimayum/3D-CAD-modelling-using-hand-gesture)

## Author

Uday Vatsa

