# Detection of Violent Behavior Using Neural Networks and Pose Estimation

This repository implements a system for detecting violent behavior in video footage using neural networks and pose estimation. The project combines YOLOv3 for object detection and OpenPose for human pose estimation to analyze actions in real-time or recorded video streams.

![Demo](https://github.com/user-attachments/assets/8b27306f-289a-467b-ab5a-cbd39aa09bf0)



## Features
- **Object Detection**: YOLOv3 is used to detect pedestrians in video frames.
- **Pose Estimation**: OpenPose extracts human body keypoints for activity analysis.
- **Tracking**: Tracks individuals across video frames using Intersection over Union (IoU) matching.
- **Violent Behavior Detection**: Processes pose data to classify and identify violent actions.



## Usage

### 1. Setup YOLOv3
Ensure the YOLOv3 weights, configuration, and class files are downloaded and stored in the `YOLOV3_Files` directory. Run the following script:


### 2. Run Detection and Pose Estimation
Run the main script to process video files:


### 3. Parameters
- `--video_path`: Path to the input video file.
- `--output_path`: Path to save the output video with detections and poses.
- `--confidence_threshold`: Confidence threshold for YOLOv3 detections.
- `--iou_threshold`: IoU threshold for object tracking.

## How It Works

### Object Detection
YOLOv3 is used to detect pedestrians in video frames. Each pedestrian is assigned a unique ID for tracking.

### Pose Estimation
OpenPose extracts keypoints of detected pedestrians, enabling an analysis of body posture and movements.



### Tracking
IoU-based object tracking maintains consistency of IDs across frames, allowing the system to follow individuals over time.

### Violent Behavior Detection
By analyzing keypoint data, the system identifies violent actions such as hitting or kicking.

## Dependencies
- Python 3.8+
- OpenCV
- PyTorch
- NumPy

## Citation
If you use this repository, please cite the original paper:

> Author(s). "Detection of Violent Behavior Using Neural Networks and Pose Estimation." Year.

## Contributing
Contributions are welcome! Feel free to submit issues or pull requests.

## License
This project is licensed under the MIT License.

