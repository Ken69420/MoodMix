# MoodMix

MoodMix is a project that combines a Flask backend with a Flutter-based Android application. The Flask backend provides the necessary APIs and services, while the Flutter app offers a user-friendly interface for Android users.

## Project Structure

```
MoodMix/
├── backend/
│   ├── venv/
│   ├── app/
│   ├── requirements.txt
│   └── run.py
├── moodmix/
│   ├── android/
│   ├── ios/
│   ├── lib/
│   ├── test/
│   ├── pubspec.yaml
│   └── build.gradle
└── README.md
```

## Backend (Flask)

### Setup

1. **Create a virtual environment:**

   ```sh
   python -m venv venv
   ```

2. **Activate the virtual environment:**

   - On Windows:
     ```sh
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```sh
     source venv/bin/activate
     ```

3. **Install dependencies:**

   ```sh
   pip install -r requirements.txt
   ```

4. **Create a `.env` file to store your Spotify API credentials:**

   Create a file named `.env` in the `backend/` directory and add your Spotify API credentials:

   ```
   SPOTIFY_CLIENT_ID=your_spotify_client_id
   SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
   ```

5. **Load the environment variables:**

   Ensure that your Flask application loads the environment variables from the `.env` file. You can use the `python-dotenv` package for this. Install it by adding it to your `requirements.txt`:

   ```
   python-dotenv
   ```

   Then, in your `run.py` or application initialization code, add:

   ```python
   from dotenv import load_dotenv
   import os

   load_dotenv()
   spotify_client_id = os.getenv('SPOTIFY_CLIENT_ID')
   spotify_client_secret = os.getenv('SPOTIFY_CLIENT_SECRET')
   ```

6. **Run the Flask application:**

   ```sh
   python run.py
   ```

### Key Files

- `app/`: Contains the Flask application code.
- `requirements.txt`: Lists the dependencies for the Flask application.
- `run.py`: Entry point for running the Flask application.

## Frontend (Flutter)

### Setup

1. **Install Flutter:**

   Follow the instructions on the [official Flutter website](https://flutter.dev/docs/get-started/install) to install Flutter on your machine.

2. **Navigate to the Flutter project directory:**

   ```sh
   cd moodmix
   ```

3. **Get the dependencies:**

   ```sh
   flutter pub get
   ```

4. **Run the Flutter application:**

   ```sh
   flutter run
   ```

### Key Files

- `lib/`: Contains the Dart code for the Flutter application.
- `pubspec.yaml`: Lists the dependencies for the Flutter application.
- `android/`: Contains the Android-specific code and configurations.
- `ios/`: Contains the iOS-specific code and configurations.
