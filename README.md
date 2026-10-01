# 🩺 5-Disease Detection System: Medical Image & Data Analysis

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Framework](https://img.shields.io/badge/Framework-TensorFlow%20%7C%20Keras-orange.svg) 
![Computer Vision](https://img.shields.io/badge/Vision-OpenCV-red.svg)
![Web](https://img.shields.io/badge/Web-Flask-green.svg)

## 📌 Overview
An end-to-end machine learning system designed to classify and detect five distinct medical conditions. The project leverages Convolutional Neural Networks (CNNs) and transfer learning (VGG16) for radiographic and MRI imagery, alongside comparative machine learning models for tabular patient data. 

<img width="1919" height="923" alt="image" src="https://github.com/user-attachments/assets/bc09cc4a-8638-444e-85b0-d8b8e1f27856" />


## 🚀 Technical Architecture
* **Deep Learning (Vision):** CNN and VGG16 models trained to detect Lung COVID, Pneumonia, and Brain Tumors from imaging data. 
* **Computer Vision Pipeline:** MRI scans undergo automated preprocessing using OpenCV, which applies Gaussian blurring, thresholding, and contour detection to isolate the brain region and crop out extraneous dark space based on extreme boundary points.
* **Machine Learning (Tabular):** Benchmarked classification models leveraging Scikit-Learn to analyze patient metrics for Diabetes and Heart Disease.
* **Backend API:** Built a Flask web application (`app.py`) to handle file uploads, preprocess data, and serve real-time model predictions.
* **Frontend:** Developed a responsive user interface (`templates/` and `static/`) for seamless interaction.

## 📊 Model Performance & Metrics

| Condition | Data Type | Architecture/Model | Test Accuracy |
|:---|:---|:---|:---|
| **COVID-19** | Chest X-Ray | Custom 4-Layer CNN | **93.75%** |
| **Pneumonia** | Chest X-Ray | Custom 3-Layer CNN | **88.46%** |
| **Brain Tumor** | Brain MRI | VGG16 Transfer Learning | **91.20%** |
| **Diabetes** | Clinical Tabular | Random Forest / XGBoost | **76.62%** |
| **Heart Disease** | Patient Metrics | XGBoost Classifier | **89.13%** |

<details>
<summary><h3>🔍 Click to view sample diagnosis and UI outputs</h3></summary>
<img width="1892" height="912" alt="image" src="https://github.com/user-attachments/assets/d7639b65-3049-4fbb-8358-2b340ce93c14" />
<img width="1844" height="1054" alt="image" src="https://github.com/user-attachments/assets/f9bffa01-b4ed-4dee-a794-78049cb25b23" />
<img width="1919" height="907" alt="image" src="https://github.com/user-attachments/assets/3b2c0ba9-fe75-41bd-b319-585c79821bc6" />
<img width="1919" height="936" alt="image" src="https://github.com/user-attachments/assets/45ad35db-1cda-48b4-a0af-08f5ad6bd603" />
<img width="1691" height="1079" alt="image" src="https://github.com/user-attachments/assets/3f4d1ff6-f80f-42c5-92a3-055f62258830" />
<img width="1919" height="926" alt="image" src="https://github.com/user-attachments/assets/b5659a69-1878-4411-9d60-9c64420d8149" />
</details>

## 📁 Repository Structure
```text
├── data/               # Medical imaging and tabular datasets
├── models/             # Saved model weights
├── notebooks/          # Jupyter notebooks for EDA and model training
├── static/             # CSS and client-side assets
├── templates/          # HTML interfaces for the web app
├── .gitignore          # Ignored files and directories
├── app.py              # Main Flask application entry point
└── requirements.txt    # Python dependencies

```

## ⚙️ Local Setup

**1. Clone the repository:**
```bash
git clone https://github.com/sohamparab77/5-Disease-Detection-System.git
cd 5-Disease-Detection-System
```

**2. Install dependencies:**
```bash
pip install -r requirements.txt
```

**3. Run the application:**
```bash
python app.py
```
*Navigate to `http://localhost:5000` in your browser.*
