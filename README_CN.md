# YOLO Studio

<div align="center">
    <p>
        <a href="README.md">English</a> | <b>简体中文</b>
    </p>
    <img src="assets/logo.png" alt="YOLO Studio Logo" width="200"/>
    <br>
    <h3>一站式YOLO模型训练、标注与部署工具</h3>
    <p>
        <img src="https://img.shields.io/badge/Python-3.7+-blue.svg" alt="Python 3.7+"/>
        <img src="https://img.shields.io/badge/Framework-Tkinter-green.svg" alt="Tkinter"/>
        <img src="https://img.shields.io/badge/AI-YOLO-yellow.svg" alt="YOLO"/>
        <img src="https://img.shields.io/badge/License-Apache--2.0-orange.svg" alt="License: Apache-2.0"/>
    </p>
</div>

## ✨ 项目简介

YOLO Studio 是一个桌面应用，提供矩形图像标注、YOLOv5/YOLOv8 训练参数配置，以及模型导出和推理模块。

**公开仓库范围：** 当前未包含可选的 `security` 授权模块，程序默认按免费模式运行；导出、推理和断点续训受专业版授权检查限制。专业版截图和模块源码不代表这些流程在当前仓库中即可使用。

## 🚀 核心特性

- **矩形标注工具**：通过图形界面标注目标边界框
- **YOLO训练集成**：提供YOLOv5、YOLOv8的配置和训练启动路径
- **训练参数配置**：通过图形界面设置训练参数并启动训练
- **模型导出模块**：提供ONNX、TFLite和OpenVINO转换路径，需要专业版权限和对应依赖
- **目标平台**：源码包含Windows、Linux、macOS处理路径，仓库未提供跨平台验证矩阵
- **简洁界面设计**：专为非技术用户设计的友好操作流程
- **推理模块**：提供图像、视频推理与检测结果展示代码，需要专业版权限
- **数据集导航**：加载图像文件夹并浏览标注

## 📸 界面预览-专业版

<div align="center">
    <img src="assets/screenshots/annotation_CN.png" alt="标注界面" width="45%"/>
    <img src="assets/screenshots/training_CN.png" alt="训练界面" width="45%"/>
    <br><br>
    <img src="assets/screenshots/export_CN.png" alt="导出界面" width="45%"/>
    <img src="assets/screenshots/inference_CN.png" alt="推理界面" width="45%"/>
</div>

## 🔧 快速开始

### 环境要求
- Python 3.7+
- CUDA (可选，用于GPU训练)

### 安装步骤

```bash
# 克隆仓库
git clone https://github.com/garycli/YOLO-Studio.git
cd YOLO-Studio

# 安装依赖
pip install -r requirements.txt

# 启动应用
python main.py
```

程序提供依赖检查和安装辅助；所选流程所需的YOLO代码、权重和转换依赖仍需配置。

### 语言设置

YOLO Studio 支持多语言界面：

1. 启动应用后，点击顶部菜单栏中的"帮助" > "语言设置"
2. 在弹出的对话框中选择您希望使用的语言
3. 点击"应用"按钮
4. 部分界面元素（如菜单）会立即更新
5. **重要：** 要完全切换界面语言，您需要重启应用程序

目前支持的语言：
- 简体中文（默认）
- 英文

## 📚 功能模块详解

### 1. 数据标注模块

- 支持标注形状：矩形
- 便捷的图像导航和缩放功能
- 自动保存和恢复标注进度
- 快捷键支持提高标注效率
- 标注预览与撤销、重做历史

### 2. 模型训练模块

- YOLOv5代码路径配置和YOLOv8包集成
- 可视化训练参数配置
- 训练日志、进度和解析出的损失值
- 展示所选YOLO后端输出的训练结果
- 断点续训代码（需要专业版权限）
- 预训练模型选择

### 3. 模型导出模块

- 转换路径：PyTorch到ONNX、ONNX到TFLite、ONNX到OpenVINO
- TFLite FP16/INT8选项及OpenVINO精度设置，支持范围取决于转换路径
- 导出参数可视化配置
- 安装ONNX依赖后进行模型结构检查，不保证数值等价

### 4. 推理测试模块

- 图像和视频推理支持
- 单个图像或视频输入选择
- 推理结果可视化
- 检测框、类别和置信度展示

## 🛠️ 版本对比

专业版权限依赖未提交的授权模块。下表说明界面中的权限路径，不代表已验证的专业版发行；当前公开源码无法确认图片、类别数量限制。

| 功能 | 开源版 | 专业版 |
|------|--------|--------|
| 数据标注 | ✅ 矩形标注 | 已有矩形标注代码，未实现其他形状 |
| 模型训练 | 基础训练配置 | 依赖授权的参数检查 |
| 模型导出 | 受授权限制 | 已有转换代码，需要授权模块 |
| 推理测试 | 受授权限制 | 已有推理代码，需要授权模块 |
| 断点续训 | 受授权限制 | 已有续训代码，需要授权模块 |

## 🤝 如何贡献

我们非常欢迎社区贡献！无论是功能改进、Bug修复还是文档完善都非常感谢。

1. Fork本仓库
2. 创建特性分支 (`git checkout -b feature/amazing-feature`)
3. 提交更改 (`git commit -m 'Add some amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 创建Pull Request

## 📄 开源协议

本项目采用 Apache-2.0 许可证。详见 [LICENSE](LICENSE) 文件。

## 🙏 鸣谢

- [Ultralytics](https://github.com/ultralytics/yolov5) - YOLOv5原作者
- [ONNX](https://github.com/onnx/onnx) - 开放神经网络交换格式
- [OpenCV](https://github.com/opencv/opencv) - 计算机视觉库

## 📬 联系方式

- 项目问题请使用 [GitHub Issues](https://github.com/garycli/YOLO-Studio/issues)
- 商业合作或者获得专业版应用和许可证请联系: its.jianghe@gmail.com

---

<div align="center">
    <strong>YOLO Studio - 让AI目标检测变得简单</strong>
    <br>
    <sub>如果这个项目对您有帮助，请给它一个⭐️</sub>
</div> 
