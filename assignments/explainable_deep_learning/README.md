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

## Methods Used
- **Grad-CAM** — coarse, region-level focus
- **Grad-CAM++** — tighter focus on class-defining parts like on text/digits
- **LayerCAM** — crisp edges and shape boundaries (octagon/triangle/rectangle)

## What I Implemented
- Load pretrained **ResNet-50** (ImageNet weights), no fine-tuning
- Preprocess images with official weights’ transforms
- Generate heatmaps with **Grad-CAM / Grad-CAM++ / LayerCAM**
  
## Key Findings (short)
- Grad-CAM++ focuses most on **text/digits** (e.g., “STOP”, “30”) with less background spill.
- LayerCAM highlights **edges/shape** (octagon, triangle, rectangle) and arrow contours.
- Grad-CAM is broader and sometimes includes **background** (trees/road/bushes).
- Overall the methods agree on *where* the sign is, but emphasize different evidence.
