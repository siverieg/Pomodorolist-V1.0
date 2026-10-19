# Pomodorolist

A minimal, free focus app with custom Pomodoro timers, named sessions, streaks, focus graphs, levels, a cosmetic shop, friends and leaderboards. Log in on any device and your progress follows you.

**Live app:** https://siverieg.github.io/Pomodorolist-V1.0/

<!-- Add screenshots here: drag images into this editor -->

## Why Pomodorolist?

Most focus apps lock streaks, stats, sync and themes behind a subscription. Pomodorolist gives you all of it for free, with no ads and no tracking.

## Features

### Focus
- **Custom Pomodoro timers:** set your own focus, short break and long break lengths, and save them as presets
- **Named sessions:** label what you're working on (e.g. "Physics – Rotation")
- **Recently used:** jump back into recent session names and presets in one tap
- **Ambient sounds:** rain, brown noise, café, ocean and more while you focus
- **Notifications and sounds** when a session or break ends

### Stats and streaks
- **Daily streaks:** hit your daily focus goal to keep your streak going
- **Focus graphs:** today's timeline, weekly bars, a monthly heatmap and a yearly contribution grid
- **Totals and averages:** best day, top subjects and lifetime focus hours

### Progression
- **XP for focus time:** 1 XP per minute focused, with a bonus for long sessions
- **Coins for completed sessions,** daily goals and streak milestones
- **9 level tiers with badges:** Novice → Apprentice → Scholar → Focused → Disciplined → Expert → Master → Grandmaster → Legend
- **Achievements** for milestones like 100 sessions, a 30-day streak or early-morning focus
- **Cosmetic shop:** timer sounds, ambient sounds, themes, timer ring styles, fonts, completion effects, profile flair and Streak Freezes. Everything in the shop is cosmetic and never affects your stats.
- **Hide gamification** in Settings if you just want a plain timer

### Friends and leaderboards
- **Add friends** by username or invite link, with friend requests, remove and block
- **Friend profiles:** see their streak, level, 7-day focus chart, 12-week heatmap and recent sessions
- **Compare** your week with a friend's, side by side
- **Leaderboards:** Friends and Global, for Daily, Weekly, Monthly and Lifetime
- **Focusing now:** see when friends are in a session
- **Kudos and nudges:** send a 🔥 👏 💪 ⭐ reaction or a "Time to focus? 👀" nudge
- **Friend streaks:** build a shared streak when you both hit your daily goal
- **Weekly challenges:** e.g. "Focus 10 hours this week", joined with friends for bonus coins
- **Weekly recap card** you can share as an image

### Everything else
- **Cross-device sync:** sessions, streaks, levels, coins, purchases and settings sync between devices
- **Works offline:** keep focusing without internet; it syncs when you're back online
- **Light and dark mode,** and JSON export/import for backups

## How it works (local vs. cloud)

The app runs entirely in your browser as a single HTML file, with no custom server.

- **With an account:** data is stored in **Google Firebase** (Authentication + Firestore). A copy is kept in your browser so the app stays fast and works offline.
- **Without an account:** choose **"Use on this device only"** on the login screen. Everything stays in your browser (localStorage) and nothing is uploaded. Friends and leaderboards need an account.

The Firebase config in the code is meant to be public. Access is controlled by Firestore security rules: your private data is readable only by you, and friend activity only by accepted friends.

## Privacy and safety

- No ads, no analytics, no tracking.
- Passwords are handled by Firebase Authentication and never stored by the app.
- Usernames only: no real names, emails or photos are shown to others.
- **You control what friends see:** hide session names, hide your activity, or hide your "focusing now" status.
- **The Global leaderboard is opt-in** and off by default.
- **No chat or free-text messages,** only preset reactions and nudges.
- Block anyone at any time.
- You can erase all your data from Settings.

## Known limitations

- **No password reset:** accounts use a username, not an email, so pick a password you'll remember.
- **Usernames can't be changed,** because the username is your login.
- **Running timers stay on one device.** Completed sessions sync everywhere.
- **Leaderboards can't be fully cheat-proof** without a server. Security rules block obvious cheating (impossible session lengths, more minutes than real time allows), but not every case.
- If you opt in to Global, someone who blocked you can still see your leaderboard row, but not your profile or activity.

## Built with

- HTML, CSS and vanilla JavaScript in a single file
- Firebase Authentication + Cloud Firestore (free Spark plan)
- Chart.js for graphs, Web Audio API for all sounds
- Hosted on GitHub Pages

## Run your own copy

1. Fork this repo and enable **GitHub Pages** (Settings → Pages → main branch).
2. Create a Firebase project, add a web app, and paste your `firebaseConfig` into `index.html` (search for `EDIT HERE`).
3. Enable **Email/Password** sign-in in Firebase Authentication.
4. Create a Firestore database, then publish the rules from `firestore.rules` and create the indexes listed in `firestore.indexes.json`.
5. Add your GitHub Pages domain under Authentication → Settings → **Authorized domains**.

## Feedback

Found a bug or have an idea? [Open an issue](https://github.com/siverieg/Pomodorolist-V1.0/issues). All feedback is welcome!

---

Built by a Class 11 student who wanted a free way to track study hours.
