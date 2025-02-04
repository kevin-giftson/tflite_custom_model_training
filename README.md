# tflite_custom_model_training

# Custom Object Detection with TensorFlow Lite
This repository provides a comprehensive pipeline for training and deploying custom object detection models using TensorFlow Lite (TFLite). The workflow is designed for lightweight, efficient model deployment on mobile and edge devices.

Features
Environment Setup: Create an isolated Python environment using Miniconda to manage dependencies seamlessly.
Dataset Management: Access and prepare datasets stored in Google Drive. Supports custom datasets with images and annotations.
Model Training: Train custom object detection models using transfer learning with the tflite-model-maker library.
TFLite Conversion: Convert trained models into TFLite format for optimized inference on resource-constrained devices.
Requirements
Python 3.9
Libraries: tflite-model-maker, opencv-python, numpy, pycocotools
Miniconda
Setup
Clone the Repository:

bash
Copy
Edit
git clone https://github.com/kevin-giftson/tflite_custom_model_training.git
cd repository-name  
Install Miniconda:

bash
Copy
Edit
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh  
chmod +x Miniconda3-latest-Linux-x86_64.sh  
./Miniconda3-latest-Linux-x86_64.sh -b -p ~/miniconda  
Create Environment:

bash
Copy
Edit
conda create -n myenv python=3.9  
conda activate myenv  
Install Dependencies:

bash
Copy
Edit
pip install tflite-model-maker opencv-python numpy==1.23.4 pycocotools  
Training the Model
Mount your Google Drive:

python
Copy
Edit
from google.colab import drive  
drive.mount('/content/gdrive')  
Extract the dataset:

bash
Copy
Edit
unzip /path-to-your-dataset.zip  
Run the training script:

bash
Copy
Edit
python train.py  
Deployment
The trained model is automatically converted to TFLite format for deployment on mobile or edge devices.

License
This project is licensed under the MIT License.

Contributions
Contributions, issues, and feature requests are welcome! Feel free to fork this repository and submit a pull request.
