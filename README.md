# small-bird-detection-YOLOv8-MRF
 A hybrid object detection approach combining YOLOv8 and Markov Random Fields for detecting small, distant birds in wildlife camera trap images.


This project demonstrates a hybrid object detection pipeline developed for wildlife camera-trap image datasets. The system combines the high-speed accuracy of YOLOv8 with the pixel-level precision of Markov Random Fields (MRF) to detect small and distant birds in challenging natural environments.

Problem Statement

Detecting small birds in camera-trap footage is difficult due to image blur, low resolution, and the bird's visual similarity to background elements like branches or leaves. Conventional CNN models struggle to distinguish subtle features in such conditions. This project explores whether traditional probabilistic methods, like MRFs, can assist in localizing fine-grained changes and enhance deep learning performance.

Solution Overview

Step 1: Apply image pre-processing and motion filtering using absolute difference techniques.

Step 2: Use YOLOv8 to detect coarse bounding boxes around probable animals.

Step 3: Refine detection using MRF-based change detection, particularly for small, blurred, or distant birds.

Step 4: Compare performance metrics across methods using recall, precision, and confusion matrix visualizations.

Key Features

Combines classical (MRF) and modern (YOLOv8) detection techniques

Handles dense backgrounds, low-light, and high-blur images

Dataset sourced from Cal Poly Pomona’s Wildlife Research Project

Analysis includes PR curves, confusion matrix, and visual results

Python notebooks provided with visual examples

Directory Structure

small-bird-detection-yolov8-mrf/

MRF.ipynb : Markov Random Field implementation

Abs_Differenceonly.ipynb : Image differencing and motion filtering

abs_difference_with_contour.ipynb : Contour detection from difference images

Animal_DetectionSlides.pptx : Project presentation slides

images/ : Folder with input/output samples (e.g., Figure1.jpg, Figure2.jpg)




Requirements

Python 3.8 or higher

OpenCV

NumPy

YOLOv8 (Ultralytics)

Matplotlib

SciPy
