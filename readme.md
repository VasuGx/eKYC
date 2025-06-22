# 🧾 eKYC Face Verification & PAN Card OCR System

An end-to-end **electronic Know Your Customer (eKYC)** system built with **Streamlit**, **OpenCV**, **EasyOCR**, **DeepFace**, and **MySQL**. The application allows users to upload a **PAN card image** and a **selfie**, then:
- Detects and matches the face on the ID and the uploaded image
- Extracts PAN details via OCR
- Verifies identity
- Stores the user info and face embedding in a MySQL database

---

## 🚀 Features

- 🖼️ **Image Upload Interface** via Streamlit
- 🧠 **Face Detection** using Haar Cascades
- 👥 **Face Matching** with DeepFace or FaceRecognition
- 🔍 **OCR Text Extraction** using EasyOCR
- 🧾 **PAN Card Data Parsing**
- 🗃️ **MySQL Integration** for record storage
- 📊 **Duplicate Checking**
- 🪵 **Detailed Logging**

---

## 📂 Project Structure
'''
ekyc/
├── app.py # Streamlit app entry point
├── face_verification.py # Face detection and comparison logic
├── preprocess.py # Image reading and ID card region extraction
├── ocr_engine.py # EasyOCR integration for PAN text
├── postprocess.py # Parses text to structured info
├── mysqldb_operations.py # MySQL operations: insert, fetch, check
├── myutils.py # Utilities: YAML, file checks
├── config.yaml # Configuration paths
├── logs/ # Runtime logs
├── data/
│ ├── 01_raw_data/ # Raw ID and face images
│ ├── 02_intermediate_data/ # Processed face crops
└── README.md # You’re here!

'''
---

## 📷 How It Works

1. Upload a **PAN card image** and a **face/selfie image**.
2. The app extracts the face from the PAN card and compares it to the selfie.
3. If matched:
   - Uses OCR to extract the user's name, father's name, DOB, and PAN.
   - Checks for duplicate records in the database.
   - Saves new user data with face embedding to the MySQL database.

---

## 🛠️ Requirements

> 📌 Python 3.8 or later is recommended.

### 📦 Install Dependencies

```bash
pip install -r requirements.txt

🐍 Required Libraries
opencv-python

face_recognition

deepface

easyocr

streamlit

sqlalchemy

mysql-connector-python

pandas

pyyaml

numpy

logging