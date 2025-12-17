# 🎵 Music App - Flutter

A full-stack music streaming application built with Flutter and FastAPI, featuring user authentication, music playback, favorites management, and song uploads.

## 📱 Features

### Client (Flutter)
- **User Authentication**: Secure signup and login system with persistent sessions
- **Music Player**: 
  - Full-featured music player with play/pause controls
  - Background audio playback support
  - Real-time progress tracking with seekable slider
  - Album artwork display with gradient themes
  - Favorite/unfavorite songs functionality
- **Music Library**:
  - Browse all available songs
  - Recently played songs grid view
  - Personal favorites library
- **Upload Songs**: 
  - Upload custom songs with metadata (artist name, song name)
  - Audio waveform preview before upload
  - Custom thumbnail selection
  - Color picker for song theme customization
- **Modern UI**:
  - Animated transitions and hero animations
  - Dynamic color themes based on currently playing song
  - Bottom navigation with persistent music slab
  - Responsive design

### Server (FastAPI)
- RESTful API for authentication and song management
- PostgreSQL database integration
- File upload handling for songs and thumbnails
- User favorites management

## 🛠️ Tech Stack

### Frontend
- **Framework**: Flutter (Dart)
- **State Management**:  Riverpod
- **Audio Playback**: 
  - `just_audio` - Audio playback engine
  - `just_audio_background` - Background playback support
  - `audio_service` - Platform audio integration
  - `audio_waveforms` - Waveform visualization
- **Storage**: 
  - `hive` - Local NoSQL database
  - `isar` - High-performance local database
  - `shared_preferences` - Key-value storage
- **UI Components**:
  - `flex_color_picker` - Color selection
  - `dotted_border` - Custom borders
- **Utilities**:
  - `http` - API communication
  - `fpdart` - Functional programming utilities
  - `file_picker` - File selection
  - `path_provider` - Path management

### Backend
- **Framework**: FastAPI (Python)
- **Database**: PostgreSQL (with SQLAlchemy)
- **Server**:  Uvicorn

## 📂 Project Structure

```
musicapp-flutter/
├── client/                 # Flutter application
│   ├── lib/
│   │   ├── core/          # Core utilities, themes, and providers
│   │   ├── features/      # Feature modules
│   │   │   ├── auth/      # Authentication (signup/login)
│   │   │   └── home/      # Home, library, music player, upload
│   │   └── main.dart      # App entry point
│   └── pubspec.yaml       # Flutter dependencies
│
└── server/                # FastAPI backend
    ├── routes/            # API routes (auth, song)
    ├── models/            # Database models
    ├── database.py        # Database configuration
    └── main.py            # Server entry point
```

## 🚀 Getting Started

### Prerequisites
- Flutter SDK (>=3.4.4 <4.0.0)
- Python 3.8+
- PostgreSQL

### Backend Setup

1. Navigate to the server directory: 
```bash
cd server
```

2. Install Python dependencies:
```bash
pip install -r requirements.txt
```

3. Configure your database connection in `database.py`

4. Run the server:
```bash
python main.py
```

The API will be available at `http://localhost:8000`

### Frontend Setup

1. Navigate to the client directory:
```bash
cd client
```

2. Install Flutter dependencies:
```bash
flutter pub get
```

3. Run code generation (if needed):
```bash
flutter pub run build_runner build
```

4. Run the app:
```bash
flutter run
```

## 🎨 Features in Detail

### Authentication
- Persistent login sessions using SharedPreferences
- Automatic navigation based on authentication state
- User registration and login

### Music Playback
- Stream audio from remote URLs
- Background playback continues when app is minimized
- Position tracking and seeking
- Play/pause controls
- Visual progress indicator

### Library Management
- View all uploaded songs
- Filter by favorites
- Recently played songs section
- Dynamic theming based on song colors

### Song Upload
- Pick audio files from device
- Select custom thumbnails
- Visual audio waveform preview
- Color theme selection
- Metadata input (artist, song name)

## 📝 API Endpoints

- `POST /auth/signup` - User registration
- `POST /auth/login` - User authentication
- `GET /song/*` - Song-related endpoints
- Additional endpoints in `/routes` directory

## 🎯 Future Enhancements

Potential features to consider:
- Playlist creation and management
- Search functionality
- Social features (sharing, following)
- Offline playback
- Queue management
- Previous/next song navigation
- Shuffle and repeat modes
- Connect to external devices
- Audio equalizer

## 📄 License

This project does not currently have a license specified. 

## 👤 Author

**f8th**

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! 

---

Built with ❤️ using Flutter and FastAPI
