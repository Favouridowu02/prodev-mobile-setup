# React Native + TypeScript + NativeWind + Expo

A minimal, opinionated starter README for building cross-platform mobile apps with React Native, TypeScript, NativeWind (utility-first styling), and the Expo framework.

## Summary
This stack provides:
- Cross-platform native UI (iOS & Android) with React Native
- Type safety and better DX with TypeScript
- Utility-first styling using NativeWind (Tailwind-like for RN)
- Fast iteration, device testing, and OTA updates with Expo

## Features
- Single codebase for iOS and Android
- Predictable types and autocompletion
- Fast styling with utility classes
- Easy device testing via Expo Go

## Prerequisites
- Node.js v16+
- npm or yarn
- Expo CLI (optional): npm install -g expo-cli
- A code editor (e.g., VS Code)
- Expo Go app on your device (for quick testing)

## Quick start
Create a new Expo app (with TypeScript):
```bash
npx create-expo-app MyApp --template expo-template-blank-typescript
cd MyApp
```

Start the dev server:
```bash
npm start   # or yarn start
# then scan the QR code with Expo Go or run on an emulator
```

## Add NativeWind (basic)
1. Install packages:
```bash
npm install nativewind tailwindcss
npx tailwindcss init -p
```
2. Configure `tailwind.config.js` (ensure content includes your source files):
```js
module.exports = {
    content: ["./**/*.{js,jsx,ts,tsx}"],
    theme: { extend: {} },
    plugins: [],
};
```
3. Enable the NativeWind Babel plugin in `babel.config.js`:
```js
module.exports = function(api) {
    api.cache(true);
    return {
        presets: ['babel-preset-expo'],
        plugins: ['nativewind/babel'],
    };
};
```
4. Example usage in `App.tsx`:
```tsx
import React from 'react';
import { View, Text } from 'react-native';

export default function App() {
    return (
        <View className="flex-1 items-center justify-center bg-white">
            <Text className="text-lg font-bold">Hello, NativeWind + TypeScript!</Text>
        </View>
    );
}
```

## TypeScript
- create-expo-app with the TypeScript template adds a working `tsconfig.json`.
- Use typings for React Native and any native modules you add.

## Useful npm scripts
- npm start — start Expo dev server
- npm run android — open Android emulator (if configured)
- npm run ios — open iOS simulator (macOS only)
- npm run web — run a web build (Expo web support)

## Tips
- Use Expo Go for quick device testing; use custom dev clients when adding native modules.
- Keep Tailwind classes readable by grouping and using design tokens when needed.
- Use ESLint + Prettier and enable TypeScript strictness incrementally.

## Next steps
- Add navigation (React Navigation)
- Integrate state management (Context / Redux / Recoil / Zustand)
- Configure CI, testing, and app signing for production builds

License: choose one for your project (e.g., MIT)