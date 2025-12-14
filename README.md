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

### Project Structure

com.example.todo/
├── ui/
│ ├── MainActivity.kt # Main activity with Scaffold
│ ├── screen/
│ │ └── TodoScreen.kt # Todo screen composables
│ └── theme/ # Material 3 theming
│ ├── Color.kt
│ ├── Theme.kt
│ └── Type.kt
└── viewmodel/
└── TodoViewModel.kt # Business logic and state
