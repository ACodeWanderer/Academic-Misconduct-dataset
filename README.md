# Handwritten Augmentation Pipeline

This repository contains a reproducible preprocessing and augmentation pipeline developed for a research project on handwritten academic content analysis and academic misconduct detection. The code processes scanned or photographed handwritten answer-sheet images and generates controlled, OCR-safe augmented samples that simulate realistic variations observed in student submissions.

---

## Overview

Handwritten datasets are often limited in size and exhibit significant variability in lighting, orientation, ink thickness, paper texture, and noise. To address these constraints, this pipeline expands the dataset using a **padding-first augmentation strategy** that preserves text integrity while introducing natural distortions relevant for real-world evaluation.

The pipeline:
- Works on `.jpg`, `.jpeg`, and `.png` images  
- Adds large uniform padding before any transformation  
- Applies 2–4 randomized augmentation operations  
- Saves augmented images with systematic naming  
- Ensures that all transformations remain safe for OCR and handwriting-feature extraction

This repository makes the full codebase publicly available for reproducibility and further research use.

---

## Features

- **Massive Padding (50% of width & height)**  
  Prevents text clipping during rotation and translation.

- **Random Rotation (±12°)**  
  Mimics camera tilt and notebook misalignment.

- **Translation / Shifting (up to 8%)**  
  Simulates inconsistent cropping or scanning offsets.

- **Brightness & Contrast Adjustment**  
  Models real illumination conditions such as dim rooms, glare, or exposure variations.

- **Gaussian Blur (optional)**  
  Emulates camera
