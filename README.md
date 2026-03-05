# Todoey

**Todoey** is a simple, beautiful, and intuitive to-do list application built using modern Flutter principles. It primarily focuses on managing application state cleanly and efficiently across an app using the `provider` package.

---

## Features

*   **Add Tasks:** Quickly add new to-do items using an elegant sliding bottom sheet interface.
*   **Toggle State:** Mark tasks as complete or incomplete, accompanied by dynamic UI updates (strikethrough text).
*   **Delete Tasks:** Remove items from your task list seamlessly using a "long press" interaction.
*   **State Management:** Extensively utilizes `ChangeNotifierProvider` to cleanly separate UI presentation from business logic, making the codebase highly scalable and maintainable.
*   **Responsive UI:** Built with Flutter's Material Design widgets for a cohesive and native-feeling user experience on both iOS and Android platforms.

---

## Architecture & File Structure

The project has been refactored or structured from avoiding passing callbacks down the widget tree endlessly (prop drilling), utilizing Provider instead:

```text
lib/
 ├── main.dart             # Application root, initializes the ChangeNotifierProvider
 ├── models/
 │    ├── task.dart        # Core data model representing a single task
 │    └── task_data.dart   # The ChangeNotifier class managing the state of the task list globally
 ├── screens/
 │    ├── tasks_screen.dart    # Main dashboard UI containing the header and list
 │    └── add_task_screen.dart # Modal bottom sheet UI for text input
 └── widgets/
      ├── tasks_list.dart  # ListView builder consuming Provider to render tiles
      └── task_tile.dart   # Individual list item UI component
```

---

## Getting Started

To run the application locally on your machine, follow these steps:

### Prerequisites
*   [Flutter SDK](https://flutter.dev/docs/get-started/install) (Version ^3.10.8 or higher, as defined in `pubspec.yaml`)
*   An IDE like VS Code, Android Studio, or IntelliJ with the Flutter and Dart plugins installed.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/todoey.git
    ```
2.  **Navigate into the directory:**
    ```bash
    cd todoey
    ```
3.  **Fetch the dependencies:**
    ```bash
    flutter pub get
    ```
4.  **Run the application (either on an emulator or a connected physical device):**
    ```bash
    flutter run
    ```

---

## 🛠 Built With

*   **[Flutter](https://flutter.dev/)** - UI Toolkit for creating natively compiled applications.
*   **[Dart](https://dart.dev/)** - Client-optimized programming language for rapid apps on any platform.
*   **[Provider](https://pub.dev/packages/provider)** - The community-recommended, pragmatic state management solution wrapper over InheritedWidget.

---
*Created as a demonstration of state management techniques in Flutter.*
