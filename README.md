Real-Time Object Detection with OpenCV (DroidCam) 📱🎥

This project performs real-time object detection using a webcam (or DroidCam) and a pre-trained SSD MobileNet v3 model trained on the COCO dataset.
Detected objects are displayed live with bounding boxes and labels.

🚀 Features

Real-time object detection

Uses SSD MobileNet v3 (COCO)

Works with DroidCam or any webcam

Displays object name and bounding box

Adjustable confidence threshold

Live video feed

🧠 How It Works

Video is captured from a webcam (DroidCam in this case)

Frames are passed to OpenCV’s DNN module

The model detects objects and returns:

Class ID

Confidence score

Bounding box

Bounding boxes and class names are drawn on the frame

Output is displayed in real time

🛠️ Technologies Used

Python

OpenCV (cv2)

SSD MobileNet v3

COCO Dataset

📦 Requirements

Install the required library:

pip install opencv-python

📁 Required Files

Make sure the following files are in the same directory as your script:

object_detection.py
coco.names
ssd_mobilenet_v3_large_coco_2020_01_14.pbtxt
frozen_inference_graph.pb

▶️ How to Run

Start DroidCam on your phone and connect it to your PC

Run the script:

python object_detection.py


Press Q to quit the application

🎥 Camera Configuration

The script uses DroidCam as the video source:

cam = cv2.VideoCapture(1)


If the camera does not open, try changing the index:

cam = cv2.VideoCapture(0)
cam = cv2.VideoCapture(2)

🎯 Detected Objects

The model can detect 80 objects, including:

Person

Car

Bicycle

Mobile phone

Chair

Dog, cat

Bottle, cup, laptop, etc.

(Full list available in coco.names)

⚙️ Controls
Key	Action
Q	Quit program
📈 Performance Tips

Lower input size for better FPS:

net.setInputSize(300, 300)


Close other apps using the camera (Zoom, Teams, OBS)

🚀 Possible Improvements

Show confidence percentage on screen

Filter detection (e.g. detect only persons)

Save detected frames or video

FPS counter

GUI controls

👤 Author

Houssine Fila
Computer Vision & Data Analytics Enthusiast
