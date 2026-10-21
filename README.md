# Pomodorolist 🍅

A free, minimal focus timer that turns studying into a game. Custom Pomodoro timers, streaks and stats, a tomato garden, weekly boss battles, friends and leaderboards, and a friendly tomato mascot called Pomeo. Log in on any device and your progress follows you.

**Live app:** https://siverieg.github.io/Pomodorolist-V1.0/

<!-- Add screenshots here: drag images into this editor -->

## Why Pomodorolist?

Most focus apps lock streaks, stats, sync and themes behind a subscription. Pomodorolist gives you all of it for free, with no ads and no tracking. If you just want a clean timer, **True Minimalist** mode hides all the game elements.

## Features

### Focus
- **Custom Pomodoro timers:** your own focus and break lengths, saved as presets
- **Named sessions and subtasks:** label what you're working on and tick off small goals during the session
- **Distraction parking lot:** jot down a distracting thought in two seconds without stopping the timer, and review it on your break
- **Ambient sounds:** rain, brown noise, café, ocean and more
- **Energy check-ins:** rate how focused you felt after a session and discover when you focus best

### Plan
- **Reminders:** schedule study sessions; Pomeo reminds you 5–30 minutes before, with snooze and repeat
- **Add to calendar:** export reminders to your phone's calendar (.ics or Google Calendar)
- **Spaced revision:** revise topics at 1, 3, 7, 21 and 45 days, with Hard/Easy adjustments
- **Exam countdown:** days left plus how many focus hours you're on track for

### Stats
- **Daily streaks** and a daily focus goal
- **Focus graphs:** today's timeline, weekly bars, monthly heatmap, yearly contribution grid
- **Insights:** best time of day, best session length and best days, from your energy check-ins
- **Wrapped:** a monthly and yearly story-style recap with a shareable card

### Play
- **Tomato garden:** every session grows a plant; quitting early leaves a wilted one
- **Weekly boss battles:** beat a new boss each week with focus minutes, solo or with a squad of friends
- **XP, levels and 9 tiers:** Novice → Apprentice → Scholar → Focused → Disciplined → Expert → Master → Grandmaster → Legend
- **Coins and a cosmetic shop:** themes, timer sounds, ambient sounds, timer styles, fonts, effects, profile pictures, Pomeo outfits and Streak Freezes (cosmetic only; nothing affects your stats)
- **Achievements, daily login rewards and a streak aura** around your profile

### Pomeo 🍅
- A tomato mascot who reacts when you tap or pet him, cheers you on, reminds you of sessions and gently suggests sleep late at night
- Dress him up with outfits from the shop

### Friends
- **Add friends** by username or invite link, with requests, remove and block
- **Friend profiles:** streak, level, 7-day chart, heatmap and recent sessions, plus a side-by-side compare
- **Leaderboards:** Friends and Global (opt-in), for Daily, Weekly, Monthly and Lifetime
- **Focusing now, kudos, nudges, friend streaks and weekly challenges**

### Experience
- **Interactive tutorial** with Pomeo for new users, and one-time tips
- **True Minimalist mode:** hides all gamification for a clean, calm timer
- **Glossed Interface:** a frosted-glass look (Off / Lite / Full)
- **Smooth animations and soft interface sounds,** each adjustable or switchable off
- **Inbox** for friend requests, kudos, reminders and rewards in one place
- **Command palette** (Cmd/Ctrl+K) and keyboard shortcuts
- **Light and dark mode,** offline support and JSON export/import

## Keyboard shortcuts

| Key | Action |
|---|---|
| Space | Start / pause |
| R | Reset |
| S | Skip |
| P | Parking lot |
| T | Add subtask |
| N | Session name |
| Cmd/Ctrl + K | Command palette |
| ? | Show all shortcuts |

## How it works (local vs. cloud)

The app runs in your browser as a single HTML file, with no custom server.

- **With an account:** data is stored in **Google Firebase** (Authentication + Firestore). A copy is kept in your browser so the app stays fast and works offline.
- **Without an account:** choose **"Use on this device only"**. Everything stays in your browser and nothing is uploaded. Friends and leaderboards need an account.

The Firebase config in the code is meant to be public. Access is controlled by Firestore security rules: your private data is readable only by you, and friend activity only by accepted friends.

## Privacy and safety

- No ads, no analytics, no tracking
- Passwords are handled by Firebase Authentication and never stored by the app
- Usernames and drawn avatars only: no real names, emails or photo uploads shown to others
- **You control what friends see:** session names, activity and "focusing now" status can each be hidden
- **The Global leaderboard is opt-in** and off by default
- **No chat or free-text messages,** only preset reactions and nudges
- Block anyone at any time, and erase all your data from Settings

## Known limitations

- **No password reset:** accounts use a username, not an email, so pick a password you'll remember
- **Usernames can't be changed,** because the username is your login
- **Reminders only fire while the app is open** (a background tab is fine). Use **Add to calendar** for reminders when the app is closed.
- **Running timers stay on one device;** completed sessions sync everywhere
- **Leaderboards can't be fully cheat-proof** without a server; security rules block obvious cheating, but not every case
- If you opt in to Global, someone who blocked you can still see your leaderboard row, but not your profile or activity

## Built with

- HTML, CSS and vanilla JavaScript in a single file
- Firebase Authentication + Cloud Firestore (free Spark plan)
- Chart.js for graphs, Web Audio API for every sound
- Hosted on GitHub Pages

## Run your own copy

1. Fork this repo and enable **GitHub Pages** (Settings → Pages → main branch).
2. Create a Firebase project, add a web app, and paste your `firebaseConfig` into `index.html` (search for `EDIT HERE`).
3. Enable **Email/Password** sign-in in Firebase Authentication.
4. Create a Firestore database, publish the rules from `firestore.rules`, and create the indexes listed in `firestore.indexes.json`.
5. Add your GitHub Pages domain under Authentication → Settings → **Authorized domains**.

## Feedback and contact

- **Bugs and feature ideas:** [open an issue](https://github.com/siverieg/Pomodorolist-V1.0/issues)
- **Contact:** siverieg.p@gmail.com

---

© 2026 Pomodorolist · Made by [siverieg](https://github.com/siverieg)
