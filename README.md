# Underwater Image Registration and Photomosaicing

This project focuses on **underwater image registration** and **photomosaicing** using low-contrast datasets inspired by the work of *Pizarro and Singh (2003)* in _IEEE Journal of Oceanic Engineering_.  
It explores robust feature matching, homography estimation, and global alignment techniques to reconstruct large-scale underwater mosaics.

---

## 🌊 Project Overview

Due to **light attenuation** and **backscatter**, underwater imagery often suffers from low contrast, uneven illumination, and limited visibility.  
This project implements a robust **image registration pipeline** that compensates for these challenges and builds a coherent mosaic from multiple underwater images.

### Key Objectives:
1. **Enhance Robustness of Image Matching**
   - Normalize images before matching to handle nonuniform lighting.
   - Use RANSAC for outlier rejection.
2. **Homography Estimation**
   - Compute transformations between overlapping images using **Levenberg–Marquardt optimization**.
3. **Global Mosaic Construction**
   - Construct a global factor-graph representation of image connectivity.
   - Optimize using **GTSAM** to refine image poses and covariance structure.
4. **Extended Dataset**
   - Apply to both small subsets (6 images) and larger collections (29+ images) to evaluate scalability.

---

## 🧠 Dataset

**Skerki Dataset** – [Google Drive Link](https://drive.google.com/drive/folders/1AtvT65txGIgAG23NRs3EkvDET036a81O?usp=sharing)

- Consists of images captured near the *Roman shipwreck site of Skerki Bank*.
- Two subsets:
  - **6-Image Subset:** for initial pairwise registration.
  - **29-Image Set:** for large-scale mosaicing experiments.

---

## ⚙️ Implementation Details

- **Language:** Python 3  
- **Main File:** `underwater_image_registration.ipynb`
- **Libraries Used:**
  - `OpenCV` – Feature detection, matching, and homography estimation.
  - `NumPy`, `Matplotlib` – Numerical processing and visualization.
  - `GTSAM` – Global optimization using factor graphs.
  - `SciPy` – Levenberg–Marquardt solver for homography refinement.

---


## 📊 Results

- Successfully matched non-sequential underwater images under low lighting.
- Achieved consistent alignment using robust optimization.
- Constructed mosaics with reduced ghosting and improved edge alignment.
- Demonstrated factor-graph–based optimization for pose refinement.

---

## 🧾 Reference Paper

**Pizarro, O. & Singh, H. (2003).**  
“_Toward Large-Area Mosaicing for Underwater Scientific Applications._”  
*IEEE Journal of Oceanic Engineering, 28(4), 651–672.*  


---


## 📘 References

- [Pizarro & Singh, 2003 – IEEE JOE Paper]
- [GTSAM Library](https://gtsam.org/)
- [OpenCV Documentation](https://docs.opencv.org/)
