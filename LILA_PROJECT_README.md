# Lila — Living Desktop Companion

Lila is a persistent, system-integrated animated AI character for Android. She lives on top of your phone's UI, responds to voice commands, and performs autonomous playful animations.

## Features

- **Animated Overlay**: A cute character that stays on top of all apps.
- **AI Voice Assistant**: Integrated with OpenAI for intelligent conversations.
- **System Awareness**: Detects app changes and keyboard status via Accessibility Services.
- **Interactive Animations**: Lottie-based animations for idling, waving, and more.
- **Customization**: Change her color theme and positioning in the settings.

## Technical Details

- **Language**: Kotlin
- **Build System**: Gradle 8.1
- **Target SDK**: 34 (Android 14)
- **Min SDK**: 24 (Android 7.0)
- **Key Components**:
    - `OverlayService`: Manages the system-alert window and character rendering.
    - `LilaAccessibilityService`: Monitors system events for context-aware interactions.
    - `VoiceAssistant`: Handles Speech-to-Text (STT) and Text-to-Speech (TTS).
    - `AIClient`: Retrofit client for OpenAI API integration.

## Setup Instructions

1. **Import to Android Studio**: Open the project folder in Android Studio.
2. **API Key**: Add your OpenAI API key in `AIClient.kt` or implement a secure way to provide it.
3. **Permissions**:
    - Grant **Display over other apps** permission when prompted.
    - Enable **Lila Accessibility Service** in System Settings -> Accessibility.
    - Grant **Microphone** permission for voice commands.
4. **Build and Run**: Deploy to an Android device or emulator.

## Project Structure

- `app/src/main/java/com/lila/companion/`: Core source code.
- `app/src/main/res/layout/`: UI layouts for the main app, settings, and overlay.
- `app/src/main/res/raw/`: Lottie animation JSON files.
- `app/src/main/res/xml/`: Accessibility service configuration.
