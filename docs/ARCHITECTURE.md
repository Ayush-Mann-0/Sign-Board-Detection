# Architecture Documentation

This document provides a detailed overview of the Sign Board Detection application's architecture, design patterns, and component interactions.

## High-Level Architecture

The application follows a clean, modular architecture with separation of concerns:

```
┌─────────────────┐    ┌──────────────────┐    ┌──────────────────┐
│   Activities    │◄──►│   Detector       │◄──►│ TensorFlow Lite  │
│ (UI Components) │    │ (ML Processing)  │    │   (Inference)    │
└─────────────────┘    └──────────────────┘    └──────────────────┘
       │                        │
       ▼                        ▼
┌─────────────────┐    ┌──────────────────┐
│   Utilities     │    │   Settings       │
│ (Helpers)       │    │ (Configuration)  │
└─────────────────┘    └──────────────────┘
```

## Core Components

### 1. Activities (UI Layer)

#### WelcomeActivity
- Entry point of the application
- Displays animated logo and get started button
- Handles initial navigation to OptionsActivity

#### OptionsActivity
- Main hub for selecting detection modes
- Implements card-based UI with animations
- Handles permission requests for different modes
- Provides access to SettingsActivity

#### SettingsActivity
- Configuration interface for detection parameters
- Uses SharedPreferences for persistence
- Controls model selection, confidence thresholds, etc.

#### ImageDetectionActivity
- Handles static image processing
- Integrates with device gallery and camera
- Displays detection results on images

#### VideoDetectionActivity
- Processes video files for sign detection
- Uses ExoPlayer for video playback
- Implements frame-by-frame analysis

#### LiveDetectionActivity
- Real-time camera feed processing
- Uses CameraX for camera operations
- Implements continuous detection loop

### 2. Detector (Business Logic Layer)

The Detector class is the core of the application's machine learning functionality:

#### Key Responsibilities:
- Loading TensorFlow Lite models
- Preprocessing input data (images)
- Running inference on the model
- Post-processing detection results
- Applying Non-Maximum Suppression
- Integrating with ObjectTracker

#### Methods:
- `setup()`: Initializes the TensorFlow Lite interpreter
- `detect()`: Performs asynchronous detection on a frame
- `detectSync()`: Performs synchronous detection for batch processing
- `clear()`: Releases resources
- `updateSettings()`: Updates detection parameters from settings

#### Configuration:
- Model selection (Float16 vs Float32)
- Confidence threshold adjustment
- Maximum detections limit
- GPU acceleration toggle

### 3. ObjectTracker (Utility Layer)

Implements temporal consistency for object detection:

#### Features:
- Kalman filter-based tracking
- ID assignment for persistent objects
- Velocity calculation for smooth movement
- Handling of object entry/exit

#### Methods:
- `trackObjects()`: Updates object positions based on new detections
- `getTrackedObjects()`: Returns currently tracked objects
- `reset()`: Clears all tracked objects

### 4. BoundingBox (Data Model)

Represents a detected object with its properties:

#### Properties:
- Coordinates (x1, y1, x2, y2)
- Center point (cx, cy)
- Dimensions (w, h)
- Confidence score (cnf)
- Class information (cls, clsName)

#### Methods:
- `area()`: Calculates bounding box area
- Getters for all properties

### 5. OverlayView (UI Component)

Custom view for drawing detection results:

#### Features:
- Real-time bounding box rendering
- Label display with confidence scores
- Color-coded classes
- Smooth animations

#### Methods:
- `setResults()`: Updates display with new detection results
- `clear()`: Clears the display
- Drawing methods for boxes and labels

### 6. Constants (Configuration)

Centralized configuration management:

#### Properties:
- Model paths
- Label file paths
- Default settings values

## Data Flow

### 1. Initialization Phase
```
App Launch
    ↓
WelcomeActivity
    ↓
OptionsActivity
    ↓
[User selects mode and grants permissions]
    ↓
Mode-specific Activity (Image/Video/Live)
    ↓
Detector.setupWithSettings()
    ↓
[Load model, initialize interpreter]
```

### 2. Detection Phase
```
Input Frame (Bitmap)
    ↓
Detector.detect()
    ↓
[Preprocessing: normalize, resize]
    ↓
TensorFlow Lite Inference
    ↓
[Post-processing: bounding boxes]
    ↓
Non-Maximum Suppression
    ↓
Object Tracking (if enabled)
    ↓
Results to OverlayView
    ↓
UI Display
```

## Design Patterns

### Observer Pattern
- DetectorListener interface for async detection results
- Settings listeners for configuration changes

### Singleton Pattern
- Settings management through static methods
- Shared preferences access

### Builder Pattern
- ImageProcessor configuration
- TensorFlow Lite interpreter options

### Factory Pattern
- Model path selection based on settings

## Performance Considerations

### Memory Management
- Efficient bitmap handling
- Resource cleanup in `onDestroy()`
- Proper lifecycle management

### Threading
- UI thread for rendering
- Background threads for inference
- Coroutine-based async operations

### Battery Optimization
- Frame rate limiting
- GPU acceleration when available
- Early termination of processing when not needed

## Extensibility Points

### Adding New Sign Classes
1. Update labels.txt in assets
2. Retrain the TensorFlow Lite model
3. Replace model files in assets
4. Update UI color schemes if needed

### Adding New Detection Modes
1. Create new Activity extending base functionality
2. Implement mode-specific input handling
3. Add to OptionsActivity
4. Update permission requirements

### Customizing UI
1. Modify layout files in res/layout/
2. Update styles in res/values/
3. Add new animations in res/animator/
4. Update color schemes in res/values/colors.xml