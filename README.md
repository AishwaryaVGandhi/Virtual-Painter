# Virtual Painter

This project is a virtual painter application that allows users to draw on screen using hand gestures detected through a webcam. It uses computer vision techniques with OpenCV and MediaPipe libraries to track hand movements and translate them into drawing actions.

## Technologies Used
- **MediaPipe** - Hand tracking and landmark detection  
- **OpenCV** - Real-time video processing and rendering  
- **NumPy** - Mathematical operations for gesture analysis
- **Time** - Time-related functions for delays, timestamps, and performance measurement
- **Os** - Operating system interactions for file handling, directory management, and environment variables

## Installation

### Prerequisites
- Windows OS 
- Webcam
- Python 3.6+

### Setup
```
pip install opencv-python mediapipe numpy
```

## Project Structure 
```
Virtual Painter
├── Images                # UI assets
│   ├── 0.png             # Default header
│   ├── 1.png             # Red color
│   ├── 2.png             # Blue color
│   ├── 3.png             # Green color
│   ├── 4.png             # Brown color
│   └── 5.png             # Eraser
├── HandTrackingModule.py  # Core detection logic
└── virtual_painter.py     # Main application
```

# Hand Tracking Module

## Features
- Real-time hand landmark detection
- Finger position tracking (21 landmarks per hand)
- Gesture recognition (fingers up/down)
- Configurable detection parameters

## Methods
- **findHands()**: Processes image and draws hand landmarks
- **findPosition()**: Returns list of landmark coordinates
- **fingersUp()**: Detects which fingers are raised


# Virtual Painter

## Features
-  4 color options + eraser
-  Canvas clearing functionality

## Controls
| Gesture | Action |
|---------|--------|
| 👆 Index finger up | Draw Mode |
| ✌️ Two fingers up | Color Selection Mode|

## Customization
```python
brushThickness = 15      # Default: 15px
eraserThickness = 50     # Default: 50px
header_height = 125      # Menu bar height
```



## Usage 

1. Run the application:
   ```bash
   python virtual_painter.py
   ```

2. Show your hand to the webcam

3. Control painting:
   - ✌️ Raise index + middle fingers to select colors from the top bar
   - 👆 Raise only index finger to draw with selected color
   - Select the eraser icon to erase

4. Press `q` to quit the application


