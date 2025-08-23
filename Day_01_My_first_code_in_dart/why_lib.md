# Why is `main.dart` inside the `lib` folder?

In Flutter projects, the **`lib` folder** is the main place where your application source code lives.  

---

## Key Reasons

1. **Flutter Convention**  
   - Flutter expects the app entry point (`main.dart`) inside `lib`.  
   - `flutter run` looks for `lib/main.dart` by default.

2. **Clean Project Structure**  
   - `lib` is for Dart app code (UI, logic).  
   - `android` and `ios` are for platform-specific code.  
   - `test` is for tests.  
   Keeping all app code in `lib` makes the project organized.

3. **Easier Imports**  
   - Dart uses `lib` as the package root.  
   - Files inside `lib` can be imported like:  
     ```dart
     import 'package:your_app_name/file.dart';
     ```
   - If `main.dart` were outside `lib`, imports would be more complicated.

4. **For Distribution & Packages**  
   - When publishing a package, only the `lib` folder is shared.  
   - Keeping code in `lib` follows Dart’s package structure standards.

---

## In Short
- Flutter tools expect `main.dart` inside `lib`.  
- It keeps your project clean and follows Dart conventions.  
- Makes imports and publishing easier.

---

### Optional Tip: Organizing `lib` for Larger Projects
You can create subfolders inside `lib` for better structure:
- `lib/screens/` → UI screens  
- `lib/models/` → Data models  
- `lib/services/` → APIs and business logic
