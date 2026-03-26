# Pothole Detection and Depth Analysis using Deep Learning

This project presents an end-to-end computer vision system for detecting potholes in road images and estimating their depth using deep learning models. The system integrates transformer-based object detection with depth estimation to assess road damage severity and potential vehicle impact.

---

## Overview

The pipeline combines object detection and depth estimation to move beyond simple detection and provide actionable insights. Each detected pothole is analyzed to estimate its depth, categorize severity, and assign an impact rating.

---

## Features

* Pothole detection using RF-DETR (transformer-based object detection)
* Depth estimation using Depth-Anything (HuggingFace)
* Impact rating system (scale of 1 to 10)
* Severity categorization (SAFE, CAUTION, DANGEROUS)
* Visualization outputs including:

  * Depth heatmaps
  * Overlay bounding boxes with labels
  * 3D depth surface plots
  * Cross-sectional analysis
* Batch processing support for multiple images
* Detailed textual reports for each pothole

---

## Tech Stack

* Python
* PyTorch
* Transformers (HuggingFace)
* RF-DETR
* OpenCV
* Matplotlib
* Roboflow (dataset and annotations)

---

## Workflow

1. Train RF-DETR model on a pothole dataset
2. Perform inference to detect potholes in images
3. Generate depth maps using a pretrained depth estimation model
4. Extract depth information within detected bounding boxes
5. Compute estimated depth and assign severity category
6. Generate visualizations and analytical reports

---

## Dataset

* Source: Roboflow
* Format: COCO
* Custom pothole dataset used for training and evaluation

---

## Performance

| Metric    | Value |
| --------- | ----- |
| Precision | 0.801 |
| Recall    | 0.646 |
| mAP@50    | 0.737 |
| mAP@50-95 | 0.440 |

---

## How to Run

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Run the notebook or script

```bash
python main.py
```

### 3. Provide input images

* Supports both single and batch image processing
* Outputs include detection results, depth maps, and reports

---

## Output

The system provides:

* Bounding box detections with confidence scores
* Estimated depth (in cm)
* Severity category
* Impact rating
* Visual plots and analysis

---

## Notes

* Model weights are not included due to size limitations
* Update the weights path before running inference
* Designed for research and demonstration purposes

---

## Author

Somiya Namdeo
