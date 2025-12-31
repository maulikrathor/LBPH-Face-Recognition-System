LBPH Face Recognition System
Project Overview
This project implements a Face Recognition System using the Local Binary Patterns Histograms (LBPH) algorithm provided by OpenCV.

Unlike simple face detection (which finds a face in an image), this system performs face recognition, meaning it can identify who the person is by learning from a labeled dataset of facial images. It is robust against changes in lighting and facial expressions.

Methodology
Data Ingestion: The system automatically traverses a dataset directory structure where folders are named after the subjects (e.g., train_data/Elon_Musk/).

Label Encoding: Each person is assigned a unique integer label (e.g., 0, 1, 2) which is mapped to their name.

Training: The cv2.face.LBPHFaceRecognizer is trained on grayscale images to learn unique texture patterns (histograms) for each face.

Prediction: The trained model takes unseen test images, predicts the identity, and provides a confidence score (lower score indicates a better match).
