# Real-Time Object Detection and Distance Measurement System

This project integrates the YOLO object detection model with an Intel RealSense depth camera to enable real-time object detection, dimension calculation, and distance measurement. It is designed for applications in robotics, autonomous vehicles, and industrial automation.

---

## Features

- **Object Detection**: Utilizes YOLO for identifying objects in real time.
- **Dimension Calculation**: Calculates real-world dimensions of detected objects.
- **Distance Measurement**: Measures the distance between objects using Intel RealSense depth data.
- **Real-Time Processing**: Provides immediate feedback with bounding boxes and labels overlaid on the video stream.

---

## Requirements

### Hardware

- **Intel RealSense Depth Camera** (e.g., D435, D455, or similar)
- A computer with at least one USB 3.0 port

### Software

- Python 3.7 or higher
- Compatible OS: Windows/Linux/macOS

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/object-detection-depth.git
cd object-detection-depth
```

### 2. Install Dependencies

Ensure you have Python 3.7 or higher installed. Then, install the required libraries:

```bash
pip install -r requirements.txt
```

#### `requirements.txt`
```plaintext
numpy
opencv-python
pyrealsense2
torch
torchvision
ultralytics
matplotlib
```

---

## Setup

1. **Connect the Intel RealSense Camera**:
   - Plug the camera into your system via USB 3.0.

2. **Download YOLO Weights**:
   - Download the pre-trained YOLO model weights (e.g., YOLOv8) from [Ultralytics](https://github.com/ultralytics/ultralytics/releases) and save them in the `models/` directory.

3. **Adjust Configuration**:
   - Edit `config.py` to set up paths, camera configuration, or YOLO settings if needed.

---

## Running the Project

Run the main script to start the system:

```bash
python main.py
```

### How It Works

- The YOLO model processes frames from the RealSense camera to detect objects.
- Depth data from the RealSense camera is used to calculate distances and dimensions.
- Bounding boxes, labels, and dimensions are displayed on the live feed.

---



---

## Troubleshooting

1. **Camera Not Detected**:
   - Ensure the RealSense SDK is installed and the camera is connected to a USB 3.0 port.

2. **YOLO Model Not Found**:
   - Verify the YOLO weights file exists in the `models/` directory and matches the path in `config.py`.

3. **Performance Issues**:
   - Close unnecessary applications to free up system resources.
   - Use a system with a GPU for better performance.

---

## References

- [Intel RealSense SDK](https://www.intelrealsense.com/sdk-2/)
- [Ultralytics YOLO](https://github.com/ultralytics/yolov8)

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
