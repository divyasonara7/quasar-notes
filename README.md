# Quasar Notes App

The Quasar Notes App is a versatile application that can be used on Android, desktop, and as a Progressive Web App (PWA). It allows users to create and manage their notes effectively. This README provides instructions on how to install, run, and build the Quasar Notes App.

## Demo Link

A live demo of the Quasar Notes App can be accessed [here](https://my-quasar-notes-app.netlify.app/#/).

## Prerequisites

Before running the Quasar Notes App, ensure that you have the following software installed on your machine:

- Node.js (version 12 or higher)
- Yarn (optional, but recommended)

## Installation

To install the dependencies for the Quasar Notes App, navigate to the project's root directory in the command line and run the following command:

```bash
yarn
```

## Development Mode

To start the app in development mode, which enables hot-code reloading and error reporting, use the following command:

```bash
quasar dev
```

This command will launch the app with default settings.

### PWA Development Mode

To run the app as a Progressive Web App (PWA) in development mode, use the following command:

```bash
quasar dev -m pwa
```

### Capacitor Development Mode

To run the app on Android or iOS using Capacitor in development mode, use the following command:

```bash
quasar dev -m capacitor -T [android|ios]
```

Replace `[android|ios]` with your desired target platform.

### Electron Development Mode

To run the app as a desktop application using Electron in development mode, use the following command:

```bash
quasar dev -m electron
```

## Linting

To lint the files in the Quasar Notes App, use the following command:

```bash
yarn run lint
```

This command will analyze the code for any potential errors or style violations.

## Building for Production

To build the Quasar Notes App for production, use the following command:

```bash
quasar build
```

The production-ready app will be generated in the `/dist` directory.

## Configuration

The configuration settings for the Quasar Notes App can be customized by modifying the `quasar.conf.js` file. For detailed instructions on configuring the app, refer to the [Quasar Configuration Guide](https://v2.quasar.dev/quasar-cli/quasar-conf-js).

Feel free to explore and customize the Quasar Notes App to suit your specific needs. Happy note-taking!
