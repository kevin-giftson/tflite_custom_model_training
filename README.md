# TFLite Custom Model Training

This repository provides a streamlined pipeline for **training and deploying custom object detection models** using **TensorFlow Lite (TFLite)**. The workflow is designed for lightweight and efficient deployment on **mobile and edge devices**.

---

## **Features**
- **Environment Setup**: Use Miniconda to create an isolated environment for seamless dependency management.
- **Dataset Management**: Manage and prepare custom datasets, including annotations and images.
- **Model Training**: Train object detection models using transfer learning with the `tflite-model-maker` library.
- **TFLite Conversion**: Optimize trained models for deployment on resource-constrained devices.

---

## **Repository Clone**

To clone this repository, use the following command:
```bash
git clone https://github.com/kevin-giftson/tflite_custom_model_training.git
cd tflite_custom_model_training
```

## **Requirements**
- Python 3.9
- Libraries:
- tflite-model-maker
- opencv-python
- numpy==1.23.4
- pycocotools
- Miniconda

## **Setup**
- **1. Install Miniconda:**
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
chmod +x Miniconda3-latest-Linux-x86_64.sh
./Miniconda3-latest-Linux-x86_64.sh -b -p ~/miniconda
```
- **2. Create and Activate Environment:**
```bash
conda create -n myenv python=3.9
conda activate myenv
```
- **3. Install Dependencies:**
```bash
pip install tflite-model-maker opencv-python numpy==1.23.4 pycocotools
```

## **Dataset Preparation **
- **1. Mount Google Drive (if using Colab):**
```bash
from google.colab import drive
drive.mount('/content/gdrive')
```
- **2. Extract Dataset:** Place your dataset (e.g., dataset.zip) in the appropriate location and unzip it:
```bash
unzip /path-to-your-dataset.zip
```
##**Model Training**
- **Run the training script:**
```bash
python train.py
```
The training script performs:
- Data preprocessing.
- Model training using transfer learning.
- Evaluation and saving of the trained model.

  tflite_custom_model_training/
├── train.py              # Training script for the object detection model
├── tflite_custom_model   # jupyter source file
├── picam_detect          # detection file for raspi cam
├── detect                # detection file for normal cam
├── README.md             # Documentation file
└── ...                   # Other related scripts or files
