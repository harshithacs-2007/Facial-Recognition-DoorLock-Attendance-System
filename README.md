# Facial-Recognition-DoorLock-Attendance-System
A Raspberry Pi–based facial recognition door lock system using Pi Camera, relay, solenoid lock, and ultrasonic sensor — designed to unlock automatically for authorized users and record attendance.

---

## 🔍 What it does

- Detects a person’s face using the camera  
- Recognizes if the person is registered  
- Unlocks the door (using relay and solenoid lock)  
- Marks attendance with name, date, and time in a file  
- (Optional) Displays attendance through a simple web dashboard

---

## ⚙️ How it works

1. When someone stands in front of the camera, the Pi captures their image.  
2. The program compares the face with stored images.  
3. If the person matches:
   - Their name and time are recorded in the attendance file.  
   - The relay turns ON and unlocks the door for a few seconds.  
4. If no match is found, the door remains locked.

---

## 🧩 Components Used (Software Side)

- **Python** (main programming language)
- **OpenCV** – for capturing and processing camera images  
- **face_recognition** – for identifying known faces  
- **RPi.GPIO** – to control Raspberry Pi pins and relay  
- **Flask** (optional) – for web dashboard and data display  

---

## 🖥️ Folder Structure


