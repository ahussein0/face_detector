# Face Detector

This project implements real-time face detection using OpenCV and a pre-trained Caffe model. It captures video from your webcam and detects faces in each frame, drawing bounding boxes around detected faces with confidence scores.

## Features

- Real-time face detection from webcam feed
- Uses a pre-trained Caffe model for efficient face detection
- Displays confidence scores for each detected face
- Adjustable confidence threshold

## Prerequisites

Before running this program, make sure you have the following installed:
- Python 3.6+
- OpenCV (cv2)
- imutils
- numpy

You can install the required packages using pip:
pip install opencv-python imutils numpy

## Usage

To run the face detection program:

1. Clone this repository:
git clone https://github.com/ahussein0/face_detector.git
cd face_detector

2. Run the script with the following command:
   python detect_faces_videos.py --prototxt deploy.prototxt --model cafe.caffemodel

3. Optional: Adjust the confidence threshold (default is 0.5):
   python detect_faces_videos.py --prototxt deploy.prototxt --model cafe.caffemodel --confidence 0.7

4. To exit the program, press 'q' while the video window is active.

## How it works

1. The program initializes the video stream from your default webcam.
2. For each frame:
- It resizes the frame and prepares it for the neural network.
- The frame is passed through the Caffe model to detect faces.
- Detected faces are outlined with rectangles, and confidence scores are displayed.
- The processed frame is shown in a window.
3. This process continues until the user presses 'q' to quit.

## Notes

- Ensure your webcam is connected and functioning properly.
- The Caffe model files (`deploy.prototxt` and `cafe.caffemodel`) should be in the same directory as the Python script.
- Adjust the confidence threshold to balance between detection accuracy and false positives.
- Be sure not to open the cafe.caffemodel file. File corruption may occur.


Sources:
caffemodel: https://github.com/opencv/opencv_3rdparty/blob/dnn_samples_face_detector_20170830/res10_300x300_ssd_iter_140000.caffemodel
deploy.prototxt: https://github.com/opencv/opencv/blob/master/samples/dnn/face_detector/deploy.prototxt

Project Link: [https://github.com/ahussein0/face_detector](https://github.com/ahussein0/face_detector)
