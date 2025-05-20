# Bookpedia 📚

Bookpedia is a Kotlin Multiplatform project designed to showcase a cross-platform book catalog application for **Android**, **iOS**, and **Desktop**. Discover books, search for titles, save favorites, and explore detailed book information with smooth animations.

![Platforms](https://img.shields.io/badge/Platforms-Android%20%7C%20iOS%20%7C%20Desktop-blue)
![Kotlin](https://img.shields.io/badge/Kotlin-Multiplatform-purple)

* `/composeApp` is for code that will be shared across your Compose Multiplatform applications.
  It contains several subfolders:
  - `commonMain` is for code that’s common for all targets.
  - Other folders are for Kotlin code that will be compiled for only the platform indicated in the folder name.
    For example, if you want to use Apple’s CoreCrypto for the iOS part of your Kotlin app,
    `iosMain` would be the right folder for such calls.

* `/iosApp` contains iOS applications. Even if you’re sharing your UI with Compose Multiplatform,
  you need this entry point for your iOS app. This is also where you should add SwiftUI code for your project.

Learn more about [Kotlin Multiplatform](https://www.jetbrains.com/help/kotlin-multiplatform-dev/get-started.html)…

## Features ✨

- **Book Catalog**: Browse a curated list of books with cover images, titles, rating, and authors.
- **Search**: Find books by title, author, or genre.
- **Favorites**: Save your favorite books for quick access.
- **Book Details**: View detailed information including descriptions, ratings, number of pages, and languages.
- **Animations**: Smooth transitions and animations for an engaging experience.
- **Multiplatform**: Shared business logic across Android, iOS, and Desktop.

## Tech Stack 🛠️

- **Kotlin Multiplatform** (KMP) for code sharing.
- **Jetpack Compose** (Android/Desktop) & **SwiftUI** (iOS) for UI.
- **Ktor** for HTTP networking and API calls.
- **SQL** for local caching and favorites storage.
- **Room** for local database.
- **Koin** for dependency injection.
- **Coil** (Android/Desktop) & **SDWebImage** (iOS) for image loading.
- **Kotlinx Serialization** for JSON parsing.

## Installation ⚙️

### Prerequisites
- Android Studio (Electric Eel+ or Arctic Fox+) for Android/Desktop.
- Xcode 14+ (macOS required for iOS builds).
- Kotlin 1.9.0+.
- [Gradle](https://gradle.org/) 8.0+.

### Steps
1. **Clone the repository**:
   ```bash
   git clone https://github.com/Meynisa/CMP-Bookpedia.git

2. **Open the project in Android Studio or IntelliJ IDEA**
3. **Build for your target platform**

### Building 🏗️

##Android
1. Open the `androidApp` module in Android Studio
2. Run the `composeApp` configuration on an emulator or device

## iOS
1. Open iosApp/iosApp.xcodeproj in Xcode.
2. Build and run on a simulator or device

## Desktop
Run the desktopApp module via terminal
   `./gradlew run`

### Project Structure 📂
```
Bookpedia/
├── shared/               # Shared KMP module
│   ├── src/
│   │   ├── commonMain/   # Shared code (ViewModels, UseCases, etc.)
│   │   ├── androidMain/  # Android-specific code
│   │   └── iosMain/      # iOS-specific code
│   └── build.gradle.kts
├── androidApp/           # Android UI module (Jetpack Compose)
├── iosApp/               # iOS UI module (SwiftUI)
├── desktopApp/           # Desktop UI module (Compose for Desktop)
└── build.gradle.kts      # Root Gradle configuration
```

### License 📄
Distributed under the MIT License. See `LICENSE` for details.

### Reference
Reference by https://www.youtube.com/watch?v=WT9-4DXUqsM

Made by [Meynisa].

Acknowledgments to [Open Library API](https://openlibrary.org) for book data.
