## 1️⃣ BUSINESS UNDERSTANDING

### 🧩 Problem Statement
Workplace safety violations involving missing protective gear (helmets, vests, gloves) are frequent and dangerous. Manual inspection is inefficient and error-prone.

### 🎯 Objective
Develop an AI-powered visual detection system that can automatically identify whether workers are wearing the required protective equipment.

### 🏭 Target Use Cases
- Construction sites

- Manufacturing floors

- Warehouses

- Oil and gas facilities
  
  ## 2️⃣ DATA UNDERSTANDING

  #### 📦 Dataset Overview
Source: Roboflow PPE Detection Dataset

Classes:
- Helmet
- Vest
- Gloves
- No Helmet
- No Vest

Format: YOLO-compatible

Split:
- Train: 70%
- Validation: 20%
- Test: 10%

📂 Folder Structure

<img width="374" height="188" alt="image" src="https://github.com/user-attachments/assets/dc3166e9-01ec-48c2-90a5-f4b370a3bef7" />

## 3️⃣ DATA CLEANING & PREPARATION

✅ Steps Taken:
Downloaded dataset using Roboflow API

Cleaned the data.yaml file to include correct image paths:

<img width="365" height="109" alt="image" src="https://github.com/user-attachments/assets/14908030-b7e3-4bfa-aa01-7f9dd72af343" />

Verified consistency between image and label files

Checked for GPU availability (used Google Colab + CUDA)

## 4️⃣ MODEL TRAINING (YOLOv12)

🛠 Configuration:

Model: YOLOv12m

- Training Framework: Ultralytics
- Epochs: 50
- Dataset: Roboflow PPE v2
- Hardware: Google Colab GPU

📈 Training Summary:
Used command:
<img width="363" height="73" alt="image" src="https://github.com/user-attachments/assets/c9bf4286-bbda-4bc2-a6d9-28c3cbd545c0" />


