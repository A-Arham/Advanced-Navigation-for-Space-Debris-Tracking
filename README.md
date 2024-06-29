
# Advanced Navigation for Space Debris Tracking

## Overview
This project aims to improve the tracking of space debris using advanced object detection techniques. The dataset was used to train a YOLOv8 model, achieving satisfactory results with high true positive values.

## Dataset Preparation

### Preprocessing & Organizing Dataset
- Used 50% of the provided CSV file to organize a 90-10 split of train & validation datasets.
- This was the first stage of dataset preparation; further refinement was planned based on initial training results.

### Labeling Dataset
- Utilized the ROBOFLOW web application for manual labeling, dataset formatting, and auto-labeling.
- Created and annotated images for all 11 classes, with 120 images per class.

## Training

### Model Architecture
- Loaded YOLO latest from the Ultralytics library.

### Training Parameters
- Epochs: 100
- Batch size: 4
- Transformation modules: random horizontal and vertical flips, resizing to 640x540
- Data split: 70% train, 20% validate, 10% test
- Optimizer: Adam

### Results

#### Confusion Matrix
- The confusion matrix shows satisfactory results with a majority of true positive values, indicating higher model accuracy.

#### Test Data Results
- The test data predictions, learning curves, and loss curves are provided.
- The organized dataset and YOLOv8 trained weights (`best.pt`) are included in the `\detect	rain\weights\` directory for inference and further use.

## Usage

### Inference
To use the trained model for inference, load the weights from the provided directory:
```
model = torch.load('path_to_weights/best.pt')
```

### References
- [Training a Custom Object Detection Model With YOLOv5](https://medium.com/analytics-vidhya/training-a-custom-object-detection-model-with-yolo-v5-7a007dddb3fa)
- [Train YOLOv8 on Custom Dataset – A Complete Tutorial](https://learnopencv.com/train-yolov8-on-custom-dataset/)
- [How to format dataset.yaml to work with the Ultralytics Hub and a custom agent](https://github.com/ultralytics/ultralytics/issues/2650)

## Note
All test data prediction outputs, learning and loss curves, and the organized dataset are present in the provided zip file, including the YOLOv8 trained weights located in `\detect	rain\weightsest.pt`.

## Image Information
The project includes various images in PNG and JPEG formats with different resolutions and color properties. These images were used during the training and testing phases.
