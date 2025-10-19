# Copilot Instructions for ocr_sederhana

This project is a Flutter-based OCR (Optical Character Recognition) scanner app. It uses the device camera and Google ML Kit for text recognition. Follow these guidelines to be productive as an AI coding agent in this codebase:

## Architecture Overview
- **Entry Point:** `lib/main.dart` initializes the app and sets the home to `SplashScreen`.
- **Screen Navigation:**
  - `SplashScreen` (lib/screens/splash_screen.dart): Shows a loading indicator, then navigates to `HomeScreen`.
  - `HomeScreen` (lib/screens/home_screen.dart): Main menu, navigates to `ScanScreen`.
  - `ScanScreen` (lib/screens/scan_screen.dart): Handles camera, captures image, runs OCR, navigates to `ResultScreen`.
  - `ResultScreen` (lib/screens/result_screen.dart): Displays recognized text.
- **Camera & OCR:**
  - Uses `camera` and `google_mlkit_text_recognition` packages.
  - Camera initialization and image capture logic is in `ScanScreen`.
  - OCR result is passed to `ResultScreen` via navigation arguments.

## Developer Workflows
- **Build & Run:**
  - Standard Flutter commands: `flutter run`, `flutter build <platform>`.
  - No custom scripts or build steps.
- **Testing:**
  - Widget tests in `test/widget_test.dart` (default template, not project-specific).
  - Run tests with `flutter test`.
- **Dependencies:**
  - Managed in `pubspec.yaml`. Use `flutter pub get` after changes.

## Project Conventions
- **Screens:** Each UI screen is a separate widget in `lib/screens/`.
- **Navigation:** Uses `Navigator.push` and `pushReplacement` for screen transitions.
- **State Management:** Only local widget state (no global state management).
- **Styling:** Uses Material Design, with minimal custom theming.
- **Language:** Some UI text is in Indonesian (e.g., 'Menu Utama', 'Mulai Scan Teks').

## Integration Points
- **Camera:** Requires device camera permissions.
- **ML Kit:** Uses `google_mlkit_text_recognition` for OCR.
- **Path Provider:** Used for file storage (see `ScanScreen`).

## Examples
- To add a new screen, create a Dart file in `lib/screens/`, define a widget, and update navigation as needed.
- To add a dependency, update `pubspec.yaml` and run `flutter pub get`.

## References
- Key files: `lib/main.dart`, `lib/screens/`, `pubspec.yaml`
- For Flutter/Dart style, follow the conventions in existing screen files.

---
If any section is unclear or missing important project-specific details, please provide feedback for further refinement.
