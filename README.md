# Sole Seekers 1.0

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat&logo=dart&logoColor=white)](https://dart.dev)
[![Platform](https://img.shields.io/badge/Platform-iOS%20%7C%20Android%20%7C%20Web-blue)](https://github.com/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## Table of Contents
- [Overview](#overview)
- [Problem & Solution](#problem--solution)
- [Features](#features)
- [Screenshots](#application-view)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Scripts](#scripts)
- [Contributing](#development)
- [Acknowledgments](#acknowledgments)
- [Contact](#contact)

## Overview
Sole Seekers is a Flutter-based mobile application designed to be the ultimate companion for shoe enthusiasts. Leveraging the power of Flutter, this mobile application offers a smooth and engaging shopping experience across iOS and Android.

## Problem & Solution
**Problem:** Shoe enthusiasts struggle to find a clean, fast, and visually rich shopping app that works consistently across iOS and Android with reliable search, wishlist, and checkout.
**Solution:** Sole Seekers provides a Flutter-first storefront with high-resolution product imagery, advanced filters, wishlist, and a seamless checkout powered by Firebase backend services.

## Features
- **Intuitive Interface:** Enjoy a clean and user-friendly design that prioritizes ease of navigation and discovery.
- **High-Resolution Product Images:** Immerse yourself in stunning visuals that showcase the intricate details of every shoe.
- **Advanced Search Filters:** Refine your search with detailed filtering options by name and price.
- **Wishlist Feature:** Add your favorite shoes to your wishlist for easy future reference and purchase.
- **Seamless Shopping Journey:**  Enjoy a streamlined checkout process that gets you to your coveted footwear in no time.

Additional capabilities
- Authentication with Firebase Auth + Google Sign-In
- Product catalog with Firestore-backed data
- Cart and order flow
- Provider-based state management
- Local caching with Hive
- Connectivity awareness

## Application View
<img src="https://github.com/user-attachments/assets/484535f8-9e25-4ae3-915c-bdfa23ff2b06" alt="On boarding" width="300"/>
<img src="https://github.com/user-attachments/assets/18fbd978-41f4-40a4-a165-ed2d2c065d4a" alt="Home Screen" width="300"/>
<img src="https://github.com/user-attachments/assets/dd2da9c3-9f1a-4028-a025-0baa63bd26b8" alt="Home Screen" width="300"/>

## Target Audience
Sole Seekers caters to a broad audience of footwear enthusiasts, ranging from casual collectors to hardcore sneakerheads. The intuitive interface and diverse product offerings cater to various preferences, making it a one-stop shop for all your shoe needs.

## Tech Stack
- **Framework:** Flutter >=3.3.3 <4.0.0, Dart >=3.3.3
- **State Management:** provider
- **Backend:** Firebase Core, Firebase Auth, Cloud Firestore, Firebase Storage
- **Auth:** google_sign_in
- **UI/UX:** flutter_screenutil, google_fonts, skeletonizer, curved_navigation_bar, smooth_page_indicator
- **Media:** cached_network_image, image_picker
- **Local Storage:** hive_flutter
- **Network:** connectivity_plus, internet_connection_checker
- **Branding:** flutter_native_splash, flutter_launcher_icons, carbon_icons
- **Platforms:** Android, iOS, Web, Windows, macOS, Linux

## Architecture
- `lib/main.dart` — app entry point
- `lib/core/` — providers, models, services
- `lib/screens/` — feature screens and widgets
- `lib/constant/` — themes, colors, font styles, global variables
- `firebase_options.dart` — generated Firebase config
State is managed with Provider. Data lives in Firestore with Firebase Auth, and Hive is used for local persistence.

## Getting Started

### Prerequisites
- Flutter SDK (>=3.3.3 <4.0.0)
- Dart SDK
- Android Studio or Xcode for mobile development
- A Firebase project for backend services

Run `flutter doctor` to verify your setup.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/sole_seekers_1_0.git
   cd sole_seekers_1_0
   ```

2. Install dependencies:
   ```bash
   flutter pub get
   ```

3. Configure Firebase:
   - Add your `google-services.json` for Android in `android/app/`.
   - Add your `GoogleService-Info.plist` for iOS in `ios/Runner/`.
   - If any problem arises watch https://youtu.be/G-mbqiE87Lw?si=on3y5UZ2rgtNvgcv

4. Run the application:
   ```bash
   flutter run
   ```

### Environment Setup
Do not commit `google-services.json` or `GoogleService-Info.plist`. Keep Firebase keys out of source control.

## Project Structure
- `lib/`: Contains the main application code.
- `assets/`: Contains images and other assets used in the app.
- `pubspec.yaml`: Defines the project dependencies and configurations.
- `android/`: Contains Android-specific configurations and code.
- `ios/`: Contains iOS-specific configurations and code.
- `web/`: Contains web-specific configurations and code.

Typical lib layout:
- `lib/constant/` — UI constants
- `lib/core/providers/` — ServicesProvider, QueryProvider, ThemeProvider
- `lib/core/models/` — user_info.dart etc.
- `lib/screens/` — auth_screens, main_screens, misc_screens

## Dependencies
The project uses several dependencies, including:
- `firebase_auth`: For user authentication.
- `cloud_firestore`: For database services.
- `firebase_storage`: For file storage.
- `google_sign_in`: For Google authentication.
- `flutter_native_splash`: For splash screen implementation.
- `provider`: For state management.

## Scripts
```bash
flutter pub get          # install deps
flutter analyze          # static analysis
flutter test             # run tests
flutter build apk        # Android release
flutter build ios        # iOS release
```

## Development
To contribute to the project:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push to your branch and create a pull request.

Branch naming: `feature/<name>`, `fix/<name>`. Follow Dart lint rules from `analysis_options.yaml`.

## Acknowledgments
- Thanks to the Flutter community for their support and resources.
- Special thanks to Firebase for providing backend services.

## Contact
For any inquiries, please contact [olewuezimarvellous@gmail.com].

## License
MIT License. See LICENSE for details.

## Changelog / Roadmap
- v0.1.0 — Initial release with auth, catalog, cart, wishlist
- Planned: push notifications, order tracking, admin panel
