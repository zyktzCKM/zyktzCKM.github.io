---
title: Welcome to My Dataset Showcase
layout: default
---

# 👋 CKMImageNet Dataset Showcase
This is my GitHub Pages site for displaying the [CKMImageNet Dataset](https://github.com/zyktzCKM/CKMImageNet).

# ❓ What Is CKM
CKM is a site-specific database that provides location-specific channel knowledge. It offers a promising method to enable environment-awareness — this facilitates or even avoids sophisticated real-time CSI acquisition or redundant environment sensing.

## 📚 Dataset Introduction
CKMImageNet is a dataset bridging the gap between AI and environment-aware wireless communication environment-aware research for 6G systems. It integrates location-specific channel data, multi-resolution channel knowledge images and physical environmental maps, with both numerical and visual representations. 

## 🚀 Key Features
1. CKMImageNet is constructed through physics-based ray-tracing simulations using advanced tools like Wireless Insite and Sionna.
2. CKMImageNet provides multi-dimensional channel knowledge spanning channel gain, AoA, AoD, propagation delay, and other key parameters.
3. CKMImageNet introduces normalized, spatially consistent and location-specific grayscale images (32 × 32, 64 × 64, 128 × 128 pixels) encoding multi-dimensional channel parameters.
4. CKMImageNet pioneers the tight coupling of numerical channel data, binary obstacle matrices, and grayscale CKMs into a unified framework.

## 📊 Data Presentation

![CKM Dataset Overview](assets/images/dataset_01.png)
*Figure: Schematic diagram of CKMImageNet dataset structure (from dataset_01.png)*


## ❓ How to use the CKMImageNet dataset?

### 1. Normalization Rules for Image Data
- Channel gain maps: Normalized from **-250 dB ~ -50 dB** to the range of **0 ~ 1**.
- AoA/AoD maps: Normalized from **-200° ~ 180°** to the range of **0 ~ 1**.

> Note: The value of `-250 dB` for gain maps and `-200°` for angle maps are practically unreachable. They are specifically used to mark **building areas** (distinguishing valid channel data from obstacle regions).

### 2. Usage of Image Data
Due to the large volume of the raw dataset, we only provide a simple example to demonstrate how to process and utilize the raw CKM data. The following code includes three core steps: reading the raw file, extracting key channel data, and generating an NPZ file (for efficient data storage) or converting the data directly into visual images.



## 🔗 Access the Dataset
- GitHub Repository: [zyktzCKM/CKMImageNet](https://github.com/zyktzCKM/CKMImageNet)
