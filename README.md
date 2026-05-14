# Tumble Tier – Online Multiplayer Edition

A real-time multiplayer game built with Matter.js, Firebase Firestore, and Firebase Hosting.

## Project Structure

```
tumble-tier/
├── public/                 # Static files for Firebase Hosting
│   ├── index.html
│   └── styles.css
├── firebase.json          # Firebase Hosting configuration
├── .firebaserc            # Firebase project configuration
├── package.json           # Project metadata and scripts
├── .gitignore            # Git ignore rules
└── README.md             # This file
```

## Setup Instructions

### 1. Install Firebase Tools
```bash
npm install -g firebase-tools
```

### 2. Initialize Firebase (if not already done)
```bash
firebase login
firebase init hosting
```

### 3. Configure Your Firebase Project
- Update `.firebaserc` with your Firebase project ID:
  ```json
  {
    "projects": {
      "default": "your-project-id"
    }
  }
  ```

### 4. Add Your Firebase Config
- In `public/index.html`, replace the Firebase config with your credentials:
  ```javascript
  const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT.firebaseapp.com",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_PROJECT.appspot.com",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID"
  };
  ```

## Local Development

Serve locally with Firebase emulator:
```bash
npm run serve
```

## Deployment

Deploy to Firebase Hosting:
```bash
npm run deploy
```

Or directly with Firebase CLI:
```bash
firebase deploy
```

## Features

- Real-time multiplayer gaming
- Firebase Firestore for game state
- Anonymous authentication via Firebase Auth
- Responsive canvas-based UI
- Room-based matchmaking

## License

MIT
