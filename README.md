# S.B.D (Sign Board Detection)

[![Android](https://img.shields.io/badge/Platform-Android-green.svg)](https://www.android.com)
[![Kotlin](https://img.shields.io/badge/Language-Kotlin-blue.svg)](https://kotlinlang.org/)
[![TensorFlow Lite](https://img.shields.io/badge/ML-TensorFlow%20Lite-orange.svg)](https://www.tensorflow.org/lite)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

<p align="center">
  <img src="app/src/main/res/drawable/logo.png" alt="SBD Logo" width="200"/>
</p>

**Real-time Road Sign Detection Android Application using TensorFlow Lite**

S.B.D (Sign Board Detection) is an Android application that leverages machine learning to detect and classify various road signs in real-time. The app offers three distinct detection modes and utilizes TensorFlow Lite for efficient on-device inference, making it perfect for driver assistance, traffic analysis, or educational purposes.

## 🌟 Features

* **Three Detection Modes**:
  * 📷 **Image Detection**: Analyze static images from gallery or camera
  * 🎥 **Video Detection**: Process pre-recorded videos for sign recognition
  * 📹 **Live Detection**: Real-time sign detection through camera feed

* **Advanced ML Capabilities**:
  * 🔥 TensorFlow Lite for efficient on-device inference
  * ⚡ GPU acceleration for enhanced performance
  * 🎯 Object tracking for smooth visualization
  * 🧹 Non-Maximum Suppression (NMS) to eliminate redundant detections
  * 📦 Modular architecture for easy model updates

* **Customizable Settings**:
  * ⚙️ Adjustable confidence thresholds
  * 🎛️ Configurable maximum detections
  * 🖼️ Model selection (Float16 vs Float32)
  * 🎚️ Frame rate limiting controls
  * 💡 GPU acceleration toggle

* **User Experience**:
  * 🎨 Clean, intuitive Material Design interface
  * 📊 Real-time inference time display
  * 🎭 Smooth animations and transitions
  * 🔐 Proper permission handling
  * 📱 Responsive design for various screen sizes

## 📱 Supported Sign Types

The current model can detect and classify:
* 🏥 Hospital boards
* 📋 Other sign boards
* 🏫 School boards
* 🚦 Traffic signals

## 🛠️ Technical Architecture

### Core Components
* **TensorFlow Lite**: For efficient mobile inference
* **CameraX**: For camera operations in live detection
* **ExoPlayer**: For video processing
* **Material Components**: For modern UI/UX
* **SharedPreferences**: For settings persistence

### Detection Pipeline
1. Input preprocessing (normalization, resizing)
2. TensorFlow Lite model inference
3. Post-processing (bounding box calculation)
4. Non-Maximum Suppression filtering
5. Object tracking for temporal consistency
6. Visualization on screen

### Performance Optimizations
* GPU delegate support for faster inference
* Frame rate limiting to balance performance and battery
* Efficient memory management
* Model quantization (Float16 support)

## 📋 Requirements

* **Minimum SDK**: Android 8.1 (API level 27)
* **Target SDK**: Android 14 (API level 34)
* **Kotlin**: 1.9+
* **TensorFlow Lite**: 2.17.0
* **Camera Permissions**: Required for live detection
* **Storage Permissions**: Required for image/video processing

## 🚀 Installation

### Prerequisites
* Android Studio Ladybug | 2024.1.1 or later
* Android SDK API level 34
* Kotlin 1.9+

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/Ayush-Mann-0/Sign-Board-Detection
   ```
2. Open the project in Android Studio
3. Sync the project with Gradle files
4. Build and run the application

### Building from Command Line
```bash
# Assemble debug APK
./gradlew assembleDebug

# Install on connected device
./gradlew installDebug
```

## 🎮 Usage

1. Launch the application
2. Select one of the three detection modes:
   * **Image Detection**: Choose an image from gallery or capture a new one
   * **Video Detection**: Select a video file for processing
   * **Live Detection**: Use your device camera for real-time detection
3. Adjust settings in the configuration panel as needed
4. View detection results with bounding boxes and labels

## 📁 Project Structure

```
app/
├── src/
│   ├── main/
│   │   ├── java/com/ayush_mann/roadsigndetection/
│   │   │   ├── activities/     # Main activity classes
│   │   │   ├── detector/       # ML detection logic
│   │   │   ├── tracker/        # Object tracking utilities
│   │   │   └── utils/          # Helper classes
│   │   ├── assets/
│   │   │   ├── model_float16.tflite  # Quantized model
│   │   │   ├── model_float32.tflite  # Full precision model
│   │   │   └── labels.txt            # Class labels
│   │   └── res/                      # Resources
│   └── ...
├── build.gradle.kts               # App-level build config
└── ...
```

## ⚙️ Configuration

The app provides extensive configuration options accessible through the settings menu:

| Setting | Description | Range | Default |
|---------|-------------|-------|---------|
| Model Type | TensorFlow Lite model precision | Float16/Float32 | Float16 |
| Confidence Threshold | Minimum detection confidence | 0-100% | 30% |
| Max Detections | Maximum simultaneous detections | 1-20 | 10 |
| Tracking | Enable object tracking | On/Off | On |
| GPU Acceleration | Use GPU for inference | On/Off | On |
| Frame Rate Limit | Max processing FPS | 1-30 FPS | 10 FPS |

## 🧪 Testing

The project includes both unit tests and instrumented tests:

```bash
# Run unit tests
./gradlew test

# Run instrumented tests
./gradlew connectedAndroidTest
```

## 📊 Performance Metrics

Typical inference times on various devices:
* **High-end devices**: 15-30ms
* **Mid-range devices**: 30-60ms
* **Entry-level devices**: 60-120ms

Actual performance may vary based on:
* Device hardware capabilities
* Selected model type (Float16 vs Float32)
* Enabled optimizations (GPU acceleration)
* Current system load

## 🔮 Future Enhancements

* [ ] Expand sign classification database
* [ ] Add cloud model updating capability
* [ ] Implement offline maps integration
* [ ] Add detection statistics and analytics
* [ ] Support for custom sign training
* [ ] Multi-language UI support
* [ ] Dark theme implementation

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a pull request

Please ensure your code follows the existing style and includes appropriate tests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

* [TensorFlow Lite](https://www.tensorflow.org/lite) for the ML framework
* [Android Open Source Project](https://source.android.com/) for the platform
* [Material Design](https://material.io/) for the design guidelines
* All contributors who have helped shape this project

## 📞 Contact

Project Link: [https://github.com/yourusername/road-sign-detection](https://github.com/yourusername/road-sign-detection)

---

<p align="center">Made with ❤️ for safer roads and smarter driving</p>
