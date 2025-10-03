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

---

## Requirements

- Python 3.10+
- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- [Supervision](https://github.com/decile-team/supervision) (version 0.8.0)
- OpenCV (recommended: `opencv-python-headless`)
- NumPy, Matplotlib


