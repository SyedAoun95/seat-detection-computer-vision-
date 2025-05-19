# seat-detection-computer-vision-
Empty and full chair detection(Computer vision)


# Chair Occupancy Detection using YOLOv8

This project focuses on detecting **empty** and **occupied** chairs using the YOLOv8 object detection model. The system is designed to aid **visually impaired individuals** by identifying available seating spaces in real-time.

## 📌 Project Overview

* **Goal**: To build a lightweight and accurate object detection system that can differentiate between empty and full chairs.
* **Use Case**: Assist visually impaired people in finding available seating.
* **Model**: YOLOv8 (You Only Look Once - Version 8)
* **Training Platform**: Google Colab

## 📁 Directory Structure

```
ChairOccupancyDetection/
├── runs/                   # YOLOv8 training results
├── datasets/               # Custom dataset with empty and occupied chairs
├── best.pt                 # Trained YOLOv8 weights
├── detect.py               # Inference script
├── README.md               # Project documentation
└── yolov8_chair.ipynb      # Main training & evaluation notebook
```

## ✅ Features

* **Custom Object Detection**: Trained to recognize two classes:

  * `Empty Chair`
  * `Occupied Chair`
* **Portable**: Trained using Ultralytics' YOLOv8 in Google Colab for easy reproducibility.
* **Assistive Application**: Helps improve accessibility for the visually impaired.

## 🧠 Model Training Details

* **Framework**: YOLOv8 (Ultralytics)
* **Dataset**: Custom-labeled dataset with images of chairs in various environments.
* **Training Environment**: Google Colab with GPU acceleration.
* **Annotations**: YOLO format (`.txt` files with class and bounding boxes).

## ⚙️ How to Use

1. **Clone the YOLOv8 Repo** (if not already):

   ```bash
   git clone https://github.com/ultralytics/ultralytics
   cd ultralytics
   pip install -r requirements.txt
   ```

2. **Run Inference**:

   ```bash
   yolo task=detect mode=predict model=best.pt source=path/to/image_or_video
   ```

3. **Example**:

   ```bash
   yolo task=detect mode=predict model=best.pt source=test_images/
   ```

4. **Visual Output**:
   Detected chairs will be labeled as either `Empty Chair` or `Occupied Chair` in the output images/videos.

## 📦 Model File

The trained model is saved as `best.pt` and can be used for inference on new data.

## 🚀 Deployment (Optional)

You can integrate this model with:

* Raspberry Pi and camera for real-time detection.
* Voice assistant or speaker to audibly inform the user of chair availability.



