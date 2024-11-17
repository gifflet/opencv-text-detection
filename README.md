# OpenCV Text Detection (EAST text detector) 🔍

A Python application that performs real-time text detection in images and video streams using OpenCV and the EAST text detector model.

## 📋 Table of Contents
- [✨ Features](#-features)
- [🔧 Requirements](#-requirements)
- [🚀 Installation](#-installation)
- [💻 Usage](#-usage)
- [🔍 How it Works](#-how-it-works)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [🙏 Acknowledgments](#-acknowledgments)

## ✨ Features
- Real-time text detection in images
- Real-time text detection in video streams and webcam
- Support for multiple text orientations
- Non-maximum suppression for overlapping detections
- Adjustable confidence threshold
- FPS counter for performance monitoring

## 🔧 Requirements
- Python 3.6+
- OpenCV (cv2)
- NumPy
- imutils
- Pre-trained EAST text detector model

## 🚀 Installation

1. Clone this repository:

```bash
git clone https://github.com/gifflet/opencv-text-detection.git
cd opencv-text-detection
```

2. Install the required packages:

```bash
pip install opencv-python numpy imutils
```

3. Download the EAST text detector model (frozen_east_text_detection.pb)

## 💻 Usage

### Image Detection
To detect text in an image:
```bash
python text_detection.py --image path/to/image.jpg --east frozen_east_text_detection.pb
```

Optional arguments:
- `--min-confidence`: Minimum probability to filter weak detections (default: 0.5)
- `--width`: Resized image width (should be multiple of 32)
- `--height`: Resized image height (should be multiple of 32)

### Video/Webcam Detection
To detect text in video or webcam:
```bash
# For webcam
python text_detection_video.py --east frozen_east_text_detection.pb

# For video file
python text_detection_video.py --east frozen_east_text_detection.pb --video path/to/video.mp4
```

## 🔍 How it Works

The application uses the EAST (Efficient and Accurate Scene Text) detector, which is a deep learning model designed for text detection. The process involves:

1. Image preprocessing and resizing
2. Running the EAST detector to get text predictions
3. Decoding the predictions to get bounding box coordinates
4. Applying non-maximum suppression to eliminate overlapping detections
5. Drawing the results on the original image/frame

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.txt) file for details.

## 🙏 Acknowledgments

Project based on the original work by Adrian Rosebrock from PyImageSearch (https://www.pyimagesearch.com/2018/08/20/opencv-text-detection-east-text-detector/)

---

Made with ❤️ by gifflet
