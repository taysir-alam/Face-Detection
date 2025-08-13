# Face Detection Project

Real-time face detection using OpenCV’s Haar Cascade classifier. The program opens a webcam stream, detects frontal faces, and draws bounding boxes with a simple on-screen status overlay. I initially built this as an intro to OpenCV for **basketball analytics** (e.g., tracking where people are in frame).

<div align="center">
  <img src="https://github.com/user-attachments/assets/c7d8019c-835a-44c1-9f64-8f86c67d500b" alt="image" width="370">
</div>
---

## Features
- **Live webcam inference** with OpenCV `VideoCapture`
- **Haar Cascade** (frontal face) via `CascadeClassifier::detectMultiScale`
- **Visual feedback**: rectangles over faces and a small banner with the face count
- Portable C++ build (Linux/macOS/Windows)

> Haar cascades work best with good lighting and frontal views. For tougher cases, consider switching to a DNN-based detector later.
---
## Quick Start

### Prerequisites
- C++17 (or later) compiler
- OpenCV **4.x** (OpenCV 3.x can work, adjust the pkg-config name as needed)
- A webcam
- The Haar cascade XML file: `haarcascade_frontalface_default.xml`  
  (This ships with OpenCV; it’s typically inside OpenCV’s `data/haarcascades` directory. Place a copy next to the executable, or update the path in the source.)

