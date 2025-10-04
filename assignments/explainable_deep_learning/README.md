## Explainable Deep Learning (Grad-CAM & Variants)

**Course:** AIPI 590 – Emerging Trends in Explainable AI (Fall 2025)  
**Professor:** Dr. Brinnae Bent  
**Author:** Eric Ortega Rodriguez  
**Case Domain:** Traffic Sign Classification & Explainability  
**Deadline:** October 6, 2025 – 11:30 AM  

### Project Overview
This project explores model explainability in **computer vision** using pretrained deep learning models.  
The goal is to visualize what regions a model focuses on when classifying **road signs**, a safety-critical task for autonomous vehicles.

### Dataset
Five custom traffic sign images were used:
- 🛑 Stop  
- 🚫 No Entry  
- 🚸 Pedestrian Crossing  
- ⚠️ Yield  
- 🏁 Speed Limit 30  

All images are stored in the `/images` folder and resized to **224×224 px** for model input.

### Implementation Summary
1. **Model:** Pretrained ResNet-50 (`torchvision.models.resnet50`)  
2. **Explainability Methods:** Grad-CAM, Grad-CAM++, Score-CAM (using `pytorch-grad-cam`)  
3. **Visualization:** Overlay heatmaps highlighting regions of attention  
4. **Output:** Saved in `/results`

