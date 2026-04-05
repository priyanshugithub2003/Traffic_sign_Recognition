# Traffic Sign Recognition

Traffic Sign Recognition is a deep learning-based system that identifies and classifies traffic signs such as speed limits, stop signs, and turn directions. This is useful in autonomous driving systems and driver assistance applications.

---

## Features

- Classifies 43 traffic sign categories
- CNN-based image classification
- Training and testing pipeline
- GUI for predictions
- Uses GTSRB dataset

---

## Important Requirement

### Python Version

This project uses TensorFlow.

Python 3.13 is not supported.

Supported versions:
- Python 3.9 to 3.12

Recommended:
- Python 3.10 or 3.11

---

## Setup

### 1. Install Python 3.11
```bash
winget install Python.Python.3.11
```
---

### 2. Create Virtual Environment
```bash
py -3.11 -m venv tf_env
tf_env\Scripts\Activate
```
---

### 3. Install Dependencies
```bash
pip install --upgrade pip
pip install tensorflow numpy pandas matplotlib opencv-python pillow scikit-learn
```
---

## Project Structure

```
Traffic sign classification/
│
├── Train/ # Training images (0–42 folders)
├── Test/ # Test images
├── Meta/ # Metadata images
│
├── Train.csv # Training labels
├── Test.csv # Test labels
├── Meta.csv # Metadata
│
├── traffic_sign.py # Training script
├── gui.py # GUI application
│
├── my_model.keras # Saved model
├── traffic_classifier.keras
```
---

## Usage

### Train the Model
```bash
python traffic_sign.py
```

This will:
- Load training data
- Train the model
- Save the model
- Evaluate accuracy

---

### Run GUI for Prediction
```bash
python gui.py
```

Steps:
- Upload an image
- Click predict
- View result

---

### Run Only Testing (Optional)

Modify your script:
```bash
from tensorflow.keras.models import load_model
model = load_model("my_model.keras")
```

---

## Working

- Images are loaded from:
Train/<class_id>/

- Each folder corresponds to a class (0 to 42)

- Test data:
  - Path -> image location
  - ClassId -> correct label

---

### Wrong Python in VS Code

Fix: Ctrl + Shift + P → Python: Select Interpreter → tf_env

---

## Recommended Workflow

1. Install Python 3.11
2. Create virtual environment
3. Install dependencies
4. Train model once
5. Use GUI for predictions

---

## Dataset

German Traffic Sign Recognition Benchmark (GTSRB):
https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign

---

## Improvements

- Data augmentation
- Model checkpointing
- Separate train/test scripts
- Support for PyTorch (Python 3.13)

---

## License

For educational use only.
