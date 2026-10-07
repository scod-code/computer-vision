# Computer Vision Labs

**Artificial Perception module labs covering image processing, classical feature matching, deep learning, and sensor fusion.**

---

## Repository layout

```text
.
├── image-processing/
│   └── Lab_2.ipynb            # Preprocessing: filtering, thresholding, edge detection
├── classical-vision/
│   └── Lab_3.ipynb            # Feature extraction and matching (SIFT, ORB, RANSAC)
├── deep-learning/
│   └── Lab_4.ipynb            # Custom CNN vs VGG16 transfer learning, OOD testing
└── sensor-fusion/
    └── Lab_8.ipynb            # GPS + IMU fusion (averaging, weighted, Kalman filter)
```

Each notebook is self-contained and uses the small set of test images committed alongside it. They were developed in Google Colab.

---

## Lab 3 — Classical feature matching

Visual recognition across strong illumination changes (day/night photos of NTU buildings), comparing SIFT and ORB descriptors with FLANN k-NN matching and RANSAC geometric verification — up to 701 retained ORB inliers on the illumination-variant image pair.

## Lab 4 — Deep learning

Trains a from-scratch CNN and a VGG16 transfer-learning model for animal classification, then probes failure modes with out-of-distribution images (e.g. wolf, lion) to study overconfident predictions.

## Lab 2 — Image processing

Foundational preprocessing pipelines on the provided photographs: Gaussian/median noise removal, global/adaptive/Otsu thresholding, and Sobel/Canny edge detection.

## Lab 8 — Sensor fusion

Fuses noisy GPS and drifting IMU position signals with three strategies — simple averaging, weighted fusion, and a Kalman filter — and compares them on RMSE (in metres, lower is better):

| Method | RMSE |
| --- | --- |
| IMU only | 25.900 m |
| Average fusion | 12.979 m |
| Weighted fusion | 10.427 m |
| GPS only | 2.375 m |
| Kalman fusion | **0.826 m** |

The Kalman filter tracks closely through long GPS dropouts where either sensor alone fails.

---

## Running

Open any notebook in Jupyter or Colab and run top to bottom; OpenCV, TensorFlow/Keras, and matplotlib dependencies are installed from within the notebooks.

---

## Contact

**Author**: Somtochukwu C. Osigwe-Daniel  
**Email**: somtoosigwe1@gmail.com  
**LinkedIn**: [linkedin.com/in/somtoosigwedaniel](https://linkedin.com/in/somtoosigwedaniel)  
**GitHub**: [github.com/scod-code](https://github.com/scod-code)
