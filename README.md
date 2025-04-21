# Real-time-Auto-License-Plate-Recognition-with-Jetson-Nano-slashmark

# 🎥 Real-Time Object Detection with Jetson Inference

This repository contains a Python script that performs real-time object detection using NVIDIA Jetson's `jetson-inference` framework. It leverages a live video stream (e.g., from a webcam or IP camera) to detect objects using pre-trained deep learning models such as `SSD-Mobilenet-v2`.

## 📦 Features

- Real-time object detection using Jetson's deep learning models.
- Configurable input and output streams (camera, files, RTSP, etc.).
- Overlay bounding boxes, class labels, and confidence scores.
- Customizable detection threshold.
- Performance statistics per frame.

## 🧠 Requirements

- NVIDIA Jetson device (e.g., Jetson Nano, Xavier, TX2)
- JetPack SDK (includes `jetson-inference`)
- Python 3.x
- `jetson-inference` and `jetson-utils` Python modules

> Make sure your device has the [jetson-inference](https://github.com/dusty-nv/jetson-inference) library set up.

## 🚀 Getting Started

1. **Clone this repository**:

   ```bash
   git clone https://github.com/PSaiPrathap/Real-time-Auto-License-Plate-Recognition-with-Jetson-Nano-slashmark
   cd jetson-detectnet-camera
   ```

2. **Run the script**:

   ```bash
   python3 detectnet-camera.py /dev/video0 output.mp4
   ```

   Or with custom options:

   ```bash
   python3 detectnet-camera.py /dev/video0 display://0 --network=ssd-mobilenet-v2 --overlay=box,labels,conf --threshold=0.5
   ```

## 🛠️ Command-Line Arguments

| Argument        | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `input_URI`     | URI of the input stream (camera, file, RTSP, etc.)                         |
| `output_URI`    | URI of the output stream (file, display, etc.)                             |
| `--network`     | Pre-trained model to use (e.g., `ssd-mobilenet-v2`, `ssd-inception-v2`)    |
| `--overlay`     | Overlay types: `box`, `labels`, `conf`, or `none`                          |
| `--threshold`   | Minimum detection confidence threshold (0.0 to 1.0)                         |

## 📸 Example Output
![ocr_result](https://github.com/user-attachments/assets/5772e9a0-e8d6-44f5-af8b-5f3e4986d89a)

