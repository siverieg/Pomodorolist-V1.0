# Pomodorolist 🍅

A free, minimal focus timer that turns studying into a game. Custom Pomodoro timers, streaks and stats, a tomato garden, weekly boss battles, monthly Pomeo questlines, friends and leaderboards, all with a friendly tomato mascot called Pomeo. Log in on any device and your progress follows you.

**Live app:** https://siverieg.github.io/Pomodorolist-V1.0/
**Try before signing up:** tap **"Preview the app"** on the welcome page to explore a demo account.

<!-- Add screenshots here: drag images into this editor -->

## Why Pomodorolist?

Most focus apps lock streaks, stats, sync and themes behind a subscription. Pomodorolist gives you all of it for free, with no ads and no tracking. If you just want a clean timer, **True Minimalist** mode hides all the game elements.

## Features

### Focus
- **Custom Pomodoro timers:** your own focus and break lengths, saved as presets
- **Named sessions and subtasks:** label what you're working on and tick off small goals
- **Distraction parking lot:** jot down a distracting thought in two seconds without stopping the timer
- **Ambient sounds:** rain, brown noise, café, ocean and more
- **Energy check-ins:** rate your focus after a session and discover when you focus best

### Plan
- **Reminders:** Pomeo reminds you 5–30 minutes before a session, with snooze and repeat
- **Add to calendar:** export reminders to your phone's calendar (.ics or Google Calendar)
- **Spaced revision:** revise topics at 1, 3, 7, 21 and 45 days
- **Exam countdown:** days left plus how many focus hours you're on track for

### Stats
- **Daily streaks** and a daily focus goal
- **Focus graphs:** today's timeline, weekly bars, monthly heatmap, yearly contribution grid
- **Insights** from your energy check-ins: best time of day, session length and days
- **Wrapped:** a monthly and yearly story-style recap with a shareable card

### Play
- **Tomato garden:** every session grows a plant; quitting early leaves a wilted one
- **Weekly boss battles:** 10 bosses rotate week by week. Fight **Solo** or with a **Squad** of up to 5 friends in an animated arena, with angry phases, a battle log and a Trophy Hall
- **Boss rewards (free):** Solo wins give the boss's theme and aura; Squad wins give its gradient name colour and a shimmering squad aura; beat both in one week to **Master** it
- **Monthly Pomeo questlines:** a new themed event each month (Halloween, Monsoon Study, Christmas, New Year and more) with 8 hard quests and limited-time rewards: Pomeo skins, themes, auras, name colours, profile pictures, sounds and more
- **XP, levels and 9 tiers:** Novice → Apprentice → Scholar → Focused → Disciplined → Expert → Master → Grandmaster → Legend
- **Coins and a cosmetic shop:** themes, sounds, timer styles, fonts, effects, profile pictures, Pomeo outfits and Streak Freezes (cosmetic only; nothing affects your stats)
- **Achievements, daily login rewards and auras** around your profile

### Bag 🎒
- Everything you own in one place, sorted into categories, with where each item came from
- Equip anything with a live preview, choose your streak aura or a special aura, and save full looks as **Loadouts**

### Pomeo 🍅
- A tomato mascot who reacts when you tap him, cheers you on, reminds you of sessions, dresses up for events, and gently suggests sleep late at night

### Friends
- **Add friends** by username or invite link, with requests, remove and block
- **Friend profiles:** streak, level, charts, heatmap and recent sessions, plus a side-by-side compare
- **Leaderboards:** Friends and Global (opt-in), for Daily, Weekly, Monthly and Lifetime
- **Focusing now, kudos, nudges, friend streaks, weekly challenges** and event boards

### Experience
- **Welcome page** with a demo account preview and theme switcher
- **Interactive tutorial** with Pomeo for new users
- **True Minimalist mode** and **Glossed Interface** (Off / Lite / Full)
- **Smooth animations and soft interface sounds,** each adjustable, plus a **Test sounds** button
- **Inbox** for requests, kudos, reminders and rewards
- **Command palette** (Cmd/Ctrl+K) and keyboard shortcuts
- **Fast:** opens instantly from a saved copy on your device and syncs in the background
- **Festive touches** during events (switchable off), light and dark mode, offline support and JSON export/import

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

- **With an account:** data is stored in **Google Firebase** (Authentication + Firestore). A copy is kept on your device so the app opens instantly and works offline; changes from your other devices merge in within seconds.
- **Without an account:** choose **"Continue without an account"**. Everything stays in your browser and nothing is uploaded. Friends, leaderboards and squad battles need an account.
- **The demo preview** never saves anything anywhere.

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
- **Event rewards are limited:** quests must be completed during the event
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
