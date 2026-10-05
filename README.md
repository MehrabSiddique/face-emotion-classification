#  Face Emotion Classification using YOLO11

A computer vision project for classifying facial expressions into six emotion categories using a pretrained **YOLO11 classification model** and the Ultralytics framework.

##  Overview

The system classifies facial-expression images into:

* Anger
* Fear
* Happiness
* Neutrality
* Sadness
* Surprise

The project uses transfer learning by starting with pretrained YOLO11 classification weights and adapting the model to the emotion dataset.

##  Workflow

```text
Emotion Image Dataset
        ↓
Dataset Organization
        ↓
YAML Dataset Configuration
        ↓
Pretrained YOLO11 Classification Model
        ↓
Transfer Learning / Fine-Tuning
        ↓
Validation
        ↓
Best Model Weights
        ↓
Test Image Inference
        ↓
Emotion + Confidence Score
```

##  Model

The project uses:

**YOLO11 Large Classification (`yolo11l-cls.pt`)**

The pretrained classification model is fine-tuned on the emotion dataset.

### Training Configuration

* Epochs: 50
* Image size: 224 × 224
* Batch size: 8
* Validation enabled
* Early stopping patience: 20
* Optimizer: AdamW
* Framework: Ultralytics
* Backend: PyTorch

##  Dataset

The dataset contains six emotion categories:

```text
anger
fear
happiness
neutrality
sadness
surprise
```

The notebook uses approximately 3,940 training images and a 50-image validation/test split reported during training.

##  Prediction

For each test image, the trained model predicts:

1. The most likely emotion class
2. The confidence score of that prediction

The predictions are visualized together with the input images.

##  Technologies

* Python
* PyTorch
* Ultralytics YOLO11
* OpenCV
* NumPy
* Matplotlib
* PyYAML

##  Key Concepts

* Computer Vision
* Image Classification
* Transfer Learning
* Deep Learning
* Model Fine-Tuning
* Classification Confidence
* Image Preprocessing

##  Running the Project

Open `emotion_detection.ipynb` in Google Colab and execute the notebook cells sequentially.

The notebook handles dataset preparation, model training, and inference.


##  Notebook

The complete implementation is available in `emotion_detection.ipynb`.
