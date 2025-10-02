# Explainable Deep Learning Assignment

This assignment explores **explainability in deep learning models** using Grad-CAM and its variants. The goal is to visualize where models focus their attention when making predictions.


## Folder Structure
assignments/explainable_deep_learning/
├── explainable_deep_learning.ipynb   # Colab notebook (main analysis)
├── images/                           # Input test images (at least 5)
├── results/                          # GradCAM visualizations
└── README.md                         # Assignment description

## Task
- Select a pretrained deep learning model (**ResNet-50** is used here).
- Load at least **5 test images** from the `images/` folder.
- Apply **three explainability methods**:
  - Grad-CAM
  - Grad-CAM++
  - XGradCAM (or another variant)
- Save and compare the heatmaps in the `results/` folder.
- Provide a short reflection on the insights gained.
