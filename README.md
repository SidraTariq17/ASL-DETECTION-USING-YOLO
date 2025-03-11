# ASL Detection Using YOLOv8

## Repository Overview
This repository contains the code, model weights, and documentation for a **real-time American Sign Language (ASL) detection system** using **YOLOv8**. The system leverages computer vision and deep learning to detect and classify ASL gestures from images, providing a user-friendly interface via **Streamlit**.

---

## Files in the Repository

### 1. **`ASL.py`**
   - **Description**: The main script for the ASL detection system.
   - **Functionality**:
     - Loads the YOLOv8 model (`best.pt`).
     - Processes uploaded images using OpenCV.
     - Displays predictions (bounding boxes and labels) via Streamlit.
   - **Usage**: Run this script to launch the Streamlit web app.

### 2. **`best.pt`**
   - **Description**: The trained YOLOv8 model weights.
   - **Purpose**: Used for detecting ASL gestures in images.
   - **Tracking**: Tracked using **Git LFS** to manage large file storage.

### 3. **`.gitattributes`**
   - **Description**: Configuration file for Git LFS.
   - **Purpose**: Ensures large files like `best.pt` are tracked by Git LFS.

### 4. **`ASL Report.pdf`**
   - **Description**: A detailed report documenting the project.
   - **Contents**:
     - Introduction and problem statement.
     - Theoretical details of the YOLOv8 model.
     - Training and optimization process.
     - Simulation results and performance evaluation.

### 5. **`Notebooks/`**
   - **Description**: Contains Jupyter notebooks used for training and experimentation.
   - **Contents**:
     - Notebooks for dataset preprocessing, model training, and evaluation.
     - **Note**: The `noname` notebook was deleted as it was no longer needed.

---

## How to Use

### 1. **Set Up the Environment**
   - Install dependencies:
     ```bash
     pip install streamlit opencv-python numpy ultralytics
     ```

### 2. **Run the Streamlit App**
   - Launch the ASL detection system:
     ```bash
     streamlit run ASL.py
     ```

### 3. **Upload an Image**
   - Use the Streamlit interface to upload an image (JPG, PNG, or JPEG).
   - The system will process the image and display the detected ASL gestures with bounding boxes and labels.

---

## Training and Model Optimization
- The YOLOv8 model was trained on **two datasets**:
  1. **Dataset 1**: 85 epochs for initial training.
  2. **Dataset 2**: 30 additional epochs for fine-tuning.
- The best-performing model (`best.pt`) was selected after **115 epochs**, achieving optimal accuracy and robustness.

---

## Performance
- The model achieves high confidence scores (e.g., 0.80–0.83) for accurate gesture detection.
- Performance metrics (mAP, precision, recall) are documented in the **`ASL Report.pdf`**.

