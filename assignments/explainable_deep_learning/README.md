# Explainable Deep Learning (Grad-CAM & Variants)

**Course:** AIPI 590 – Emerging Trends in Explainable AI (Fall 2025)  
**Professor:** Dr. Brinnae Bent  
**Author:** Eric Ortega Rodriguez  
**Domain:** Traffic Sign Classification & Explainability  
**Deadline:** October 6, 2025 – 11:30 AM


## Project Overview
This project explores model explainability in computer vision. I use a pretrained **ResNet-50** to classify traffic-sign images and generate heatmaps that show where the model is looking using **Grad-CAM**, **Grad-CAM++**, and **LayerCAM**.

Why this matters: for road-safety applications, we want the model to focus on the **sign face** (text/digits/shape), not the **background**. Visual explanations help verify that.


## Data
Five custom traffic-sign images:

- Stop  
- No Entry  
- Pedestrian Crossing  
- Speed Limit 30  
- Yield

Images are in `assignments/explainable_deep_learning/images/`.  
The model input is resized/normalized by the official ResNet-50 transforms; overlays are resized back to the original image size for visualization.


## Methods Used
- **Grad-CAM** — coarse, region-level focus
- **Grad-CAM++** — tighter focus on class-defining parts (e.g., text/digits)
- **LayerCAM** — crisp edges and shape boundaries (octagon/triangle/rectangle)

Library: [`pytorch-grad-cam`].

Target layer: `model.layer4[-1]` (last conv block).  
Targets: auto top-1 prediction per image (no manual class IDs).


## What I Implemented
- Load pretrained **ResNet-50** (ImageNet weights), no fine-tuning
- Preprocess images with official weights’ transforms
- Generate heatmaps with **Grad-CAM / Grad-CAM++ / LayerCAM**
  
## Key Findings (short)
- Grad-CAM++ focuses most on **text/digits** (e.g., “STOP”, “30”) with less background spill.
- LayerCAM highlights **edges/shape** (octagon, triangle, rectangle) and arrow contours.
- Grad-CAM is broader and sometimes includes **background** (trees/road/bushes).
- Overall the methods agree on *where* the sign is, but emphasize different evidence.
