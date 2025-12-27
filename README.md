# industrial-surface-defect-detection
# Industrial Surface Defect Detection (Classical Computer Vision)

This repository presents a **classical image processing–based approach** for detecting surface defects in industrial metal components.  
The project was developed as part of an academic course and focuses on building an interpretable and lightweight defect detection pipeline.

---

## 📌 Problem Definition

In industrial manufacturing, surface defects such as scratches, deformations, and irregularities directly affect product quality and customer satisfaction.  
In many production environments, surface inspection is still performed manually, which leads to:

- Operator fatigue  
- Subjective evaluations  
- Low repeatability  
- Time inefficiency  

The main objective of this project is to **automatically detect surface defects** on raw metal surface images using classical computer vision techniques.

---

## 📂 Dataset

- Total images: **10**
- Images belong to the **same industrial metal component**
- Captured under **different angles and lighting conditions**

Using the same product under varying conditions allows a more controlled comparison of algorithmic behavior.

---

## 🧠 Previous Methods (Baseline)

In the first stage, classical image enhancement techniques were applied to improve image quality:

- **Gaussian Filter** – Noise reduction  
- **Sobel Operator** – Edge detection  
- **Histogram Equalization** – Contrast enhancement  

These methods improve visual quality but **do not provide automatic defect localization**.

---

## 🚀 Proposed Method

To address this limitation, a **multi-stage defect detection pipeline** is proposed.

### Pipeline Steps:
1. **CLAHE (Contrast Limited Adaptive Histogram Equalization)**  
   Improves local contrast on metallic surfaces.
2. **Median Filtering**  
   Suppresses scratch- and spot-type noise while preserving structures.
3. **Adaptive Thresholding**  
   Separates potential defect regions from the background.
4. **Morphological Operations**  
   Cleans the defect mask and removes small artifacts.
5. **Contour Analysis**  
   Automatically detects and localizes surface defects.

All steps are applied sequentially as **a single integrated method**.

---

## 📊 Results

- Surface defects are successfully separated from the background.
- Defect regions are automatically localized using bounding boxes.
- The proposed method provides **direct defect detection**, unlike baseline enhancement-only methods.

---



