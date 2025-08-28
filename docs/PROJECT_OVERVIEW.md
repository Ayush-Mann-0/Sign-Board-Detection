# Project Overview

## S.B.D - Sign Board Detection

This Android application performs real-time road sign detection and recognition using machine learning. The project demonstrates the power of mobile machine learning in real-world applications.

## Key Features

### Core Functionality
- Uses TensorFlow Lite for efficient on-device inference
- Processes live camera feed, images, and videos for sign detection
- Identifies and classifies various road signs in real-time

### Three Main Modes
1. **Image Detection**: Analyze static images from gallery or camera
2. **Video Detection**: Process pre-recorded videos for sign recognition
3. **Live Detection**: Real-time sign detection through camera feed

### Technical Highlights
- GPU acceleration for enhanced performance
- Configurable detection parameters (confidence, max detections)
- Object tracking for smooth visualization
- Non-Maximum Suppression (NMS) to eliminate redundant detections
- Modular architecture for easy model updates

### User Experience
- Clean settings interface for customization
- Adjustable frame rate limits
- Real-time inference time display
- Intuitive UI with smooth animations

## Technology Stack

- **Language**: Kotlin
- **Framework**: Android SDK
- **Machine Learning**: TensorFlow Lite
- **UI Framework**: Material Design Components
- **Camera**: CameraX
- **Video Processing**: ExoPlayer

## Supported Sign Types

Currently, the model can detect and classify:
- Hospital boards
- Other sign boards
- School boards
- Traffic signals

## Architecture

The application follows a modular architecture with the following key components:

1. **Welcome Screen**: Entry point with animated logo
2. **Options Screen**: Selection of detection modes
3. **Settings Screen**: Configuration of detection parameters
4. **Detection Activities**: 
   - Image Detection Activity
   - Video Detection Activity
   - Live Detection Activity
5. **Core Components**:
   - Detector: TensorFlow Lite model interface
   - ObjectTracker: Temporal consistency for detections
   - OverlayView: Visualization of detection results
   - BoundingBox: Data structure for detection results

## Performance Considerations

The application is optimized for:
- Battery efficiency through frame rate limiting
- Fast inference using quantized models
- Memory management for long-running sessions
- GPU acceleration when available