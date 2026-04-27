# Bird Detection and Automated Annotation System

An end-to-end computer vision pipeline for bird detection, automated annotation, and species classification.

This system reduces manual annotation effort by integrating detection, labeling, and classification into a unified workflow.

---

## Overview

The system integrates three main components:

- **Detection**: Uses pre-trained YOLO models to localize birds in images  
- **Annotation**: Automatically generates Pascal VOC XML labels from detection results  
- **Classification**: Uses a ResNet50-based model trained on a custom dataset (~50 bird species)  

**Pipeline:** Detection → Annotation → Classification

---

## Key Features

- Automated annotation generation (Pascal VOC XML)
- Configurable bounding box expansion (10–15%)
- Batch image processing
- GUI tool for running the annotation pipeline
- Top-k prediction output for classification

---

## Example Functionality

- Detect multiple birds in complex scenes  
- Generate structured annotation files automatically  
- Perform fine-grained species classification  

---

## Technical Stack

- Python  
- PyTorch (ResNet50-based classification)  
- YOLO (pre-trained object detection)  
- OpenCV / PIL (image processing)  
- Tkinter (GUI interface)  

---

## Project Structure

    code/
    ├── annotation.py      # YOLO-based detection and XML generation
    ├── classifier.py      # ResNet50-based image classification
    ├── gui.py             # GUI for annotation tool
    ├── class_names.json   # internal label mapping used by the classifier
    ├── cat_to_name.json   # human-readable labels for UI display
    
---

## Notes

- Detection uses pre-trained YOLO models for efficiency  
- Classification model was trained on a curated dataset (~50 species)  
- The system focuses on practical pipeline integration rather than model training from scratch
- Model checkpoint is not included due to size constraints, but can be provided upon request.

---

## Demo

A short demonstration video is included in the application materials.

---

## Author

Haochuan Xie
