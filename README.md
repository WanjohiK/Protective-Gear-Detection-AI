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

## 5️⃣ EVALUATION

<img width="818" height="213" alt="image" src="https://github.com/user-attachments/assets/29e663d5-b6cf-46d6-8600-dd03ce34127a" />

📊 Metrics:
mAP@0.5: Achieved high precision
Class-wise mAP@0.5:0.95 breakdown (visualized)
Confusion Matrix + Precision-Recall curves generated

📸 Visual Outputs:
train_batch0.jpg: Ground truth boxes on training images
val_batch0_pred.jpg: Prediction overlay on validation set
results.png: Loss and mAP graphs per epoch
P_curve.png, R_curve.png: Precision and Recall curves

## 6️⃣ MODEL EXPORT

💾 Saved to Google Drive:
Exported the best model checkpoint to:
/content/drive/MyDrive/ppe_detect/best.pt

🧪 Validated Model:

<img width="388" height="95" alt="image" src="https://github.com/user-attachments/assets/d7573805-7022-4697-bed8-be36b5287a9c" />

## 7️⃣ INFERENCE

🖼 Image Predictions:
Used:

<img width="296" height="65" alt="image" src="https://github.com/user-attachments/assets/8f43012e-0b8e-4f2d-a508-d52d6d2abb7b" />

Output: Annotated images in /runs/detect/predict*/

![download](https://github.com/user-attachments/assets/9b2dbdca-78e6-4d53-840d-282597824dbe)

🎥 Video Predictions:
Used inference on 2 videos:
- PPE_Part1.mp4
- PPE_Part2.mp4
IOU Threshold: 0.1 (to detect multiple overlapping objects)

## 8️⃣ CONCLUSION
✅ Key Achievements:

- Fine-tuned YOLOv12 on PPE detection
- Model shows strong generalization on unseen images and video
- Achieves near real-time performance with high confidence
- Model artifacts are exportable and deployment-ready

  ## 9️⃣ RECOMMENDATIONS
  
🔧 Technical:

- Augment data with poor lighting, motion blur, and night-time scenes
- Add more PPE classes (e.g., goggles, boots)
- Try YOLOv12n for lightweight edge deployment

🚀 Business:
- Integrate into CCTV systems
- Use alerts for non-compliance detection
- Pilot test in a real-world site with feedback loop

