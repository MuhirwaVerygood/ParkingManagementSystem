# 🔐 Smart Parking Management System 🚘

An intelligent, automated parking solution designed to streamline vehicle entry and exit using **ultrasonic sensors**, **YOLOv8**, **OCR (Tesseract)**, and **RFID** payments.

This system detects incoming vehicles, captures and processes license plates using AI-powered tools, and manages secure, contactless exits through RFID-based authentication and real-time billing.

---

## ⚙️ Key Features

- 🚗 Vehicle detection using **Ultrasonic Sensors**
- 📸 License plate localization with **YOLOv8**
- 🔡 Character recognition using **Tesseract OCR**
- 💳 Secure exit authentication via **RFID Reader**
- 🧠 Arduino-controlled barrier gate
- 🕒 Time-based billing with **CSV logging**
- 🧪 Includes **mock ultrasonic sensor** for development and testing

---

## 📸 How It Works (`car_entry.py`)

1. Detects vehicle using an **ultrasonic sensor**
2. Captures image via **webcam**
3. Runs **YOLOv8** to locate the license plate
4. Uses **Tesseract OCR** to extract the plate number
5. Validates plate format and logs it with a timestamp
6. If plate is unique within cooldown, opens the gate via **Arduino**
7. Logs data for exit-time verification and billing

---

## 🛠 Tech Stack

- **Python**
- **OpenCV**
- **YOLOv8 (Ultralytics)**
- **Tesseract OCR**
- **Arduino (Serial Communication)**
- **RFID Reader**
- **CSV Logging**
- **Mock Sensors for Dev**

---

## 🚀 Getting Started

### 🔄 Clone the Repository

```bash
git clone https://github.com/MuhirwaVerygood/ParkingManagementSystem.git
cd ParkingManagementSystem-main/ParkingManagementSystem-main
```



## 📦 Installing Dependencies
✅ This project supports both conda and venv (virtualenv) Python environments.

For Conda Users
Make sure you have Anaconda/Miniconda installed, then run:
```bash
conda create -n smart-parking python=3.10
conda activate smart-parking
pip install -r requirements.txt

```

For venv (Virtualenv) Users
If you're not using Conda:
```bash 
python -m venv env
pip install -r requirements.txt
```
# Linux/MacOS:
```bash
source env/bin/activate
```

# Windows:
```bash
.\env\Scripts\activate
pip install -r requirements.txt

```


## 📂 Project Structure
## 📁 Project Structure

The repository has the following directory structure:
## 📁 Project Structure

```text
ParkingManagementSystem/
├── car_entry.py
├── plates_log.csv
├── plates/
│   ├── plate_20240501_120000.jpg
│   └── ...
├── best.pt
└── README.md
```

### File Descriptions:

- **`car_entry.py`**  
  The core Python script that handles:
  - Vehicle detection via ultrasonic sensors
  - License plate recognition pipeline
  - Gate control through Arduino serial communication
  - Data logging for billing purposes

- **`plates_log.csv`**  
  Auto-generated log file containing:
  ```csv
  timestamp,plate_number,entry_time,exit_time,amount_due
  2024-05-01 12:00:00,ABC123,2024-05-01 12:00:00,,0.00
  



 ### 🧠 car_entry.py — Core Logic Summary

- The script ties together multiple technologies to automate:

- Distance sensing and image capture

- AI-powered plate detection and recognition

- Gate control via serial communication

- Plate validation and entry tracking with cooldown logic

- Logging entries for later exit/billing validation

Sample logs will be stored in plates_log.csv and images in plates/.

## 💡 Future Enhancements
- 📊 Real-time dashboard using Flask or Django

- 💰 Payment gateway integration (e.g., mobile money, cards)

- 🗃 License plate database integration (e.g., for blacklisting)

- 📲 SMS/email notifications for parking events


## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to improve or implement.

## 📞 Contact
Made with ❤️ by MuhirwaVerygood
