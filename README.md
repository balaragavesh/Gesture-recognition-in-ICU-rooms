# Gesture Recognition in ICU Rooms - YOLOv5

This repository contains a custom version of YOLOv5, modified for hand gesture recognition in ICU rooms. It leverages a pre-trained YOLOv5 model fine-tuned with a custom dataset to detect gestures for real-time applications in an ICU setting.

## Overview

The project utilizes the power of YOLOv5 for object detection, specifically for gesture recognition, and can be deployed on devices like Jetson Nano for real-time performance. The model has been trained using a custom dataset designed to detect gestures in ICU room settings, making it ideal for healthcare applications.

## Features

- **Custom Dataset**: The model is trained on a dataset tailored for ICU room gesture recognition.
- **Real-Time Detection**: YOLOv5 provides real-time inference, with the ability to detect gestures and objects within ICU environments.
- **Model Weights**: The `best.pt` weights file for the trained model is included, enabling quick deployment.

## Model Weights

The model is trained and stored as `best.pt` (located inside the `runs/train/exp2` directory). You can use this pretrained model for gesture recognition tasks in ICU room setups.

### Model Format:
- `best.pt`: The best-performing PyTorch model.
- `best.onnx`: The model converted to ONNX format for deployment across different platforms.

## Validation Results

The model has been validated on several test images, demonstrating its ability to accurately detect hand gestures in ICU environments. Below is an example of the model's validation results:

![Validation Results](predictions.png)

## Usage

To perform inference using the model, run the following command:

```bash
python detect.py --weights runs/train/weights/best.pt --source [image/video/path]
```

This will load the `best.pt` model and perform gesture detection on the provided source.

### Notes:
- **Source**: Specify either an image path, video file, or camera stream URL.
- The model can detect gestures and identify key actions that can be used for further analysis.

## License

This project is licensed under the **MIT License**.

See the [LICENSE](./LICENSE) file for more details.

## Acknowledgments

- YOLOv5: [Ultralytics YOLOv5](https://github.com/ultralytics/yolov5) - for their excellent object detection framework.
- Dataset: Custom dataset designed for hand gesture recognition in ICU rooms.
- CUDA: For optimized GPU support in the inference process.

---

