# AI Safety PPE Detection (Simple Hackathon Version)

## Tech Stack
- Python, FastAPI
- YOLOv8
- OpenCV
- HTML, CSS, Bootstrap

## How to Run
1. Install requirements: pip install -r requirements.txt
2. Place PPE YOLO model in model/yolov8_ppe.pt
3. Place demo video in video/demo.mp4
4. Run backend: uvicorn backend.main:app --reload
5. Open frontend/index.html in browser
6. Open frontend/dashboard.html to see logs