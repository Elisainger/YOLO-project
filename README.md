# Advanced Object Detection and Comparative Study using YOLOv26

Evaluation of YOLO deep learning models for object detection on the VisDrone dataset.  
Course: *Deep Learning for Engineers (CMPE 401), University of British Columbia*

---

## Overview
This project explores object detection using different YOLO models and evaluates their performance through structured experiments.

The workflow includes:
- Training a baseline YOLO model
- Iteratively improving performance (model size, epochs, resolution)
- Comparing multiple YOLO versions (v5, v8, v10, v26)
- Evaluating performance using standard metrics (Precision, Recall, mAP)

---

## Iterative Model Improvements

| Model | Precision | Recall | mAP50 | mAP50-95 |
|------|----------|--------|-------|----------|
| Baseline (YOLO26n, 640, 30ep) | 0.391 | 0.296 | 0.262 | 0.145 |
| Capacity ↑ (YOLO26m, 640, 30ep) | 0.568 | 0.440 | 0.444 | 0.265 |
| Epochs ↑ (YOLO26m, 640, 60ep) | 0.578 | 0.445 | 0.448 | 0.269 |
| Resolution ↑ (YOLO26m, 800, 40ep) | **0.611** | **0.490** | **0.503** | **0.307** |

 Increasing **image resolution** provided the largest improvement, especially for detecting small objects.

---

## Multi-Version YOLO Comparison

| Model | Precision | Recall | mAP50 | mAP50-95 |
|------|----------|--------|-------|----------|
| YOLOv8 | **0.412** | **0.310** | **0.286** | **0.160** |
| YOLOv10 | 0.410 | 0.304 | 0.277 | 0.153 |
| YOLOv26 | 0.384 | 0.303 | 0.266 | 0.145 |
| YOLOv5 | 0.391 | 0.296 | 0.262 | 0.145 |

 **YOLOv8 achieved the best overall performance**, while YOLOv5 was the most efficient.

---

## Key Takeaways
- Increasing model capacity significantly improved performance  
- Increasing epochs yielded only marginal gains  
- Increasing image resolution was the most effective for small-object detection  
- There is a trade-off between **accuracy and computational cost**

---

## Notebook
See `model.ipynb` for full implementation and experiments.
