---
title: Welcome to CKMImageNet Showcase
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

Below, we present a set of multi-type data for a specific environment — these data are visualized as **heatmaps** to intuitively convey the information in the images.  

Note that in our actual dataset repository, the data is provided in the form of **grayscale images**. This format is chosen because grayscale images exclude any extra irrelevant information, making them ready for direct use in your development or training workflows.
<div align="center">
  <img src="assets/images/dataset_01.png" width="600" alt="CKM Dataset Overview">
</div>

## ❓ How to use the CKMImageNet dataset?

### Normalization Rules for Image Data

- Channel gain maps: Normalized from **-250 dB ~ -50 dB** to the range of **0 ~ 1**.
  
- AoA/AoD maps: Normalized from **-200° ~ 180°** to the range of **0 ~ 1**.

> Note: The value of `-250 dB` for gain maps and `-200°` for angle maps are practically unreachable. They are specifically used to mark **building areas** (distinguishing valid channel data from obstacle regions).

### Usage of Image Data for AI Training Tasks

Leveraging CKMImageNet’s large-scale, multi-dimensional, and spatially consistent image data enables diverse AI training tasks (aligned with the case studies), addressing key challenges in environment-aware 6G systems, following are some examples:

- **CKM Denoising**  
  The image dataset (encoding channel gain, AoA/AoD, etc.) trains AI models (e.g., diffusion models, GANs) to filter noise from real-world CKM data (corrupted by sensor imperfections or environmental interference). By learning from CKMImageNet’s noise-free, environment-aligned image features, these models recover true channel characteristics—improving CKM accuracy for system optimization.

- **CKM Inpainting**  
  For missing CKM regions (e.g., safety-restricted areas), the image data supports training conditional models (e.g., conditional diffusion models) to impute missing information. With CKMImageNet’s fused obstacle maps (environmental context like building layouts), these models restore large missing regions (e.g., entire city blocks) more effectively than traditional methods (KNN, Kriging).

- **CKM Super-Resolution**  
  The multi-resolution image data (32×32/64×64/128×128) trains super-resolution models (e.g., ResNet-based networks) to upscale low-resolution CKM images (from coarse measurements) to high-resolution maps. This enhances spatial detail critical for high-precision tasks (e.g., beamforming in ultra-massive MIMO systems).

- **CKM Generation**  
  Generative models (trained on the image dataset) synthesize high-quality CKMs for environments with sparse measurements (e.g., complex urban areas). By integrating environmental-channel causal relationships from CKMImageNet, these models enable CKM expansion for 6G scenario research.

![CKM Usage Overview](assets/images/datausage.png)

## 📧 Contact
This Dataset is developed by Southeast University and Purple Mountain Laboratories. For any further information, please contact Prof. Yong Zeng yong_zeng@seu.edu.cn; Mr. Zijian Wu wuzijian@seu.edu.cn

## 🔗 Access the Dataset
- GitHub Repository: [zyktzCKM/CKMImageNet](https://github.com/zyktzCKM/CKMImageNet)

## 🌐 Our related works

[R1]Y. Zeng et al., "A Tutorial on Environment-Aware Communications via Channel Knowledge Map for 6G," in IEEE Communications Surveys & Tutorials, vol. 26, no. 3, pp. 1478-1519

[R2] X. Xu and Y. Zeng, "How Much Data Is Needed for Channel Knowledge Map Construction?" in IEEE Transactions on Wireless Communications, vol. 23, no. 10, pp. 13011-13021, Oct. 2024.

[R3]Z. Wu, D. Wu, S. Fu, Y. Qiu and Y. Zeng, "CKMImageNet: A Dataset for AI-Based Channel Knowledge Map Toward Environment-Aware Communication and Sensing," in IEEE Transactions on Communications, vol. 73, no. 12, pp. 14430-14443

[R4] D. Wu, Z. Wu, Y. Qiu, S. Fu, and Y. Zeng, “CKMImageNet: A comprehensive dataset to enable channel knowledge map construction via computer vision,” in 2024 IEEE/CIC International Conference on Communications in China (ICCC Workshops), 2024, pp. 114–119.

[R5] K. Li, P. Li, Y. Zeng, and J. Xu, “Channel knowledge map forenvironment-aware communications: EM algorithm for map construction,” in 2022 IEEE Wireless Communications and Networking Confer-ence (WCNC), 2022, pp. 1659–1664.

[R6] S. Fu, Z. Wu, D. Wu and Y. Zeng, "Generative CKM Construction Using Partially Observed Data with Diffusion Model," 2025 IEEE 101st Vehicular Technology Conference (VTC2025-Spring), Oslo, Norway, 2025, pp. 1-5

[R7] D. Wu, Y. Zeng, S. Jin, and R. Zhang, “Environment-aware hybrid beamforming by leveraging channel knowledge map,” IEEE Trans. Wireless Commun., 2023.

[R8] Z. Xu, Z. Zhou, D. Wu and Y. Zeng, "Channel Knowledge Map-Enhanced Clutter Suppression for Integrated Sensing and Communication," 2024 IEEE/CIC International Conference on Communications in China (ICCC Workshops), Hangzhou, China, 2024, pp. 90-95.

[R9] Y. Long, Y. Zeng, X. Xu, and Y. Huang, “Environment-Aware Wireless Localization Enabled by Channel Knowledge Map,” IEEE Globecom 2022.

[R10] S. Zeng, X. Xu, Y. Zeng, and F. Liu, “CKM-assisted LoS identification and predictive beamforming for cellular-connected UAV,” IEEE ICC 2023.

[R11] Y. Qiu, D. Wu and Y. Zeng, "CKM-Based Environment-Aware Pilot Reuse and Channel Estimation," 2024 16th International Conference on Wireless Communications and Signal Processing (WCSP), Hefei, China, 2024, pp. 169-174.

[R12] D. Wu, Y. Qiu, Y. Zeng and F. Wen, "Environment-Aware Channel Estimation via Integrating Channel Knowledge Map and Dynamic Sensing Information," in IEEE Wireless Communications Letters, vol. 13, no. 12, pp. 3608-3612, Dec. 2024, doi: 10.1109/LWC.2024.3482357.

[R13] D. Wu and Y. Zeng, "Environment-Aware Coordinated Multi-Point mmWave Beam Alignment Via Channel Knowledge Map," 2023 IEEE International Conference on Communications Workshops (ICC Workshops), Rome, Italy, 2023, pp. 1044-1049, doi: 10.1109/ICCWorkshops57953.2023.10283607.

[R14] Z. Dai, D. Wu, Z. Dong and Y. Zeng, “Prototyping and experimental results for environment-aware millimeter wave beam alignment via channel knowledge map,” in IEEE Transactions on Vehicular Technology, vol. 73, no. 11, pp. 16805-16816, Nov. 2024

[R15] C. Zhang, Z. Zhou, X. Xu, Y. Zeng, Z. Zhang and S. Jin, "Prototyping and Experimental Results for ISAC-based Channel Knowledge Map," in IEEE Transactions on Vehicular Technology, doi: 10.1109/TVT.2025.3545785.

  
