# 🚀 React Native Setup & Hello World App

This repository documents my step-by-step experience setting up a React Native environment and running a simple **Hello World** application on an Android device.

---

## 📌 Prerequisites

Before starting, make sure you have installed:

* Node.js (LTS version)
* npm or yarn
* Java JDK 17+
* Android Studio (with SDK & Emulator)
* VS Code (recommended IDE)

---

## ⚙️ React Native Environment Setup

### 1. Install React Native CLI

```bash
npx react-native init MyApp
```

---

### 2. Navigate to Project

```bash
cd MyApp
```

---

### 3. Start Metro Server

```bash
npx react-native start
```

---

### 4. Run App on Android

Open a new terminal and run:

```bash
npx react-native run-android
```

---

## 📱 Project Structure

```
MyApp/
 ├── android/        # Native Android code
 ├── ios/            # iOS code
 ├── App.tsx         # Main entry UI
 ├── index.js        # App entry point
 ├── package.json
```

---

## 🧠 How React Native Works

```
index.js → App.tsx → UI Components
```

* `index.js` registers the app
* `App.tsx` is the main UI file

---

## ✍️ Hello World Example

Update `App.tsx`:

```tsx
import React from 'react';
import { View, Text, StyleSheet } from 'react-native';

const App = () => {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Hello World 🚀</Text>
    </View>
  );
};

export default App;

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
  },
  title: {
    fontSize: 24,
    fontWeight: 'bold',
  },
});
```

---

## 🔄 Hot Reload

* Press `r` in Metro terminal
* Or save file → auto reload

---

## ⚠️ Common Issues & Fixes

### SDK not found

Set environment variable:

```
ANDROID_HOME
```

---

### Java version error

Use JDK 17:

```
java -version
```

---

### Gradle build issues

```
cd android
gradlew clean
cd ..
```

---

## 🎯 Key Learnings

* React Native uses `App.tsx` as main UI
* No need to run individual files
* Metro server handles live updates
* Android setup is crucial for build success

---

## 🚀 Outcome

Successfully built and ran a **Hello World app** on a real Android device 🎉

---

## 🙌 Conclusion

This setup helped me understand:

* React Native project structure
* How apps are executed
* Environment configuration

---

⭐ If this helps, feel free to star the repo!
