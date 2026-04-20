🌟 Deep Learning Mini Project
YOLOv8, YOLOv11 & Faster R-CNN — Object Detection Models

This repository contains my work on three popular object detection models: YOLOv8, YOLOv11, and Faster R-CNN.
Each model has been trained on a custom dataset and includes everything you need — training scripts, model weights, and inference notebooks.

If you're looking for a simple and clean reference for object detection, this repo will help you get started fast.

📁 Project Structure
Deep-Learning-Mini-Project/
│
├── yolov8/
│   ├── train.py
│   ├── best.pt
│   ├── data.yaml
│   └── inference.ipynb
│
├── yolov11/
│   ├── train.py
│   ├── best.pt
│   ├── data.yaml
│   └── inference.ipynb
│
├── fasterRCNN/
│   ├── train_frcnn.py
│   ├── 27.pth   (Stored using Git LFS)
│   └── inference_frcnn.ipynb
│
└── README.md
🚀 About the Models
YOLOv8

A fast and reliable one-stage detector.
Good for real-time applications and lightweight deployment.

YOLOv11

An improved, more accurate version of YOLOv8.
Better performance on small or medium datasets.

Faster R-CNN

A two-stage detector known for high accuracy on detailed images.
Slower than YOLO models but often more precise.

⚙️ Setup & Installation
Create an environment
conda create -n detection python=3.10 -y
conda activate detection
Install dependencies
pip install torch torchvision torchaudio
pip install ultralytics opencv-python matplotlib
pip install pycocotools
🏋️ Training the Models
Train YOLOv8
yolo task=detect mode=train model=yolov8s.pt data=data.yaml epochs=50 imgsz=640
Train YOLOv11
yolo task=detect mode=train model=yolov11s.pt data=data.yaml epochs=50 imgsz=640
Train Faster R-CNN
python train_frcnn.py
🔍 Running Inference
YOLOv8 / YOLOv11
yolo task=detect mode=predict model=best.pt source=example.jpg
Faster R-CNN
python inference_frcnn.py --img example.jpg
📊 Metrics Used

Each model was evaluated using common detection metrics:

mAP50
mAP50–95
Precision
Recall
COCO AP (for Faster R-CNN)

These metrics help compare accuracy and overall performance.

📌 Note on Large Files (Git LFS)

The Faster R-CNN weight file (27.pth) is larger than 100MB, so it’s stored using Git LFS.

If you're cloning this repo, make sure to run:

git lfs install
git lfs pull
🎯 Summary

This project covers:

Training three major object detection models
Comparing accuracy, speed, and usability
Setting up inference pipelines
Handling large model files with Git LFS

You can easily reuse this setup for your own detection tasks — from agriculture to surveillance, traffic, or research.
