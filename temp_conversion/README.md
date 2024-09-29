# Temperature Conversion

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.


# Temperature Converter App

A simple Flutter application that converts temperatures between Fahrenheit and Celsius. This app features:

- Real-time conversion between Fahrenheit and Celsius.
- Displays the conversion history, limited to the last 5 calculations.
- Shows the current time, updated every second.

## Table of Contents

- [Installation](#installation)
- [Features](#features)
- [App Structure](#app-structure)
- [Conversion Logic](#conversion-logic)
- [Real-Time Clock](#real-time-clock)
- [History Management](#history-management)
- [Screenshots](#screenshots)

---

## Installation

To run the project on your local machine:

1. Ensure that you have [Flutter](https://flutter.dev/docs/get-started/install) installed.
2. Clone the repository:
    ```bash
    git clone <repository-url>
    ```
3. Navigate to the project directory:
    ```bash
    cd temperature_converter
    ```
4. Run the app:
    ```bash
    flutter run
    ```

Ensure that you have an emulator or a connected device to see the app in action.

---

## Features

The app allows you to convert:

- Fahrenheit to Celsius
- Celsius to Fahrenheit

Simply input the temperature you want to convert, select the conversion mode, and click `Convert`.

### History Management

The app stores the last 5 conversion results in a list for reference. If more than 5 conversions are performed, the oldest item is automatically removed.

### Real-Time Clock

The app displays the current time, which updates every second, located at the bottom of the app.

### Reset Option

The app provides a `Reset` button that clears the input field and the conversion result, allowing users to start a fresh conversion.

---

## App Structure

The app consists of the following key components:

### 1. **`TemperatureConverterApp`**: 

The root widget of the app, which sets up the `MaterialApp`.

### 2. **`TemperatureConverter`**:

The main screen of the app, a `StatefulWidget`, responsible for managing user inputs, conversions, and displaying the current time and history.

### 3. **Conversion Modes**:

- `Fahrenheit to Celsius`
- `Celsius to Fahrenheit`

These modes are selectable by using radio buttons.

### 4. **History Management**:

- Conversion results are stored in a list (`_conversionHistory`).
- The history is limited to the last 5 entries.

---

## Conversion Logic

The conversion is handled by the `_convert()` method:

- For **Fahrenheit to Celsius**:
