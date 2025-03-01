# Solar Panel Detection using YOLOv8 and Supervision Metrics

This repository contains the full implementation of our solar panel detection system based on the research paper:

> **A solar panel dataset of very high resolution satellite imagery to support the Sustainable Development Goals**  
> Clark, C.N. & Pacifici, F. (2023)  
> [DOI: 10.1038/s41597-023-02539-8](https://doi.org/10.1038/s41597-023-02539-8)

The code solves the following tasks:
- Splitting the dataset into 80% train, 10% validation (from training), and 10% test.
- Training a YOLOv8 model (using Ultralytics) for solar panel detection.
- Demonstrating validation loss convergence over 50 epochs.
- Predicting solar panels on test images and visualizing results with ground truth (green) and predictions (blue).
- Computing evaluation metrics using supervision metrics and a custom mAP@50 implementation.
- Generating a table of Precision, Recall, and F1-scores for various IoU ([0.1, 0.3, 0.5, 0.7, 0.9]) and confidence thresholds ([0.1, 0.3, 0.5, 0.7, 0.9]).

---

## Directory Structure


*Explanation of the YOLOv8 Directory Structure:*  
- The `dataset.yaml` file defines the dataset path (here `/workspace/deepfake/yolov8`) and specifies the subdirectories for training, validation, and testing images as well as the corresponding labels.  
- The `yolov8` folder contains three subfolders:  
  - `train`: Contains `images` and `labels` used for training.  
  - `val`: Contains `images` and `labels` used for validation.  
  - `test`: Contains `images` and `labels` used for testing and evaluation.  
- The `runs_solar` folder holds all the training outputs, including logs and saved model weights.
- Two Jupyter Notebook files, `data_exploration.ipynb` and `yolov8.ipynb`, provide additional insights and the step-by-step implementation of the data processing and YOLOv8 training pipeline.
- The `fundamental_functions.ipynb` computes IoU and calculates Average Precision (AP) using Pascal VOC 11 point interpolation, COCO 101-point interpolation method and Area under Precision-Recall Curve. It also 
  compares the AP50 (Average Precision at IoU 0.5) computed by all 3 above mentioned methods.

---

## Requirements

- Python 3.10+
- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- [Supervision](https://github.com/decile-team/supervision) (version 0.8.0)
- OpenCV (recommended: `opencv-python-headless`)
- NumPy, Matplotlib


