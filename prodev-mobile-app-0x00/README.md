### Resetting the Project

When you run `npm run reset-project`, the project is reverted to a clean starter state. As part of this process:

- The existing app scaffolding is reset, which can overwrite or remove local changes.
- A new directory named `app-example/` is created. This folder contains example app templates you can choose from.

Important:
- This operation is destructive. Commit or stash your work before running it.
- After the reset, browse `app-example/`, pick a template, and copy its contents into your `app/` directory to continue development.

## Scaffolding Process

Open your terminal and move to your parent project directory:

cd prodev-mobile-setup

Initialize a new Expo project using the latest Expo Router template:

npx create-expo-app@latest .

Modify the Home Screen

Open app/(tabs)/index.tsx.
Locate the default text Welcome!.
Change it to ** First App Created**.

When i ran the `npm run reset-project` it reset the codebase and created a directory called app-example. This contained the examples templates that on can chose from