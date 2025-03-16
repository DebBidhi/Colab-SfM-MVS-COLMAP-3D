# Colab-SfM-MVS-COLMAP-3D

This repository demonstrates how to perform 3D reconstruction from video using COLMAP within Google Colab. By leveraging Structure-from-Motion (SfM) and Multi-View Stereo (MVS) techniques, the workflow extracts frames from videos, performs sparse and dense reconstructions.

## Purpose

I created this project to alleviate the overheating of my desktop when running long SfM steps that utilize both the NVIDIA GPU and CPU. Depending on the project size, these processes can take anywhere from 10 minutes to 2 hours, potentially causing overheating and hardware damage. By using Google Colab for the intensive computation, I can save my desktop from overheating!!!

## Features

- **COLMAP Installation on Google Colab:** Instructions for installing COLMAP with CUDA support on Colab's T4 GPU, enabling accelerated processing.
- **Video Frame Extraction:** Extract frames from a video using OpenCV for 3D reconstruction.
- **Sparse and Dense Reconstruction:** Guidance for performing both sparse (Structure-from-Motion) and dense (Multi-View Stereo) reconstruction with COLMAP.
- **3D Model Visualization:** Instructions on visualizing the reconstructed 3D model in Meshlab.
- **Google Drive Integration:** Easily save and load your COLMAP environment and reconstruction files to/from Google Drive for future use.

## Getting Started

To get started with this project, follow these steps:

1. **Open the Google Colab Notebook:**
   - Access the provided Google Colab notebook using [this link](#).
   
2. **Setup the Runtime:**
   - Change the runtime type to "GPU" and select the "T4" hardware accelerator for better performance.

3. **Install Dependencies:**
   - Run the provided cells in the notebook to install COLMAP and all necessary dependencies, including the CUDA Toolkit and OpenCV.

4. **Prepare Your Data:**
   - Upload your video file to Google Drive in the specified folder.
   - You can adjust the frame extraction settings depending on the video content and your preferences.

5. **Perform Reconstruction:**
   - Follow the instructions in the notebook to run both sparse and dense reconstruction steps with COLMAP.

6. **Visualize the Model:**
   - After reconstruction, download the 3D model files and view them in Meshlab to examine the result.

## Example

To quickly test the setup, you can use a short video (around 50 seconds) featuring a rotating object or scene. The notebook will guide you through the process of:

1. Extracting frames from the video.
2. Running the sparse and dense reconstruction steps.
3. Visualizing the 3D model generated from your video.

> **Note:** COLMAP installation may take up to 30 minutes. You can find the pre-built version stored in my Google Drive here: [COLMAP Build on Google Drive](https://drive.google.com/drive/folders/1sn09GHg13miCgTLlLwE0FIB4hwySnKIp?usp=drive_link).

> **Important:** The total reconstruction time should not exceed 12-15 minutes, but the bottleneck is the sparse reconstruction phase (SfM), which can take about 8 minutes due to CPU utilization (note that Colab provides 2 CPU cores).

This quick test will confirm that the entire pipeline works as expected, allowing you to move on to more complex or larger projects.

## Dependencies

- Google Colab (for running the notebook)
- COLMAP (for 3D reconstruction)
- CUDA Toolkit (for GPU acceleration)
- OpenCV (for video frame extraction)

## Usage

Follow the instructions in the Google Colab notebook to execute the steps. Adjust the paths, video settings, and other parameters to suit your project’s specific needs.
