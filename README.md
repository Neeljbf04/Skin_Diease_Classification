# 🩺 Skin Disease Classification using YOLOv8  

This project focuses on **skin disease classification** using **YOLOv8 (classification mode)**. It utilizes a dataset containing **900 images** categorized into **9 different skin diseases**, helping to develop an AI-powered diagnostic tool for dermatology.  

## 📂 Dataset Information  
The dataset consists of **900 labeled images**, split into **80% training and 10% validation and 10% testing**. The model is trained to classify the following skin conditions:  

- **Actinic Keratosis**  
- **Atopic Dermatitis**  
- **Benign Keratosis**  
- **Dermatofibroma**  
- **Melanocytic Nevus**  
- **Melanoma**  
- **Squamous Cell Carcinoma**  
- **Tinea/Ringworm/Candidiasis**  
- **Vascular Lesion**  

## 🛠️ Tech Stack  
- **Framework:** PyTorch, Ultralytics YOLOv8  
- **Dataset:** Kaggle (Nooby123/Skin-Disease)  
- **Optimization:** Adam Optimizer (`lr=1e-4`)  
- **Image Size:** 224x224  
- **Batch Size:** 32  
- **Training:** 15 epochs  

## 🚀 How to Run  
1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/skin-disease-classification.git  
   cd skin-disease-classification  
   ```
2. Install dependencies:  
   ```bash
   pip install torch torchvision ultralytics kagglehub matplotlib  
   ```
3. Download the dataset:  
   ```python
   import kagglehub  
   path = kagglehub.dataset_download("nooby123/skin-disease")  
   ```
4. Train the YOLOv8 classifier:  
   ```python
   from ultralytics import YOLO  
   model = YOLO('yolov8s-cls.pt')  
   model.train(data=path, epochs=15, imgsz=224, batch=32, optimizer='Adam', lr0=1e-4)  
   ```

## 📊 Evaluation Metrics  
After training, the model will be evaluated using:  
- **Accuracy**  
- **Precision**  
- **Recall**  
- **F1 Score**  
