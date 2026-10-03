# YOLO Studio

<div align="center">
    <p>
        <b>English</b> | <a href="README_CN.md">简体中文</a>
    </p>
    <img src="assets/logo.png" alt="YOLO Studio Logo" width="200"/>
    <br>
    <h3>All-in-One YOLO Model Training, Annotation and Deployment Tool</h3>
    <p>
        <img src="https://img.shields.io/badge/Python-3.7+-blue.svg" alt="Python 3.7+"/>
        <img src="https://img.shields.io/badge/Framework-Tkinter-green.svg" alt="Tkinter"/>
        <img src="https://img.shields.io/badge/AI-YOLO-yellow.svg" alt="YOLO"/>
        <img src="https://img.shields.io/badge/License-Apache--2.0-orange.svg" alt="License: Apache-2.0"/>
    </p>
</div>

## ✨ Project Overview

YOLO Studio is a desktop application for rectangular image annotation and configurable YOLOv5/YOLOv8 training, with model export and inference modules.

**Public repository scope:** The optional `security` licensing module is not included. The application defaults to free mode; export, inference, and checkpoint resumption are gated by professional-license checks. Professional screenshots and source modules do not establish that those workflows are available in this checkout.

## 🚀 Key Features

- **Rectangle Annotation Tool**: Graphical interface for bounding-box annotation
- **YOLO Training Integration**: Configuration and launch paths for YOLOv5 and YOLOv8
- **Training Configuration**: Graphical controls for training parameters and process launch
- **Export Modules**: ONNX, TFLite, and OpenVINO conversion paths; require professional access and format-specific dependencies
- **Platform Targets**: Windows, Linux, and macOS code paths; this repository does not include a cross-platform validation matrix
- **Clean Interface Design**: User-friendly workflow designed for non-technical users
- **Inference Module**: Image/video inference code with detection visualization; requires professional access
- **Dataset Navigation**: Load an image folder and navigate annotations

## 📸 Interface Preview - Professional Version

<div align="center">
    <img src="assets/screenshots/annotation.png" alt="Annotation Interface" width="45%"/>
    <img src="assets/screenshots/training.png" alt="Training Interface" width="45%"/>
    <br><br>
    <img src="assets/screenshots/export.png" alt="Export Interface" width="45%"/>
    <img src="assets/screenshots/inference.png" alt="Inference Interface" width="45%"/>
</div>

## 🔧 Quick Start

### Requirements
- Python 3.7+
- CUDA (optional, for GPU training)

### Installation Steps

```bash
# Clone the repository
git clone https://github.com/garycli/YOLO-Studio.git
cd YOLO-Studio

# Install dependencies
pip install -r requirements.txt

# Launch the application
python main.py
```

The application includes dependency checks and installation helpers. YOLO code, weights, and conversion-specific dependencies still need to be configured for the selected workflow.

### Language Settings

YOLO Studio supports multiple languages:

1. After launching the app, click "Help" > "Language Settings" in the top menu bar
2. Select your preferred language in the dialog
3. Click the "Apply" button
4. Some UI elements (like menus) will update immediately
5. **Important:** To fully switch the interface language, you need to restart the application

Currently supported languages:
- Simplified Chinese (Default)
- English

## 📚 Module Details

### 1. Data Annotation Module

- Supports annotation shapes: rectangles
- Convenient image navigation and zoom functions
- Automatic saving and restoration of annotation progress
- Shortcut key support to improve annotation efficiency
- Annotation preview and undo/redo history

### 2. Model Training Module

- YOLOv5 code-path configuration and YOLOv8 package integration
- Visual training parameter configuration
- Training logs, progress, and parsed loss values
- Display of training output reported by the selected YOLO backend
- Checkpoint resumption code (requires professional access)
- Pre-trained model selection

### 3. Model Export Module

- Conversion paths: PyTorch to ONNX, ONNX to TFLite, and ONNX to OpenVINO
- TFLite FP16/INT8 options and OpenVINO precision settings; support depends on the conversion path
- Visual export parameter configuration
- ONNX structural checks when the ONNX dependency is available; no numerical-equivalence guarantee

### 4. Inference Testing Module

- Image and video inference support
- Single image or video input selection
- Inference result visualization
- Detection box, class, and confidence display

## 🛠️ Version Comparison

Professional access depends on the omitted licensing module. The table describes the UI's access paths, not a verified professional release; image/class limits cannot be confirmed from this public snapshot.

| Feature | Open Source Version | Professional Version |
|---------|---------------------|----------------------|
| Data Annotation | ✅ Rectangle annotation | Rectangle annotation code; additional shapes not implemented here |
| Model Training | Basic training configuration | License-dependent parameter checks |
| Model Export | License-gated | Conversion code present; licensing module required |
| Inference Testing | License-gated | Inference code present; licensing module required |
| Checkpoint Resumption | License-gated | Resumption code present; licensing module required |

## 🤝 How to Contribute

We welcome community contributions! Whether it's feature improvements, bug fixes, or documentation improvements, we appreciate all help.

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Create a Pull Request

## 📄 License

This project is licensed under the Apache-2.0 License. See the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Ultralytics](https://github.com/ultralytics/yolov5) - YOLOv5 creator
- [ONNX](https://github.com/onnx/onnx) - Open Neural Network Exchange format
- [OpenCV](https://github.com/opencv/opencv) - Computer Vision library

## 📬 Contact

- For project issues, please use [GitHub Issues](https://github.com/garycli/YOLO-Studio/issues)
- For business cooperation or to obtain the professional version and license, please contact: its.jianghe@gmail.com

---

<div align="center">
    <strong>YOLO Studio - Making AI Object Detection Simple</strong>
    <br>
    <sub>If this project helps you, please give it a ⭐️</sub>
</div> 
