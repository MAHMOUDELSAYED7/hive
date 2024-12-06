# HiveDb - Hive Database Handler for Flutter

This Flutter project provides a reusable, singleton class, **HiveDb**, to handle Hive database operations. The class manages the initialization, configuration, and CRUD operations on a database, allowing developers to define their own data models and manage user accounts, pizzas, and invoices dynamically.

## Features

- **Singleton Pattern**: Uses a single database instance throughout the app.
- **Initialization**: Sets up the database and opens necessary boxes.
- **Table Management**: Allows custom table definitions for box creation.
- **CRUD Operations**: Provides methods for creating, reading, updating, and deleting records.
- **User Management**: Supports user insertion and retrieval with validation.
- **Invoice Management**: Saves invoices and generates the next invoice number.

## Getting Started

### Prerequisites

Ensure you have Flutter installed and set up on your machine. You will also need to include the following dependencies in your `pubspec.yaml` file:

```yaml
dependencies:
  flutter:
    sdk: flutter
  hive: ^2.0.0
  hive_flutter: ^1.1.0
  path_provider: ^2.0.10

dev_dependencies:
  build_runner: ^2.4.11
  hive_generator: ^2.0.1
```
### Installation
1. Clone the repository or copy the HiveDb class into your Flutter project.

2. Run the build_runner command in your terminal:
```
dart run build_runner build
```
3. Initialize the database in your main application file. You can do this using an anonymous object:

```dart
Future<void> main() async {
  WidgetsFlutterBinding.ensureInitialized();
  await HiveDb().initializeDatabase();
  runApp(MyApp());
}
```
## Notice

You can easily customize the database structure by modifying the user, pizza, and invoice classes as needed. This makes `HiveDb` suitable for a variety of applications, from simple projects to more complex systems with unique data requirements.
## Contact

For any questions or feedback, please reach out via email: [mahmoudelsayed.dev@gmail.com](mahmoudelsayed.dev@gmail.com)
