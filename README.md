# MicroVision

A mobile app for a microplastic detection system, built as an undergraduate thesis in Computer Engineering at the University of St. La Salle, Bacolod City.

The system uses a YOLO-based object detection model running with a Raspberry Pi to detect microplastics under visible and UV light. This repository contains the companion **React Native mobile app**, which handles authentication and data storage through Firebase.



## Overview

Microplastics are difficult to spot and count by eye. This project explores an automated approach: capture a sample image, run it through an object detection model, and present the results in a mobile app.

- **Detection:** YOLO-based object detection model trained on a custom dataset
- **Hardware:** Raspberry Pi integrated with the detection model (device connectivity and system configuration)
- **Mobile app:** React Native (TypeScript) app with Firebase authentication and cloud data storage

## Results

| Metric | Result |
| --- | --- |
| Detection accuracy (visible light) | 95% |
| Detection accuracy (UV light) | 91% |
| Training dataset | 700 self-collected samples, expanded with data augmentation |

## System Overview

```
[Sample] -> [Raspberry Pi + camera] -> [YOLO detection model] -> [Firebase] -> [MicroVision mobile app]
```


## App Features
- User sign-up and login (Firebase Authentication)
- [View detection results]
- [Save and browse past detection records]

## Screenshots



## Tech Stack

- **Mobile:** React Native, TypeScript
- **Backend:** Firebase (Authentication, Cloud Firestore, Cloud Storage)
- **Detection:** YOLO-based object detection model
- **Hardware:** Raspberry Pi
- **Tooling:** Android Studio, VS Code, Git/GitHub

## Repository Structure

```
MicroVision/
├── App.tsx              # App entry point
├── Screens/             # App screens
├── components/          # Reusable UI components
├── assets/fonts/        # Custom fonts
├── images/              # Image assets
├── android/ , ios/      # Native project files
├── __tests__/           # Tests
└── Firebaseconfig.js    # Firebase client configuration
```

## Getting Started

### Prerequisites

- Node.js and npm
- React Native development environment ([setup guide](https://reactnative.dev/docs/set-up-your-environment))
- Android Studio (for Android) or Xcode (for iOS)

### Installation

```bash
git clone https://github.com/Gordinus3/MicroVision.git
cd MicroVision
npm install
```

### Firebase setup

This app uses Firebase. To run it against your own project, replace the values in `Firebaseconfig.js` with the configuration from your Firebase project settings, and enable Authentication, Cloud Firestore, and Cloud Storage in the Firebase console.

### Run the app

```bash
# Start Metro
npm start

# In a second terminal
npm run android    # or: npm run ios
```

## Scope of This Repository

This repository contains the **mobile application only**. The trained YOLO model weights, the dataset, and the Raspberry Pi detection scripts are not included here.

## Authors

- **Emmanuel Clyde Flores**
- **Renan Talorong**
- **Gio Leonard Vasquez**


Undergraduate thesis, BS Computer Engineering, University of St. La Salle, 2026.