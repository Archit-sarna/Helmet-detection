# Helmet-detection

## Description
This repository contains code for a helmet detection system using YOLOv3 (You Only Look Once) for object detection and a pre-trained CNN (Convolutional Neural Network) model for helmet classification. The system can process video input, identify individuals on motorcycles, locate their helmets, and determine whether they are wearing a helmet or not. If a rider is detected without a helmet, the system captures a frame from the video as evidence.

## Features
- Real-time helmet detection in video streams.
- Classification of helmet-wearing status (helmet or no-helmet) using a pre-trained CNN model.
- Captures frames when a rider is detected without a helmet.
- CUDA support for faster object detection using the GPU.
- Video output with detected objects and helmet classification.

## About Data
The system uses two main components for helmet detection:

1. YOLOv3 Object Detection Model:
   - Weight file: `yolov3-custom_7000.weights`
   - Configuration file: `yolov3-custom.cfg`
   - These files contain the YOLOv3 model pre-trained on a custom dataset, which includes helmet detection.

2. Helmet Classification Model:
   - Model file: `helmet-nonhelmet_cnn.h5`
   - The classification model is a pre-trained Convolutional Neural Network that determines whether a detected helmet is worn or not.

The sample video file is located at `sample/1.mp4`. The system processes this video for helmet detection and classification.

## Instructions
1. Ensure you have the required Python packages installed, including OpenCV, NumPy, imutils, and TensorFlow.
2. Download the YOLOv3 weight and configuration files and place them in the same directory as the code.
3. Download the helmet classification model (`helmet-nonhelmet_cnn.h5`) and ensure it is in the same directory as the code.
4. Update the input video source by modifying the `cap = cv2.VideoCapture('sample/1.mp4')` line. You can replace `'sample/1.mp4'` with the path to your desired video source.
5. Set your desired confidence thresholds for object detection and classification in the code.
6. Run the code and observe real-time helmet detection, classification, and the capture of frames when a rider is detected without a helmet.

## Conclusion
This helmet detection system combines YOLOv3 for object detection with a pre-trained CNN model for helmet classification. It is capable of real-time helmet detection in video streams and can capture frames as evidence when a rider is detected without a helmet. Please note that the system's accuracy may vary depending on the quality of the input video and the trained models. Further improvements and customization can be made to enhance the system's performance and adapt it to specific use cases.
