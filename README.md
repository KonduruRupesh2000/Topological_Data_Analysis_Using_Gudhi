
# Topological Data Analysis for Image Segmentation

## Introduction
Skin lesions represent unusual changes in the skin that may arise from various causes, such as infections, allergic reactions, or conditions like acne and eczema. Early detection and segmentation of skin lesions are critical, particularly in identifying conditions like melanoma, where timely treatment improves outcomes. 

This project leverages **Topological Data Analysis (TDA)** as an innovative approach to improve image segmentation accuracy. By studying the shape and structure of data, TDA, through techniques like persistent homology, enhances the segmentation process by identifying critical topological patterns within an image while filtering noise.

## Features
- Implements **Intersection over Union (IoU)** and **Pixel Accuracy** as performance metrics.
- Demonstrates the effectiveness of **persistent homology** for accurate segmentation.
- Utilizes the **HAM10000 dataset**, a comprehensive collection of dermatoscopic images, for training and evaluation.

## Dataset
The project uses the **HAM10000 dataset**, which includes 10,015 dermatoscopic images with segmentation masks. These masks help delineate lesions from healthy skin, enabling effective training and evaluation of machine learning models.

## Problem Statement
In traditional approaches, methods like `np.argmin()` were used to find pixel values corresponding to birth and death values in persistence diagrams. This introduced ambiguity and inaccuracies due to the lack of spatial arrangement awareness.

## Proposed Solution
This project resolves the above issues by:
1. Using **birth and death indices** directly from GUDHI's `regular_cofaces`.
2. Mapping these indices to pixel coordinates with `np.unravel_index`, ensuring correct associations between persistence values and pixel locations.
   
This method improves segmentation reliability and accuracy.

## Results
| Metric             | Traditional Approach | Proposed Approach |
|--------------------|-----------------------|-------------------|
| **IoU**           | 0.6737               | 0.6901           |
| **Pixel Accuracy** | 0.8747               | 0.8875           |

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/tda-image-segmentation.git
