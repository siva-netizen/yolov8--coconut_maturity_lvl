# 🥥 Coconut Maturity Level Detection using YOLOv8

This project implements an object detection model using **YOLOv8** to detect **on-tree mature coconuts**. It leverages **Roboflow** for dataset handling and **Ultralytics YOLO** for model training, validation, and inference.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/siva-netizen/yolov8--coconut_maturity_lvl/blob/main/yolo%5Bcoconut%5D.ipynb)

---

## 🚀 Features

- Uses **YOLOv8** for object detection  
- Integrated with **Roboflow API** for dataset access  
- Includes **data augmentation** techniques (Mosaic, Mixup, HSV adjustments, etc.)  
- Trains and validates on GPU (if available)  
- Visualizes predictions on sample images  

---

## 📁 Dataset

- **Dataset Name**: On-Tree Mature Coconut Fruit Detection  
- **Source**: [Roboflow](https://roboflow.com/)  
- **Classes**: Presumably different maturity levels or general coconut detection  
- **Format**: YOLO format (downloaded via Roboflow API)  

---

## 🛠️ Installation

Install the necessary dependencies:

```bash
pip install ultralytics roboflow opencv-python torch torchvision numpy matplotlib
```

---

## 💻 Usage

Run the notebook on Google Colab or your local Jupyter environment. The main steps include:

1. Import Required Libraries  
2. Connect to Roboflow and Download Dataset  
3. Define Augmentations  
4. Train the YOLOv8 Model  
5. Validate Model Performance  
6. Perform Inference and Visualize Results  

---

## ⚙️ Configuration

Augmentation parameters:

```python
augmentation = {
    "flipud": 0.5,
    "fliplr": 0.5,
    "mosaic": 1.0,
    "mixup": 0.2,
    "hsv_h": 0.015,
    "hsv_s": 0.7,
    "hsv_v": 0.4
}
```

Training command example:

```python
model.train(data="path/to/data.yaml", epochs=50, imgsz=640, batch=16)
```

---

## 🖼️ Sample Output

- Runs YOLOv8 inference on test images  
- Visualizes bounding boxes and confidence scores  
- Uses OpenCV and Matplotlib for plotting  

---

## 📌 Notes

- Be sure to use your own **Roboflow API key**  
- Ensure a **GPU runtime** is selected for faster training  
- You can export the model to **ONNX**, **TFLite**, or **CoreML** formats for deployment  

---

## 📜 License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details.
