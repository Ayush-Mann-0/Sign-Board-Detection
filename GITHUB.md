# S.B.D (Sign Board Detection)

[![Android](https://img.shields.io/badge/Platform-Android-green.svg)](https://www.android.com)
[![Kotlin](https://img.shields.io/badge/Language-Kotlin-blue.svg)](https://kotlinlang.org/)
[![TensorFlow Lite](https://img.shields.io/badge/ML-TensorFlow%20Lite-orange.svg)](https://www.tensorflow.org/lite)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

<p align="center">
  <img src="app/src/main/res/mipmap-xxxhdpi/ic_launcher.png" alt="SBD Logo" width="200"/>
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

## 📸 Screenshots

<div style="display:flex; flex-wrap:wrap; gap:10px;">
  <img src="screenshots/welcome_screen.png" alt="Welcome Screen" width="200"/>
  <img src="screenshots/options_screen.png" alt="Options Screen" width="200"/>
  <img src="screenshots/settings_screen.png" alt="Settings Screen" width="200"/>
  <img src="screenshots/live_detection.png" alt="Live Detection" width="200"/>
</div>

## 🛠️ Technical Architecture

### Core Components
* **TensorFlow Lite**: For efficient mobile inference
* **CameraX**: For camera operations in live detection
* **ExoPlayer**: For video processing
* **Material Components**: For modern UI/UX
* **SharedPreferences**: For settings persistence

## 📋 Requirements

* **Minimum SDK**: Android 8.1 (API level 27)
* **Target SDK**: Android 14 (API level 34)
* **Kotlin**: 1.9+
* **TensorFlow Lite**: 2.17.0

## 🚀 Installation

### Prerequisites
* Android Studio Ladybug | 2024.1.1 or later
* Android SDK API level 34
* Kotlin 1.9+

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/road-sign-detection.git
   ```
2. Open the project in Android Studio
3. Sync the project with Gradle files
4. Build and run the application

## 📁 Documentation

Detailed documentation is available in the [docs](docs/) directory:
* [Project Overview](docs/PROJECT_OVERVIEW.md)
* [Getting Started Guide](docs/GETTING_STARTED.md)
* [Architecture Documentation](docs/ARCHITECTURE.md)
* [User Manual](docs/USER_MANUAL.md)
* [Contributing Guidelines](docs/CONTRIBUTING.md)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guidelines](docs/CONTRIBUTING.md) for details on how to submit pull requests, report issues, and suggest improvements.

---

<p align="center">Made with ❤️ for safer roads and smarter driving</p>