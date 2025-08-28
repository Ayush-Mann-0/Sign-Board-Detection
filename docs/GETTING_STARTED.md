# Getting Started Guide

This guide will help you set up and run the Sign Board Detection application on your local development environment.

## Prerequisites

Before you begin, ensure you have the following installed:
- Android Studio Ladybug (2024.1.1) or later
- Android SDK API level 34
- Kotlin 1.9+
- Git (for version control)

## Cloning the Repository

1. Open your terminal or command prompt
2. Navigate to the directory where you want to clone the project
3. Run the following command:

```bash
git clone https://github.com/yourusername/road-sign-detection.git
```

4. Navigate to the project directory:
```bash
cd road-sign-detection
```

## Opening in Android Studio

1. Launch Android Studio
2. Select "Open an existing Android Studio project"
3. Navigate to the cloned project directory and select it
4. Wait for Gradle to sync all dependencies (this may take a few minutes)

## Project Structure

The project follows the standard Android project structure:

```
RoadSignDetection/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/ayush_mann/roadsigndetection/
│   │   │   ├── assets/
│   │   │   ├── res/
│   │   │   └── AndroidManifest.xml
│   │   └── ...
│   ├── build.gradle.kts
│   └── ...
├── gradle/
├── build.gradle.kts
├── gradle.properties
├── gradlew
├── gradlew.bat
├── settings.gradle.kts
├── README.md
├── LICENSE
└── .gitignore
```

## Dependencies

The project uses the following key dependencies:

- TensorFlow Lite (2.17.0) for machine learning inference
- CameraX for camera operations
- ExoPlayer for video processing
- Material Components for UI
- Kotlin Coroutines for asynchronous operations

All dependencies are managed through Gradle and will be automatically downloaded during the build process.

## Building the Project

### From Android Studio:
1. Select "Build" → "Make Project" from the menu
2. Or use the keyboard shortcut (Ctrl+F9 on Windows/Linux, Cmd+F9 on Mac)

### From Command Line:
```bash
# On Windows
gradlew.bat assembleDebug

# On macOS/Linux
./gradlew assembleDebug
```

## Running the Application

### From Android Studio:
1. Connect an Android device or start an emulator
2. Select "Run" → "Run 'app'" from the menu
3. Or click the green "Run" button in the toolbar

### From Command Line:
```bash
# On Windows
gradlew.bat installDebug

# On macOS/Linux
./gradlew installDebug
```

## Troubleshooting

### Common Issues:

1. **Gradle sync failed**:
   - Ensure you have a stable internet connection
   - Try "File" → "Sync Project with Gradle Files"
   - Check that all required SDK components are installed

2. **Missing SDK components**:
   - Open SDK Manager in Android Studio
   - Install API level 34 (Android 14)
   - Install necessary build tools

3. **Emulator issues**:
   - Ensure Intel HAXM is installed for better performance
   - Try creating a new AVD with different specifications

4. **Permission errors**:
   - Ensure your device/emulator is running Android 8.1 (API 27) or higher
   - Grant necessary permissions when prompted

### Need Help?

If you encounter issues not covered in this guide:
1. Check the [Issues](https://github.com/yourusername/road-sign-detection/issues) section of the repository
2. Create a new issue if your problem hasn't been reported
3. Include detailed information about your environment and the error you're experiencing