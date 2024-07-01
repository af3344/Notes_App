# Notes_App
# Notes App Assignment 3

## Overview

This project is a simple notes application built for Android using Java. It leverages Firebase Realtime Database to store and retrieve notes. The main features of the app include creating, viewing, and listing notes with a timestamp.

## Features

- Add new notes with a title, content, and timestamp.
- Store notes in Firebase Realtime Database.
- Retrieve and display notes using a RecyclerView.
- Ensure smooth user interface integration with system bars using Edge-to-Edge display.

## Requirements

- Android Studio
- Firebase project setup with Realtime Database enabled
- Internet connection

## Setup and Configuration

1. **Clone the Repository:**
   ```sh
   git clone https://github.com/af3344/notes_app_assignment_3.git
   cd notes_app_assignment_3
   ```

2. **Open the Project in Android Studio:**
   - Launch Android Studio.
   - Select `Open an existing Android Studio project`.
   - Navigate to the cloned repository and open it.

3. **Configure Firebase:**
   - Go to the Firebase Console and create a new project or use an existing one.
   - Add your Android app to the Firebase project.
   - Download the `google-services.json` file and place it in the `app` directory of your project.
   - Add Firebase to your Android project by following the instructions in the Firebase Console.

4. **Add Dependencies:**
   Ensure your `build.gradle` files are configured correctly with Firebase and other necessary dependencies.
   ```gradle
   // Project-level build.gradle
   dependencies {
       classpath 'com.google.gms:google-services:4.3.3'
   }

   // App-level build.gradle
   dependencies {
       implementation 'com.google.firebase:firebase-database:19.7.0'
       implementation 'com.firebaseui:firebase-ui-database:8.0.0'
       implementation 'com.google.android.material:material:1.3.0'
   }

   apply plugin: 'com.google.gms.google-services'
   ```

5. **Run the App:**
   - Connect your Android device or start an emulator.
   - Click on the `Run` button in Android Studio to build and launch the app.

## Code Structure

- **MainActivity.java:**
  - Handles the main UI and user interactions.
  - Contains logic for adding new notes and displaying them in a RecyclerView.

- **NotesAdapter.java:**
  - Custom adapter for binding note data to RecyclerView items.

- **Note.java:**
  - Model class representing a note with a title, content, and timestamp.

- **activity_main.xml:**
  - Layout file for the main activity, including RecyclerView and FloatingActionButton.

- **add_new_note_dialog_design.xml:**
  - Layout file for the dialog used to add a new note.

## Usage

1. **Adding a New Note:**
   - Click on the FloatingActionButton (`+` button) to open the add new note dialog.
   - Enter the note title and content.
   - Click `Save` to store the note in Firebase Realtime Database.
   - The new note will be displayed in the RecyclerView.

2. **Viewing Notes:**
   - Notes stored in Firebase Realtime Database are automatically retrieved and displayed in the RecyclerView.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Contact

For any issues or contributions, please contact [Arooj Naseer](https://github.com/af3344).
