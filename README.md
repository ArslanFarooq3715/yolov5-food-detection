# Food Recognition YOLOv5

This repository contains a comprehensive implementation of food recognition using state-of-the-art deep learning models, including YOLOv5 and YOLOv8. The project integrates object detection, image classification, and semantic segmentation, tailored specifically for food-related applications.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Models](#models)
- [Dataset](#dataset)
- [Implementation Details](#implementation-details)
- [Contributing](#contributing)
- [License](#license)

## Features
- **Object Detection**: Detect food items in images with high accuracy.
- **Image Classification**: Classify food items into specific categories.
- **Semantic Segmentation**: Segment food items in images for detailed analysis.
- **Pretrained Weights**: Access pretrained models for faster inference.
- **Web Application**: Run a user-friendly web app for inference and training.

## Installation
To get started with this project, clone the repository and install the required dependencies:

```bash
git clone https://github.com/ArslanFarooq3715/yolov5-food-detection.git
cd yolov5-food-detection
pip install -e .
```

## Usage
### Inference
To run the web application, use the following command:

```bash
# Windows
run.bat

# Or, alternatively
python3 app.py
```

**Note**: You can safely run the app in an insecure HTTP connection on localhost. For HTTPS, generate an SSL certificate.

### Training
Refer to the respective notebooks for training your own models:
- [Detection Notebook](#)
- [Classification Notebook](#)
- [Semantic Segmentation Notebook](#)

## Models
| Model          | Image Size | Epochs | mAP@0.5 | mAP@0.5:0.95 |
|----------------|------------|--------|---------|---------------|
| YOLOv5s        | 640x640    | 172    | 0.907   | 0.671         |
| YOLOv5m        | 640x640    | 112    | 0.897   | 0.666         |
| YOLOv5l        | 640x640    | 118    | 0.940   | 0.730         |
| YOLOv5x        | 640x640    | 62     | 0.779   | 0.533         |
| YOLOv8s        | 640x640    | 70     | 0.963   | 0.820         |

### Segmentation Models
| Model          | Image Size | Epochs | Pixel AP | Pixel AR | Dice Score |
|----------------|------------|--------|----------|----------|------------|
| UNet++         | 640x640    | 5      | 0.931    | 0.935    | 99.95      |

### Classification Models
| Model                | Image Size | Epochs | Accuracy | Balanced Acc | F1-score |
|---------------------|------------|--------|----------|--------------|----------|
| EfficientNet-B4     | 640x640    | 7      | 84.069   | 86.033       | 84.116   |

## Dataset
- **Detection**: [Merged OID and Vietnamese Lunch Dataset](#)
- **Classification**: [MAFood121](#)
- **Semantic Segmentation**: [UECFood](#)

### Dataset Details
To train the food detection model, we surveyed various datasets, enhancing our model's performance and variety.

## Implementation Details
The repository contains multiple implementation versions:
- **Training Template**: Utilizes a custom object detection template based on Ultralytics' source code, leveraging COCO format datasets.
- **Ensemble Technique**: Merges results from four models to improve accuracy.
- **Label Enhancement**: Uses a pretrained EfficientNet-B4 classifier for refining labels related to food items.
- **Test-Time Augmentation**: Added to enhance the robustness of the web app.

For those interested in earlier versions, check out the `v1` branch.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

