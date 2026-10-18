# Pomodorolist

A minimal, free focus app with custom Pomodoro timers, named sessions, daily streaks and focus graphs. Log in on any device and your progress follows you.

**Live app:** https://siverieg.github.io/Pomodorolist-V1.0/

<!-- Add screenshots here later: drag images into this editor -->

## Features

- **Custom Pomodoro timers:** set your own focus, short break and long break lengths, and save them as presets
- **Named sessions:** label what you're working on (e.g. "Physics – Rotation")
- **Recently used:** jump back into recent session names and presets in one tap
- **Daily streaks:** hit your daily focus goal to keep your streak going
- **Focus graphs:** today's timeline, weekly bars, a monthly heatmap and a yearly contribution grid
- **Cross-device sync:** log in with a username and password, and your sessions, streaks and settings sync between devices
- **Works offline:** keep focusing without internet; it syncs when you're back online
- **Light and dark mode**, plus JSON export/import for backups

## How it works (local vs. cloud)

The app itself runs entirely in your browser. There's no custom server.

- **With an account:** your data is stored in **Google Firebase** (Authentication + Firestore database). A copy is also kept in your browser, so the app stays fast and works offline.
- **Without an account:** choose **"Use on this device only"** on the login screen. Everything stays in your browser (localStorage) and nothing is uploaded.

The Firebase config in the code is meant to be public. Access is protected by Firestore security rules, so each user can only read and write their own data.

## Privacy

- No ads, no analytics, no tracking.
- Passwords are handled by Firebase Authentication and never stored by the app.
- You can erase all your data from Settings at any time.

## Known limitations

- **No password reset yet.** Accounts use a username, not an email, so pick a password you'll remember.
- **Running timers don't sync live.** A timer runs on the device you started it on; completed sessions sync everywhere.

## Built with

HTML, CSS and vanilla JavaScript in a single file, with Firebase (Auth + Firestore), Chart.js and GitHub Pages hosting.

## Feedback

Found a bug or have an idea? [Open an issue](https://github.com/siverieg/Pomodorolist-V1.0/issues). All feedback is welcome!
