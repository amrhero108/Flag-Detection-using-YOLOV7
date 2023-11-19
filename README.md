# Flag Detection with YOLOv7

## Overview

This repository contains the code and resources for a machine learning project aimed at detecting flags in images using the YOLOv7 object detection model. Flags are essential elements in various contexts, such as national events, sports competitions, and public gatherings. This project leverages state-of-the-art deep learning techniques to accurately identify and localize flags within images.

## Key Features

- **YOLOv7 Implementation:** Utilizes the YOLOv7 architecture for robust and efficient object detection.
  
- **Custom Dataset:** Trained on a custom dataset curated specifically for flag detection, ensuring model accuracy in diverse scenarios.

- **Easy Configuration:** Simple configuration files for adjusting hyperparameters, dataset paths, and class labels.

- **Training and Inference Scripts:** Scripts for both model training and inference, facilitating seamless deployment.

- **Pre-trained Weights:** Pre-trained weights for YOLOv7, providing a starting point for training on your specific flag detection dataset.

## Getting Started

Follow these steps to get started with the flag detection project:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/amrhero108/Flag-Detection-using-YOLOV7.git
   cd flag-detection-yolov7
   ```

2. **Install Dependencies:**
   ```bash
   pip install -U -r requirements.txt
   ```

3. **Prepare Your Dataset:**
   Organize your flag detection dataset with images and corresponding annotation files. Refer to the documentation for dataset formatting details.

4. **Configuration:**
   Modify configuration files (`./data/custom.yaml`, `./models/yolov7-custom.cfg`) to match your dataset and requirements.

5. **Training:**
   ```bash
   python train.py --workers 1 --device 0 --batch-size 8 --epochs 150 --data data/data.yaml --img 640 640 --cfg cfg/training/yolov7-tiny.yaml --weights yolov7 tiny.pt --name yolov7finaly --hyp data/hyp.scratch.p5.yaml
   ```

6. **Inference:**
   ```bash
   python detect.py --weights best.pt --img-size 640 --conf 0.4 --source data/test/images --view-img --no-trace
   ```
