# User Manual

This document provides detailed instructions on how to use the Sign Board Detection application effectively.

## Installation

1. Download the APK from the releases page or build from source
2. Enable "Install from unknown sources" in your device settings
3. Install the APK
4. Grant necessary permissions when prompted

## Getting Started

### Launching the Application

When you first launch the application, you'll see the welcome screen with an animated logo and a "Get Started" button. Tap the button to proceed to the main options screen.

### Main Options Screen

The main screen presents three detection modes:

1. **Image Detection**: Process static images
2. **Video Detection**: Analyze video files
3. **Live Detection**: Real-time camera processing

Each mode is represented by a card with an icon and description. Tap on any card to select that mode.

### Settings

Access the settings by tapping the gear icon in the top right corner of the main options screen. Here you can configure:

- **Model Type**: Choose between Float16 (faster, smaller) and Float32 (more accurate) models
- **Confidence Threshold**: Adjust the minimum confidence level for detections (0-100%)
- **Max Detections**: Set the maximum number of simultaneous detections (1-20)
- **Tracking**: Enable or disable object tracking for smoother visualization
- **GPU Acceleration**: Toggle GPU acceleration for faster processing
- **Frame Rate Limit**: Control maximum frames per second (1-30 FPS)

## Mode-Specific Instructions

### Image Detection

1. Select "Image Detection" from the main screen
2. Choose between:
   - **Gallery**: Select an existing image from your device
   - **Camera**: Capture a new image
3. The app will process the image and display detected signs with bounding boxes
4. Tap "Process Another" to analyze a different image

### Video Detection

1. Select "Video Detection" from the main screen
2. Choose a video file from your device
3. The video will play with real-time detection overlay
4. Use the playback controls to pause, resume, or seek
5. Adjust playback speed if needed

### Live Detection

1. Select "Live Detection" from the main screen
2. Grant camera permission when prompted
3. The camera feed will appear with real-time detection overlay
4. Detected signs will be highlighted with bounding boxes
5. Inference time is displayed at the top of the screen
6. Press the back button to exit

## Interpreting Results

### Detection Display

- **Bounding Boxes**: Rectangles around detected signs
- **Labels**: Text indicating the sign type
- **Confidence Scores**: Percentage indicating detection confidence
- **Colors**: Different colors for different sign types:
  - Red: Hospital boards
  - Blue: School boards
  - Green: Traffic signals
  - Yellow: Other sign boards

### Performance Metrics

- **Inference Time**: Time taken for model processing (displayed in Live mode)
- **Frame Rate**: Current processing speed (visible in settings)

## Troubleshooting

### Common Issues and Solutions

1. **No Detections Found**
   - Ensure good lighting conditions
   - Try adjusting confidence threshold in settings
   - Make sure signs are clearly visible in the frame

2. **Slow Performance**
   - Enable GPU acceleration in settings
   - Reduce frame rate limit
   - Use Float16 model instead of Float32
   - Close other resource-intensive apps

3. **Camera Not Working**
   - Check camera permissions
   - Ensure no other app is using the camera
   - Restart the application

4. **App Crashes**
   - Update to the latest version
   - Clear app cache and data
   - Reinstall the application

### Performance Tips

- For best results, ensure signs are well-lit and clearly visible
- In Live Detection mode, hold the device steady
- Lower the confidence threshold if you're missing detections
- Increase the confidence threshold if you're getting false positives
- Use GPU acceleration for better performance on supported devices

## Settings Explained

### Model Type

- **Float16**: Faster processing, smaller model size, slightly less accurate
- **Float32**: More accurate, larger model size, slower processing

### Confidence Threshold

Controls how confident the model must be to display a detection:
- Lower values (10-20%): More detections, including potentially false positives
- Higher values (50-80%): Fewer but more reliable detections

### Max Detections

Limits the maximum number of simultaneous detections displayed:
- Lower values (1-5): Cleaner display, less clutter
- Higher values (10-20): More comprehensive detection coverage

### Tracking

Enables temporal consistency for smoother visualization:
- On: Objects maintain consistent IDs and smoother movement
- Off: Each frame processed independently

### GPU Acceleration

Uses GPU for faster processing when available:
- On: Faster inference on supported devices
- Off: CPU-only processing (more compatible)

### Frame Rate Limit

Controls maximum processing frames per second:
- Lower values (5-10 FPS): Better battery life, less heat
- Higher values (15-30 FPS): Smoother real-time processing

## Privacy and Permissions

The application requires the following permissions:

- **Camera**: For Live Detection mode
- **Storage**: For Image and Video Detection modes
- **Internet**: For downloading updates (if implemented in future versions)

All processing happens on-device. No images or videos are uploaded to external servers.

## Frequently Asked Questions

### Q: Does the app work offline?
A: Yes, all processing happens on your device. No internet connection is required for detection.

### Q: What types of signs can the app detect?
A: Currently, the app can detect Hospital boards, School boards, Traffic signals, and Other sign boards.

### Q: Can I add new sign types?
A: The current version doesn't support adding new sign types without rebuilding the model. This feature may be added in future versions.

### Q: Is my data safe?
A: Yes, all processing is done locally on your device. No personal data is collected or transmitted.

### Q: Why is the app slow on my device?
A: Performance depends on your device's hardware. Enable GPU acceleration and use the Float16 model for better performance.

## Support

For support, please:
1. Check this user manual
2. Review existing issues on GitHub
3. Create a new issue if your problem isn't addressed

## Version Information

Current version: 1.0
Target SDK: Android 14 (API 34)
Minimum SDK: Android 8.1 (API 27)