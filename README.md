# Flutter To-Do App

A simple, themed To-Do list application built with Flutter and Hive for persistent local storage. This project demonstrates:

- Clean architecture: separation of data, domain, and presentation layers
- DRY principles with reusable widgets and services
- State management via `setState` and Flutter forms/validation
- Local persistence using Hive
- Intuitive UI theme (pink accent, custom dialogs, slidable list items)

---

## 📋 Features

- Add, delete, and toggle tasks
- Persist tasks locally across app restarts (Hive)
- Input validation with inline error messages
- Swipe-to-delete via `flutter_slidable`
- Responsive UI for long task names (ellipsis + wrapping)
- Empty-state prompt when no tasks exist

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (>=2.10)
- Dart 2.16+
- A device/emulator running Android or iOS

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/flutter_todo_app.git
   cd flutter_todo_app
   ```
2. Install dependencies:
   ```bash
   flutter pub get
   ```
3. Initialize Hive:
   ```dart
   // main.dart
   await Hive.initFlutter();
   await Hive.openBox('mybox');
   ```

### Running

```bash
flutter run
```

---

## 🗂️ Project Structure

```text
lib/
├─ data/             # Hive database wrapper (`ToDoDataBase`)
├─ model/            # Domain models (`ToDo` entity)
├─ util/             # Reusable widgets: DialogBox, MyButton, ToDoTile
└─ presentation/
   └─ screens/       # HomeScreen, AddTaskScreen
main.dart           # App entrypoint
```

---

## 🏛️ Architecture

- **Data Layer**: `ToDoDataBase` handles CRUD operations on a Hive box
- **Domain Layer**: `ToDo` model defines the entity
- **Presentation Layer**: Flutter widgets and screens compose the UI
- **State Management**: Simple `setState` and `Form` validation

---

## 🎨 UI Theme

- **Primary**: Pink accent
- **Dialog**: Custom `AlertDialog` with rounded corners, inline validation
- **List**: Slidable cards with shadows, wrapped text, and delete actions

---

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

