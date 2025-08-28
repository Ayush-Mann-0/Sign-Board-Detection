# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2025-08-28

### Added
- Initial release of Sign Board Detection application
- Three detection modes: Image, Video, and Live
- TensorFlow Lite integration for on-device inference
- Support for detecting 4 types of road signs:
  - Hospital boards
  - Other sign boards
  - School boards
  - Traffic signals
- GPU acceleration support
- Configurable detection parameters:
  - Confidence threshold
  - Maximum detections
  - Model selection (Float16/Float32)
  - Frame rate limiting
  - Object tracking
- Material Design UI with smooth animations
- Comprehensive settings panel
- Proper permission handling for all Android versions
- Real-time inference time display
- Non-Maximum Suppression for eliminating redundant detections
- Object tracking for temporal consistency
- Support for Android 8.1 (API 27) to Android 14 (API 34)

### Technical Features
- Kotlin implementation
- CameraX for camera operations
- ExoPlayer for video processing
- TensorFlow Lite 2.17.0
- Modern Android architecture components
- Efficient memory management
- Battery optimization through frame rate limiting
- Modular code structure for easy maintenance

### Documentation
- Comprehensive README with setup instructions
- User manual
- Architecture documentation
- Contribution guidelines
- Getting started guide