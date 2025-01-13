# PoseLift: Exploring Pose-Based Anomaly Detection for Retail Security: A Real-World Shoplifting Dataset and Benchmark
This directory contains the PoseLift dataset published in WACV 2025 conference.
## Overview
PoseLift is a dataset created specifically for detecting shoplifting behaviors using pose-based anomaly detection techniques. Built in collaboration with a retail store, PoseLift captures real-world shopping and shoplifting behaviors while addressing key challenges such as privacy concerns, data scarcity, and model biases. PoseLift dataset includes bounding box, person ID, and pose annotations, along with frame-level labels for shoplifting, categorizing all frames into two groups: normal behavior or shoplifting.

## Dataset Description
### Features
-**Privacy-Preserving**: The dataset includes pose sequences derived from CCTV footage, with anonymized human identities and no raw pixel-level video data, ensuring compliance with privacy regulations.
-**Real-World Data and Diverse Shoplifting Behaviors**: Recorded in a retail store with various camera views, the footage includes both normal shopping and shoplifting behaviors. The dataset captures a broad range of shoplifting scenarios in different locations across the store. The shoplifting behaviors demonstrated in these videos included actions such as placing items into pockets, placing them in bags, and hiding them under shirts, jackets, and pants.
-**Pose-Based Annotations**: PoseLift provides bounding boxes, person IDs, and human pose annotations instead of raw videos to support privacy-preserving shoplifting detection.
- **Camera Views**: 6 indoor cameras (C1 to C6) from various aisles and locations.
- **Shoplifting and Shopping Instances**: The dataset consists of 153 files, including 43 instances of shoplifting and 110 instances of regular shopping activities. These were captured from various angles and locations to ensure diverse scenarios.

## Data Processing
- **Video Lengths & Frame Rates**: Videos range from a few seconds to over 5 minutes, with a resolution of 1920x1080 and a frame rate of 15 fps.
- **Pose Data Extraction**: Anonymized pose data is extracted using state-of-the-art models like YOLOv8 for object detection, ByteTrack for person tracking, and HRNet for human pose estimation.
- **Data Modifications**: To address occlusions caused by store shelves, specific areas of interest for each camera were defined. Missing poses were interpolated, and data smoothing was applied for continuity.

## Benchmarking

We provide benchmark results for top pose-based anomaly detection models tested on the PoseLift dataset.

| Methods          | AUC-ROC | AUC-PR| EER |
|------------------|---------|-------|-----|
| STG-NF         |    67.46   | 84.06        | 0.39   |
|TSGAD           |   63.35    |  39.31       | 0.41    |
| GEPC          |   60.61    |  50.38       | 0.38  |

## Usage
PoseLift is designed for research on shoplifting detection, particularly in real-world retail settings. Researchers can use the dataset for:
•	Training and evaluating pose-based anomaly detection models.
•	Developing privacy-preserving systems for surveillance and security in retail environments.
•	Exploring methods for detecting complex behaviors like shoplifting in natural settings.

## Citation
If you use PoseLift in your research, please cite:

## Contact
If you have any questions or need assistance, please contact the authors at nrashvan@charlotte.edu.
