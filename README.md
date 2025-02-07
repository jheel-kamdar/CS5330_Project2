# CS 5330 - Pattern Recognition and Computer Vision – Project 2  
## Content-Based Image Retrieval (CBIR)  

### **Authors:**  
- **Adit Shah**  
- **Jheel Kamdar**  

---

## **Project Overview**  
This project implements a **Content-Based Image Retrieval (CBIR) system** using various feature extraction and similarity matching techniques. The system retrieves the most similar images from a database given a target image. The implemented methods include:  

- **Baseline Matching** – Uses a **7×7 center patch** and compares using **Sum of Squared Differences (SSD)**.  
- **Histogram Matching** – Extracts **color histograms** and compares using **Histogram Intersection**.  
- **Multi-Histogram Matching** – Computes histograms from different **spatial regions** for improved accuracy.  
- **Texture & Color Matching** – Uses **Sobel gradients, GLCM, and LBP** to combine texture and color analysis.  
- **Deep Network Embeddings** – Uses **ResNet18 embeddings** to find semantically similar images.  
- **Custom Feature (Depth-Based Matching)** – Extracts **depth-aware RGB histograms** to focus on foreground objects.  

---

## **Development Environment**  
- **Operating System:** macOS 
- **IDE Used:** Visual Studio Code 
- **Dependencies:**  
  - OpenCV  
  - C++ Standard Libraries  
  - ONNX Runtime (for deep learning models)  
  - ResNet18 Pretrained Model  
---
## Time Travel days used: 0 
---

## **Instructions for Running Executables**  
- Image_matcher1,2,3.cpp has the code for first 3 tasks.
- image-matcher.cpp has tasks 4,5,6 and face detection extension
- CIBR_analysis.cpp has task 7 
- tetxture_analysis.cpp has FFT extension 
- DNN_exmaple.cpp is an extension
- feature_Extractor will give the features.csv

### **1. Compiling the Code**  
Ensure **CMake** is installed and then compile using:  
```bash
mkdir build
cd build
cmake ..
make

./image-matcher <target_image> <database_directory> <feature_type> <top_N_results> <matching_method>

