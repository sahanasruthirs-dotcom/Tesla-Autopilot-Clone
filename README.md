
# Tesla Autopilot Clone – Road Object Detection Using YOLOv8

## 1. Project Overview

The Tesla Autopilot Clone is a computer vision project that detects objects in road-driving videos using the YOLOv8 deep learning model.

The system processes a recorded road video and identifies objects such as cars, trucks, buses, motorcycles, bicycles, and pedestrians. It displays bounding boxes, object labels, and confidence scores around detected objects.

This project demonstrates a basic object detection pipeline inspired by the perception component of autonomous driving systems.

## 2. Objectives

- Detect road objects in video frames.
- Identify objects using a pretrained YOLOv8 model.
- Display bounding boxes and predicted class labels.
- Generate an annotated output video.
- Explore the application of computer vision in autonomous driving.

## 3. Technologies Used

- **Programming Language:** Python
- **Deep Learning Model:** YOLOv8
- **Computer Vision:** OpenCV
- **Deep Learning Framework:** PyTorch
- **Development Environment:** Google Colab
- **Model Library:** Ultralytics

## 4. Approach

The project follows these steps:

1. Upload a recorded road video.
2. Load the pretrained YOLOv8 object detection model.
3. Read the video frame by frame.
4. Perform object detection on each frame.
5. Draw bounding boxes, class labels, and confidence scores.
6. Process the frames and save them as an annotated video.
7. Review the output video to verify the detected objects visually.

## 5. Dataset

A recorded road-driving video was used as the input for object detection.

**Input video:** `15001976_2160_3840_30fps.mp4`

The video contains road-scene content used to test the model's ability to detect objects in different frames.

Note: This implementation uses a recorded video for inference. The pretrained YOLOv8 model is used without additional project-specific training.

## 6. Model Selection

The project uses **YOLOv8s**, a pretrained object detection model provided by Ultralytics.

YOLO (You Only Look Once) performs object detection by predicting object locations and classes in an image.

The pretrained model can recognize multiple object categories, including:

- Person
- Car
- Motorcycle
- Bus
- Truck
- Bicycle

The actual detections depend on the objects visible in the input video and the model's confidence threshold.

## 7. Installation

Install Python and the required libraries.

```bash
pip install ultralytics opencv-python torch
```

## 8. How to Run

### Using Google Colab

1. Open Google Colab.
2. Install the required libraries.
3. Upload the road video.
4. Load the YOLOv8s pretrained model.
5. Run the object detection code on the video.
6. Save and download the annotated output video.

### Using Python Locally

Save the source code as `detect_video.py`.

Run the following command:

```bash
python detect_video.py --source "15001976_2160_3840_30fps.mp4"
```

The command assumes the source code accepts the `--source` argument and that the input video is in the current directory. Check the source code for any additional arguments or output-path settings.

## 9. Results

The model was tested on a recorded road video.

The output video contains:
- Detected objects marked with bounding boxes.
- Predicted object class labels.
- Confidence scores for detections.
- Frames processed sequentially to produce an annotated video.

A sample frame was visually checked, and detections such as trucks and pedestrians were observed.

**Output:** An annotated video containing the detected objects.

Add screenshots of the original video, sample detections, and the final output video here before submission.

## 10. Evaluation

The output was checked visually to confirm that objects were detected and bounding boxes appeared around them.

Formal metrics such as precision, recall, mean Average Precision (mAP), and Intersection over Union (IoU) require ground-truth annotations for comparison. These metrics have not been reported because a labeled evaluation dataset was not used in this implementation.

## 11. Challenges

- Some objects may be missed in difficult scenes.
- Detection quality can vary with lighting, distance, and object size.
- Processing high-resolution videos can be slow, especially on a CPU.
- The pretrained model may incorrectly classify some objects.

## 12. Future Improvements

- Train or fine-tune YOLOv8 using a relevant road-scene dataset.
- Evaluate the model using labeled data and standard object detection metrics.
- Improve detection under low-light and adverse weather conditions.
- Add object tracking to follow vehicles across frames.
- Optimize inference speed for real-time processing.
- Explore lane detection and traffic sign recognition.

## 13. Limitations

This project demonstrates object detection on recorded videos. It is not a complete autonomous driving system and does not control a real vehicle.

The model uses pretrained weights and has not been specifically trained for this project. Its predictions should not be relied upon for real-world driving or safety-critical decisions.

## 14. Project Structure

```text
Tesla-Autopilot-Clone/
├── detect_video.py
├── README.md
├── requirements.txt
├── input_video/
│   └── road_video.mp4
└── outputs/
    └── annotated_video.avi
```

The folder and output filenames may differ depending on how the project files are saved.

## 15. Conclusion

This project demonstrates how deep learning and computer vision can be used to detect objects in road-driving videos. By applying a pretrained YOLOv8 model, the system identifies visible road users and generates an annotated video.

The project provides a foundation for further exploration of object tracking, model evaluation, and autonomous-driving perception systems.

## 16. References

- Ultralytics YOLO Documentation: https://docs.ultralytics.com/
- OpenCV Documentation: https://docs.opencv.org/
- PyTorch Documentation: https://pytorch.org/docs/
