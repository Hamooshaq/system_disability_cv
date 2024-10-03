Disability Detection System using YOLO

This project aims to build a computer vision model that detects disabilities such as old-aged persons, people using canes, and wheelchair users in public spaces. The model uses YOLO (You Only Look Once) architecture and is trained on a custom dataset.

Table of Contents

Project Overview
Dataset
Model
Installation
Usage
Results
Contributing
License
Project Overview

The goal of this project is to develop a YOLO-based model that detects:

Old-aged persons
Individuals using canes
Wheelchair users
The dataset consists of images from real-world scenarios, and the project aims to improve accessibility by integrating this detection system into various applications like public transportation monitoring systems.

Dataset

The dataset is structured into three main parts:

Train: Used for training the YOLO model
Validation: Used for evaluating the model during training
Test: Used for testing the model after training
Dataset Structure
The dataset follows this folder structure:

arduino
Copy code
dataset/
│
├── train/
│   └── image/
│       └── [training images]
├── valid/
│   └── image/
│       └── [validation images]
└── test/
    └── image/
        └── [test images]
Each of these directories contains an annotation.csv file with bounding box coordinates and class labels. The classes are:

old-aged-person
cane
wheelchair
YAML File
A configuration file datasett_augmented.yaml is used to define the paths and classes for the YOLO model:

yaml
Copy code
names:
- old-aged-person
- cane
- wheelchair
nc: 3
train: /path_to_dataset/train/image
val: /path_to_dataset/valid/image
test: /path_to_dataset/test/image
Model

We are using YOLOv8 for detecting the three classes of objects:

YOLOv8n: A lightweight version of YOLO for faster performance
YOLOv8: A more robust version with higher accuracy
Pre-trained weights can be fine-tuned using the provided dataset.

Contributing

We welcome contributions to improve this project. To contribute:

License

This project is licensed under the MIT License. See the LICENSE file for more details.
