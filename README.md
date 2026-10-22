# Colonoscopy Polyp Detection

A computer vision project that explores real-time polyp detection in colonoscopy video using YOLO11n. The goal is to provide a visual aid during a procedure by highlighting frames where a polyp is detected and saving those frames for later review.

## Overview

During a colonoscopy, the system processes the camera feed and detects visible polyps. When a detection occurs, it can alert the physician and save the corresponding frame as an image. These saved frames may help the physician revisit findings after the procedure and use them when preparing a report.

This project is an assistive computer vision prototype. It does not replace clinical judgment, medical devices, or a physician's diagnosis.

## Model and training

- **Model:** YOLO11n (YOLO11 nano)
- **Image size:** 640 × 640
- **Task:** Polyp object detection
- **Augmentation:** YOLO augmentations configured from the Ultralytics training options

YOLO11n was selected as a lightweight model for experimentation. Training uses 640-pixel images to retain detail relevant to detecting polyps. The training augmentations are intended to improve robustness to variation in colonoscopy imagery.

## Dataset

The dataset was obtained from Roboflow. The dataset link and related information are provided in the repository's `Dataset` file.

The dataset is already formatted for YOLO, so no annotation-format conversion is required. Refer to the original Roboflow dataset page for its license, citation, and usage conditions.

## Inference workflow

1. Read frames from a colonoscopy video stream or recorded video.
2. Run YOLO11n inference on each frame.
3. Display an alert or visual indication when a polyp is detected.
4. Save the frame associated with a detection for review after the procedure.

The exact alert behavior, confidence threshold, and frame-saving policy depend on the implementation and can be documented here once finalized.

## Intended use

This repository is for computer vision experimentation and research into colonoscopy video assistance. It is not a clinically validated diagnostic system and should not be used as the sole basis for diagnosis or treatment decisions.

## Suggested GitHub topics

`polyp-detection` · `colonoscopy` · `medical-imaging` · `computer-vision` · `object-detection` · `yolo11` · `ultralytics` · `deep-learning` · `roboflow`
