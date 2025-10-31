# Mobile Development Setup with Expo (React Native)

A smooth mobile dev workflow requires more resources than web. This README sets up Expo Go for testing React Native apps on physical devices and, optionally, the iOS Simulator.

## Prerequisites
- Node.js LTS
- VS Code (recommended)
- macOS, Linux, or Windows
- Stable Wi‑Fi network shared by your computer and phone
- Expo account (free)

## Why Expo Go
Emulators/simulators can be heavy and fragmented. Expo Go lets you run React Native apps directly on physical devices (iOS and Android) with minimal setup.

## Install Expo Go
- Visit https://expo.dev/go
- Select the latest SDK
- Install for your device:
    - Android: Google Play Store
    - iOS: Apple App Store
- Open Expo Go and sign in (or create an account)

## iOS Setup

### Run on a physical iPhone/iPad
- Install Expo Go from the App Store.
- Ensure your iOS device and development machine are on the same Wi‑Fi.
- Create a new project or use an existing one:
    - npx create-expo-app MyApp
    - cd MyApp
    - npx expo start
- In the dev server UI/CLI:
    - If LAN fails on iOS, switch to Connection: Tunnel.
- On your iPhone:
    - Open Expo Go and sign in with the same account (recommended), then tap the project under Recent, or
    - Scan the QR code shown in your terminal/browser. On iOS, use the Camera app or the QR scanner inside Expo Go.

Notes:
- iOS LAN discovery may be blocked by network firewalls. Tunnel mode is the most reliable on mixed networks.
- Keep Expo Go and iOS updated for best compatibility.

### Run on the iOS Simulator (macOS only)
- Install Xcode from the Mac App Store.
- Open Xcode once to complete setup and accept licenses.
- Install Command Line Tools in Xcode > Settings > Locations.
- From your project:
    - npx expo start --ios
    - This launches the iOS Simulator and installs the Expo Go client automatically.
- The Simulator does not require a physical iPhone and works only on macOS.

## Android (optional)
- Install Expo Go from Google Play.
- npx expo start
- Scan the QR code in Expo Go or press a in the terminal to open an Android emulator if installed.

## Troubleshooting
- App not loading on iOS (LAN): switch to Tunnel in the dev server.
- Stuck cache or mismatched SDK: npx expo start -c
- Same network requirement: ensure both devices share the same Wi‑Fi and that VPNs/firewalls are off or allow local traffic.
- Reinstall/update Expo Go if the SDK is outdated.

## Document Your Setup
Record:
- Device model and OS version
- Expo SDK version
- Connection type used (LAN or Tunnel)
- Issues encountered and fixes
- Screenshots of Expo Go running your app (optional)
- Update this README as you iterate

You are ready to build and test React Native apps with Expo on iOS and Android.