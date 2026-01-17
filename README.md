# AI Safety Compliance System

## Overview

The AI Safety Compliance System is a computer vision–based application designed to monitor Personal Protective Equipment (PPE) compliance in workplaces such as factories, construction sites, laboratories, and industrial environments.

The system processes a video feed, detects people using a YOLOv8 model, evaluates PPE compliance, calculates risk levels, tracks repeated violations, generates annotated videos, and displays live results on a modern web dashboard.

This project is suitable for hackathons, demonstrations, academic projects, and as a base for real-world safety monitoring systems.



---<img width="1892" height="907" alt="Screenshot 2026-01-17 114107" src="https://github.com/user-attachments/assets/aed24729-d431-454d-82e7-bf79ab7063b7" />
<img width="1903" height="895" alt="Screenshot 2026-01-17 114619" src="https://github.com/user-attachments/assets/5d90c7d0-3cd7-4af1-a260-40b9f4c867eb" />


## Key Features

- Person detection using YOLOv8  
- PPE compliance analysis (Helmet, Mask, Goggles, Shoes)  
- Risk scoring (LOW, MEDIUM, HIGH)  
- Escalation logic for repeated violations  
- Incident duration tracking  
- Annotated output video with bounding boxes and labels  
- Browser-compatible video playback  
- Live dashboard with logs and statistics  
- FastAPI backend with single-page frontend  
- Works on Windows and Linux  

---

## Project Structure

safety-ppe-simple-project/  
├── backend/  
│   ├── main.py  
│   └── detect.py  
├── video/  
│   ├── sample.mp4  
│   └── output_annotated.mp4  
├── index.html  
├── requirements.txt  
├── database.db  
└── README.md  

---

## Technologies Used

- Python 3.9 or higher  
- FastAPI  
- Uvicorn  
- OpenCV  
- YOLOv8 (Ultralytics)  
- SQLite  
- HTML and Bootstrap  
- FFmpeg  

---

## Running the Project on Windows

### Step 1: Open Command Prompt or PowerShell

Navigate to the project folder:

cd path\to\safety-ppe-simple-project

---

### Step 2: Create a Virtual Environment

py -m venv venv

---

### Step 3: Activate the Virtual Environment

venv\Scripts\activate

---

### Step 4: Upgrade pip

python -m pip install --upgrade pip

---

### Step 5: Install Required Packages

python -m pip install fastapi uvicorn

pip install -r requirements.txt

---

### Step 6: Install FFmpeg

Download FFmpeg from:  
https://ffmpeg.org/download.html  

Extract it and add the ffmpeg/bin folder to your system PATH.

Verify installation:

ffmpeg -version

---

### Step 7: Run the Server

uvicorn backend.main:app --reload

---

### Step 8: Open the Application

Open your browser and go to:

http://127.0.0.1:8000

---

## Running the Project on Linux (Ubuntu / Debian)

### Step 1: Open Terminal

Navigate to the project folder:

cd ~/path/to/safety-ppe-simple-project

---

### Step 2: Install System Dependencies

sudo apt update  
sudo apt install python3 python3-venv python3-pip ffmpeg -y

---

### Step 3: Create a Virtual Environment

python3 -m venv venv

---

### Step 4: Activate the Virtual Environment

source venv/bin/activate

---

### Step 5: Upgrade pip

pip install --upgrade pip

---

### Step 6: Install Required Packages

pip install fastapi uvicorn

pip install -r requirements.txt

---

### Step 7: Run the Server

uvicorn backend.main:app --reload

---

### Step 8: Open the Application

Open your browser and go to:

http://127.0.0.1:8000

---

## How the System Works

The input video is read frame by frame.  
YOLOv8 detects people in each frame.  
PPE compliance is evaluated.  
Risk score and risk level are calculated.  
Escalation is triggered for repeated violations.  
Bounding boxes and labels are drawn on the video.  
An annotated video is generated for browser playback.  
Logs are stored in an SQLite database.  
The frontend fetches live data from the backend and updates automatically.

---

## Notes

- PPE detection logic is demo-based and can be replaced with a trained PPE detection model.  
- The annotated video is generated after detection completes.  
- The browser reloads the annotated video automatically.  
- Designed for hackathon and educational use.

---

## Future Enhancements

- Real-time webcam or CCTV stream support  
- WebSocket-based live video streaming  
- Advanced analytics charts  
- Mobile-first UI improvements  
- Cloud deployment on AWS, Azure, or GCP  

---

## Author

Developed as a hackathon-ready AI Safety Compliance Monitoring System.
