# Crowd Counting

The goal of this project is crowd counting analysis based on image and video dataset input.

# Introduction

This project leverages an image-based dataset to build models that analyse and count the number of people in a crowded scenery. The trained models have been implemented on videos for a practical application of the project.

# Project Structure

```
project
├── README.md
├── casacded_cnn.ipynb
├── cascaded_cnn_regression_only.pth
├── clip_vitb.ipynb
├── crowd_counting_model_sam.pth
├── mcnn_csrnet_vgg.ipynb
├── sam_vith.ipynb
├── yolo_optical_flow.ipynb
├── yolov8.ipynb
└── yolov8m.pt
```

# Key Components

- **casacded_cnn.ipynb**: A Cascaded CNN model for achieving multi-scale feature extraction. Uses a Gaussian kernel based density mapping process through which images are processed through separate density sampling layers.
- **cascaded_cnn_regression_only.pth:** A custom PyTorch model checkpoint for the Cascaded CNN model.
- **clip_vitb.ipynb**: A Contrastive Language-Image Pre-training (CLIP) model with a custom block wise classification head to to replicate results of DMCount-like models, combining regression and classification results to provide robust results for discrete counts and continuous density maps.
- **crowd_counting_model_sam.pth**: A PyTorch model checkpoint for the SAM ViT-H model.
- **mcnn_csrnet_vgg.ipynb**: A model that integrates components from two crowd counting architectures: Multi Column CNN and Congested Scene Recognition Network.
- **sam_vith.ipynb**: A Segment Anything Model (SAM) with a Vision Transformer-Huge (ViT-H) backbone to approach crowd counting by integrating head localisation, segmentation and regression-based crowd counting network. 
- **yolo_optical_flow.ipynb**: A YOLO-based model with integrated Optical Flow system to add a layer of depth and analysis of the crowd movement in the system.
- **yolov8.ipynb**: A YOLO-based system which utilizes a direct single-stage object detection paradigm. 
- **yolov8m.pt**: A PyTorch model checkpoint for the YOLOv8 model.

# Models Used

The project implements five deep learning models to predict the number of people in a crowded scenery:

- Cascaded CNN (custom)
- MCNN + CSRNet, using VGG extractor
- ViT-B/16
- SAM + ViT-H
- YOLOv8 (Fine tuned + integrated with Optical Flow)

The pre-trained YOLO model was then integrated with an Optical Flow system to give it more depth, and to help analyse more qualitative crowd motion, like direction and magnitude of speed of individuals.

# Model Implementation on Video Input

The implementation of the given models on a video input can be accessed using this link: https://drive.google.com/drive/folders/1gpwJn30qorTybmu1rfocJ8qOUrQCcwzo?usp=drive_link
