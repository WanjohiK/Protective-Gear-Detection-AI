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

project/
  └── train/
      ├── images/
      └── labels/
  └── valid/
      ├── images/
      └── labels/
  └── test/
      ├── images/
      └── labels/
