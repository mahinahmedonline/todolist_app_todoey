# Todoey

A simple and elegant Todo list application built with Flutter, focused on managing daily tasks efficiently. 

This project demonstrates strong state management practices and provides a solid foundation for implementing comprehensive Software Quality Assurance (SQA) practices.

## App Features

- **Add Tasks:** Easily add new tasks to your list.
- **Toggle Status:** Mark tasks as completed or incomplete with a simple checkbox toggle.
- **Delete Tasks:** Remove tasks you no longer need.
- **State Management:** Utilizes the `provider` package for robust and scalable state management across screens.

## Technical Details

- **Framework:** Flutter (Dart)
- **State Management:** Provider Architecture (`ChangeNotifier`, `ChangeNotifierProvider`)
- **Key Flutter Widgets used:** `ListView`, `ListTile`, `FloatingActionButton`, `BottomSheet`

## Testing & Quality Assurance (SQA) Focus

This project is structured to support rigorous automated testing at various levels:

- **Unit Testing:** The `TaskData` model (`ChangeNotifier`) can be unit tested independent of the UI to ensure the core logic for adding, updating, and deleting tasks functions flawlessly.
- **Widget Testing:** Individual components like the `TaskTile` and the `TasksList` are isolated, making them ideal candidates for Flutter widget tests to verify UI rendering and user interactions (like checking a task).
- **Integration Testing:** The complete flow of opening the `AddTaskScreen`, typing a task, saving it, and verifying it appears on the `TasksScreen` can be verified using Flutter's integration testing framework.

## Project Structure

- `lib/main.dart` - Entry point setting up the Provider.
- `lib/models/` - Contains data models (`Task`, `TaskData`).
- `lib/screens/` - Contains app screens (`TasksScreen`, `AddTaskScreen`).
- `lib/widgets/` - Contains reusable UI widgets (`TasksList`, `TaskTile`).

## Getting Started

1. Ensure you have Flutter installed on your machine.
2. Clone this repository.
3. Run `flutter pub get` to install dependencies.
4. Run the app using `flutter run`.
5. Execute available tests using `flutter test`.
