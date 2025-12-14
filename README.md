# 📝 Todo App - Part 1

A simple Android Todo application built with Jetpack Compose and MVVM architecture. This project demonstrates modern Android development practices with ViewModel and state management.

## 📱 Description

This is a basic Todo list application that displays a list of todo items. The app uses MVVM (Model-View-ViewModel) architecture pattern to separate business logic from UI components, making the code more maintainable and testable.

## ✨ Features

- **Todo List Display:** View a list of todo items in a scrollable list
- **MVVM Architecture:** Clean separation between UI and business logic
- **Modern UI:** Built with Jetpack Compose and Material 3
- **Lazy Loading:** Efficient list rendering with LazyColumn
- **State Management:** Reactive state handling with ViewModel

## 🏗️ Architecture

The app follows MVVM (Model-View-ViewModel) architecture:

- **View:** `TodoScreen` - Composable UI components
- **ViewModel:** `TodoViewModel` - Manages UI state and business logic
- **State:** `mutableStateListOf<String>` - Reactive todo list

## 🛠️ Built With

- **Kotlin** - Primary programming language
- **Jetpack Compose** - Modern declarative UI toolkit
- **Material 3** - Latest Material Design components
- **ViewModel** - Lifecycle-aware state management
- **Android Studio** - Official Android development environment

## 🎨 Key Components

### TodoViewModel

Manages the application state with a reactive list of todos:

```kotlin
class TodoViewModel : ViewModel() {
    val todos = mutableStateListOf<String>()
}
```

### TodoScreen

Smart component that connects ViewModel to UI:

```kotlin
@Composable
fun TodoScreen(todoViewModel: TodoViewModel = viewModel()) {
    TodoList(todos = todoViewModel.todos)
}
```

### TodoList

Presentational component that renders the list:

```kotlin
@Composable
fun TodoList(todos: List<String>) {
    LazyColumn {
        items(todos) { todo ->
            Text(text = todo)
        }
    }
}
```

## 🚀 Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/c3sean00/Todopart1.git
   ```

2. Open the project in Android Studio

3. Build and run on an emulator or physical device

## 📋 Requirements

- Android Studio Hedgehog | 2023.1.1 or newer
- Minimum SDK: API 24 (Android 7.0)
- Target SDK: API 34 (Android 14)
- Kotlin 1.9+

## 🔄 Future Improvements (Part 2+)

- Add new todo functionality
- Delete todo items
- Mark todos as completed
- Edit existing todos
- Persist data with Room database
- Add todo categories/tags

## 📝 License

This project is created for educational purposes.

## 👤 Author

**c3sean00**

- GitHub: [@c3sean00](https://github.com/c3sean00)

---

⭐ Star this repository if you find it helpful!
