# Melodix Music App

A Vite + React + TypeScript music app with Firebase-backed auth/storage support and a demo fallback for local development.

## Firebase setup

1. Copy `.env.example` to `.env`.
2. Replace the values with your Firebase project credentials.
3. Ensure the variables are prefixed with `VITE_`.
4. Rebuild and redeploy the app after changing them.

Example:

```bash
cp .env.example .env
```

The required environment variables are:

```env
VITE_FIREBASE_API_KEY="..."
VITE_FIREBASE_AUTH_DOMAIN="..."
VITE_FIREBASE_PROJECT_ID="..."
VITE_FIREBASE_STORAGE_BUCKET="..."
VITE_FIREBASE_MESSAGING_SENDER_ID="..."
VITE_FIREBASE_APP_ID="..."
```

## Static hosting / uploaded website

If you are uploading a built static site to a host that does not preserve `.env` files, either:

- set these values in your host's environment settings before running the production build, or
- create a runtime config file like `public/firebase-config.js` using the example at `public/firebase-config.example.js`.

The app will automatically read `window.__FIREBASE_CONFIG__` if present.

## Demo mode

If Firebase is not configured, the app intentionally runs in local demo mode and shows built-in sample tracks instead of live Firebase data.

## Development

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
```
