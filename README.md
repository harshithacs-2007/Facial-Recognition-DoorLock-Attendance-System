# Face Recognition Attendance System

A Raspberry Pi–based attendance system that uses facial recognition to identify individuals and log attendance automatically.

---

## 🧠 Overview

This system detects a person using sensors, captures their face using a Pi Camera, and records attendance in a local database when a match is found.

---

## 📂 Project Structure

Attendance_System/
│
├── encode_faces.py # Generates encodings from known faces
├── database.py # Creates and manages SQLite database
├── attendance_logger.py # Logs recognized faces into database
├── sensor_trigger.py # Reads sensor data (PIR / Ultrasonic)
├── face_recognition_main.py # Main integration file
│
├── dataset/
│ └── known/
│ ├── Person1/
│ │ ├── 1.jpg
│ │ └── 2.jpg
│ └── Person2/
│ ├── 1.jpg
│ └── 2.jpg
│
├── encodings.pickle
└── attendance.db

---

---

## ⚙️ Setup Instructions

### 1️⃣ Install Dependencies
```bash
sudo apt update
sudo apt install python3-pip python3-opencv python3-numpy
pip install face_recognition dlib

2️⃣ Prepare Dataset

Add your known faces in:

dataset/known/<PersonName>/


Each folder should contain 3–10 clear face images.

3️⃣ Encode Faces

Run once to create face encodings:

python3 encode_faces.py


This generates encodings.pickle.

4️⃣ Initialize Database
python3 -c "from database import init_db; init_db()"

5️⃣ Run the Main Script

With Raspberry Pi Camera & Sensor:

python3 face_recognition_main.py


Without hardware (testing on PC):

python3 face_recognition_main.py --simulate

🔌 Hardware Used

Raspberry Pi 4 (4GB)

Raspberry Pi Camera Module

HC-SR04 Ultrasonic Sensor / PIR Sensor

5V 3A Power Adapter

Breadboard + Jumper Wires

MicroSD Card (≥32 GB)
