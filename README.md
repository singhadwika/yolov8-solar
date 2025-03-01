# yolov8-solar

# Solar Panel Detection using YOLOv8 and Supervision Metrics

This repository implements a complete pipeline for solar panel detection using high-resolution satellite imagery. The work is based on the research paper:

> **A solar panel dataset of very high resolution satellite imagery to support the Sustainable Development Goals**  
> Clark, C.N. & Pacifici, F. (2023)  
> [DOI: 10.1038/s41597-023-02539-8](https://doi.org/10.1038/s41597-023-02539-8)

---

## Overview

In this project, I:
- **Split the dataset** into an 80-10-10 train-validation-test split (using 10% of training data for validation).
- **Trained a YOLOv8 model** from Ultralytics to detect solar panels.
- **Monitored validation loss** to ensure convergence during training.
- **Visualized predictions** on several test images by overlaying predicted (blue) and ground truth (green) bounding boxes.
- **Computed evaluation metrics**:
  - Calculated mAP@50 using both the supervision library and a custom implementation.
  - Generated a table of Precision, Recall, and F1-scores for various IoU thresholds ([0.1, 0.3, 0.5, 0.7, 0.9]) and confidence thresholds ([0.1, 0.3, 0.5, 0.7, 0.9]).

---
