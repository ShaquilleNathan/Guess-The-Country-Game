# 🌍 Guess The Country - React Native Game

An experimental mobile game built with **React Native** and **Realm**, where users guess the name of a country based on its famous landmarks. This app is written primarily in **JavaScript** and runs in **debug mode** via **Metro bundler**. The project is still in early development and is meant to be explored and modified further.

> ⚠️ **Disclaimer:**  
> This project is experimental and intended for learning, exploration, and extension. Feel free to fork, modify, and expand the functionality!

---

## 🎮 Gameplay

- A random landmark image is shown to the user.
- The user must guess the country that the landmark belongs to.
- **Answers are not case-sensitive** (e.g., "france", "FRANCE", and "France" are all valid).
- If the guess is **correct**, the player receives **+10 points**.
- If the guess is **incorrect**, no points are awarded, and the game moves to the next landmark.
- Once the player reaches **50 points**, a **"You Win"** screen appears.
- The user can then tap **"Play Again"** to restart the game.

<div align="center">
  <img src="https://i.postimg.cc/nLLVJnY4/Whats-App-Image-2025-05-18-at-15-30-08.jpg" alt="Demo Image" style="width: 200px; height: auto;" />
  <img src="https://i.postimg.cc/LXYHJvWh/Whats-App-Image-2025-05-18-at-15-30-08-1.jpg" alt="Demo Image" style="width: 200px; height: auto;" />
  <img src="https://i.postimg.cc/wxNqHfJG/Whats-App-Image-2025-05-18-at-15-30-09.jpg" alt="Demo Image" style="width: 200px; height: auto;" />
  <img src="https://i.postimg.cc/QxrXMQJx/Whats-App-Image-2025-05-18-at-15-30-09-1.jpg" alt="Demo Image" style="width: 200px; height: auto;" />
</div>

---

## ⚙️ Tech Stack

- [React Native](https://reactnative.dev/)
- [Realm](https://www.mongodb.com/docs/realm/sdk/react-native/)
- JavaScript (ES6+)
- Metro bundler (debug mode)

---

## 🚀 Getting Started

### 1. Clone this repository

```bash
git clone https://github.com/ShaquilleNathan/Guess-The-Country-Game.git
cd your-project-name
```

### 2. Install React Native CLI (if not already installed)
```bash
npm install -g react-native-cli
```

### 3. Install project dependencies
```bash
npm install
```
Or if you're using Yarn:
```bash
yarn install
```
Make sure all dependencies are the same as `package.json`.

### 4. Set up the development environment
Follow the official React Native Environment Setup.
Make sure to select the React Native CLI Quickstart tab, not Expo.

### 5. Start Metro Bundler
```bash
npx react-native start
```
This starts the Metro bundler in your terminal and prepares the app for debugging.

### 6. Run the app on an emulator or real device
Android emulator:
```bash
npx react-native run-android
```
iOS simulator (macOS only):
```bash
npx react-native run-ios
```
Make sure your emulator/device is connected and detected by adb devices (for Android).

### ✅ Optional: Creating New Project (for fresh setup)
If you're starting from scratch, you can initialize a new project with this command:
```bash
npx react-native@(your react-native version) init (your project name) --version (your react-native version)
```
Then follow steps 2-4 above.

---
## 📝 Notes
- This app is currently running in **debug mode**, not release. Expect possible performance issues and unoptimized builds.
- The app uses **Realm** for local data storage. If you're unfamiliar with Realm, please refer to the [official Realm React Native docs](https://www.mongodb.com/docs/realm/sdk/react-native/).
- Landmark images are stored locally in the `assets/` folder. You can add or replace images to expand the country database.
- The answer comparison logic uses a **case-insensitive match** (`toLowerCase()`) to validate user guesses.
- The UI is kept simple and minimal for readability and quick iteration. Feel free to improve the styling using libraries like `react-native-paper` or `styled-components`.
- The scoring system is basic (correct = +10 points, incorrect = 0). You can modify the logic to include negative points, streak bonuses, etc.
- If you encounter issues with Realm setup or build errors on Android, try the following:
  - Run `cd android && ./gradlew clean` then `cd ..`
  - Make sure all native dependencies are properly linked and rebuilt.
  - Restart Metro bundler using `npx react-native start --reset-cache`

> 🔧 **Debug tip:** If the "You Win" screen appears unexpectedly at the start, double-check the initial state values for score in your game screen or Realm database initialization.

---
