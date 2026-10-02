# Hand Gesture Presentation Control with OpenCV

A Python computer vision project that uses OpenCV and MediaPipe to control PowerPoint presentations through real-time hand gestures.

The application detects clenched left and right fists through a webcam and uses PyAutoGUI to send keyboard commands for navigating presentation slides.

## Features

- Real-time hand detection with MediaPipe
- Webcam-based gesture recognition
- Detection of up to two hands
- Right-hand fist gesture sends the `Up` key
- Left-hand fist gesture sends the `Down` key
- OpenCV live video display
- Hand landmark visualization
- PyAutoGUI keyboard automation

## How It Works

1. The webcam captures video frames.
2. MediaPipe Hands detects hand landmarks.
3. The application evaluates the thumb, index, and middle finger distances.
4. A hand is classified as a fist when the configured distance thresholds are satisfied.
5. A right-hand fist triggers the `Up` key.
6. A left-hand fist triggers the `Down` key.
7. The process continues in real time until `q` is pressed.

## Requirements

Python 3.x and the following packages:

```bash
pip install opencv-python
pip install mediapipe
pip install pyautogui

Project Structure
.
├── HandySlides_project.py
├── README.md
├── LICENSE
└── .gitignore
Notes

Gesture detection depends on camera position, lighting conditions, hand orientation, and the configured distance thresholds.

The application uses PyAutoGUI to generate keyboard input, so the active application must be able to receive those keystrokes.

Use automated keyboard interaction only in environments where you have permission to do so.

Author

Morteza Roostaie

GitHub: https://github.com/roostaiemorteza