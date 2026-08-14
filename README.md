# LiDAR-Camera Data Fusion Pipeline

![Visual Fusion Pipeline in Action](output/out_2.gif)

This repository contains a Python implementation of an end-to-end multi-sensor fusion pipeline. Using the KITTI tracking dataset, the project projects 3D LiDAR point clouds onto 2D camera images to achieve spatial synchronization between independent sensors.

## Features
* **3D-to-2D Projection:** Computes homogeneous transformations using raw translation vectors and intrinsic/extrinsic calibration matrices.
* **Spatial Filtering:** Implements point-cloud clipping to isolate spatial data strictly within the camera's field of view (frustum), minimizing downstream computational overhead.
* **Visualization:** Generates overlaid multi-modal images mapping depth intensity onto 2D camera frames.

## Technology Stack
* **Language:** Python, C++, CUDA
* **Libraries:** NumPy, OpenCV, Matplotlib
* **Environment:** Google Colab / Visual Studio Code
* **Dataset:** KITTI Tracking Dataset

## Repository Structure
* `notebooks/`: Contains the primary development notebook with step-by-step projection geometry.
* `data/`: Local directory for KITTI calibration, image, and velodyne data streams.

## Getting Started

### Prerequisites
Ensure you have the required libraries installed:
```bash
pip install numpy opencv-python matplotlib

### Dataset Setup
1. Download the calibration files and object data from the [KITTI Tracking Benchmark](https://www.cvlibs.net/datasets/kitti/eval_tracking.php).
2. Place the unzipped sensor streams into the `data/` directory.

### Running the Pipeline
 To run the cells sequentially, upload it directly to Google Colab.
