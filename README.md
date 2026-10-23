# Pomodorolist 🍅

A free, minimal focus timer that turns studying into a game. Custom Pomodoro timers, streaks and stats, a tomato garden, weekly boss battles, monthly Pomeo questlines, friends, clans with live study sessions, and a friendly tomato mascot called Pomeo. Log in on any device and your progress follows you.

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
- **No interruptions:** pop-ups, rewards and notifications wait until your focus block ends
- **Ambient sounds:** rain, brown noise, café, ocean and more
- **Energy check-ins:** rate your focus after a session and discover when you focus best
- **Completion stamps:** a satisfying stamp when a session ends, with collectible styles

### Plan
- **To-do list:** tasks with due dates, priorities, tags, notes and checklists, plus "Focus on this" to start a session from a task
- **Reminders:** Pomeo reminds you 5–30 minutes before a session, with snooze and repeat
- **Add to calendar:** export reminders to your phone's calendar (.ics or Google Calendar)
- **Spaced revision:** revise topics at 1, 3, 7, 21 and 45 days
- **Exam countdown:** days left plus how many focus hours you're on track for

### Stats
- **Daily streaks** and a daily focus goal
- **Focus graphs:** today's timeline, weekly bars, monthly heatmap, yearly contribution grid
- **Insights** from your energy check-ins: best time of day, session length and days
- **Wrapped:** a monthly and yearly story-style recap with a shareable card
- **Profile card:** a game-style player card with a stats board, featured highlights and custom banners, shareable as an image or a link

### Play
- **Tomato garden:** every session grows a plant; quitting early leaves a wilted one
- **Weekly boss battles:** 10 bosses from ★ Easy (300 HP) to ★★★★★ Legendary (600 HP), rotating weekly. Fight **Solo** or with a **Squad** of friends in an animated arena
- **Boss rewards (free):** themes, auras, name colours and boss profile pictures, getting rarer and fancier as bosses get harder. Squad rewards are one step fancier, and beating both in one week **Masters** the boss
- **Monthly Pomeo questlines:** a new themed event each month with 8 hard quests and limited-time rewards
- **XP, levels and 9 tiers:** Novice → Apprentice → Scholar → Focused → Disciplined → Expert → Master → Grandmaster → Legend
- **Coins and a cosmetic shop:** themes, sounds, timer styles, fonts, effects, stamps, profile pictures, Pomeo outfits and Streak Freezes (cosmetic only; nothing affects your stats)
- **Achievements, daily login rewards and auras** around your profile

### Clans 🛡️ (study groups)
- **Create a clan for free** and invite people with a link or code; leaders choose approval (default) or open joining
- **Roles:** Leader, Officers and Members
- **Clan levels 1–30** from focus done *while in the clan*, plus Clan Points for a clan shop (emblems, banners, themes, frames)
- **Clan cosmetics:** clan tag, name colours, auras and frames that get rarer as your clan levels up
- **Planned study sessions:** schedule sessions, RSVP, get reminders and add them to your calendar
- **Live study sessions:** one shared timer for everyone, a study table with Pomeo, and preset reactions
- **Weekly clan quests, a monthly raid boss, an activity feed, an MVP board, a trophy case and a clan study streak**
- **Public Clans leaderboard** (weekly and all-time)

### Bag 🎒
- Everything you own in one place, sorted into categories, with where each item came from
- Equip anything with a live preview, choose your streak aura or a special aura, and save full looks as **Loadouts**

### Pomeo 🍅
- A tomato mascot who reacts when you tap him, cheers you on, reminds you of sessions, dresses up for events, and gently suggests sleep late at night

### Friends
- **Add friends** by username or invite link, with requests, remove and block
- **Friend profiles:** streak, level, charts, heatmap, recent sessions and their profile card
- **Leaderboards:** Friends, Global (opt-in) and Clans
- **Focusing now, kudos, nudges, friend streaks, weekly challenges** and event boards

### Experience
- **A short intro and welcome page** with a demo account preview and theme switcher
- **Interactive tutorial** with Pomeo for new users
- **True Minimalist mode** and **Glossed Interface** (Off / Lite / Full)
- **Time-of-day backgrounds:** sunrise, day, sunset and night skies
- **Smooth animations and soft interface sounds,** each adjustable, plus a **Test sounds** button
- **Inbox** for requests, kudos, reminders, clan news and rewards
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
| 1–9 | Switch tabs |
| Cmd/Ctrl + K | Command palette |
| ? | Show all shortcuts |

## How it works (local vs. cloud)

The app runs in your browser as a single HTML file, with no custom server.

- **With an account:** data is stored in **Google Firebase** (Authentication + Firestore). A copy is kept on your device so the app opens instantly and works offline; changes from your other devices merge in within seconds.
- **Without an account:** choose **"Continue without an account"**. Everything stays in your browser and nothing is uploaded. Friends, leaderboards, squads and clans need an account.
- **Live study sessions** use one shared start time, so everyone's timer stays in sync without constant updates.
- **The demo preview** never saves anything anywhere.

The Firebase config in the code is meant to be public. Access is controlled by Firestore security rules: your private data is readable only by you, friend activity only by accepted friends, and clan member data only by members of that clan.

## Privacy and safety

- No ads, no analytics, no tracking
- Passwords are handled by Firebase Authentication and never stored by the app
- Usernames and drawn avatars only: no real names, emails or photo uploads shown to others
- **You control what friends and clanmates see:** session names, activity and "focusing now" status can each be hidden
- **No chat, DMs or free-text messages** anywhere, only preset reactions, nudges and descriptions
- **Clan names, tags and session titles** pass a word filter
- **Clans require approval to join by default,** and leaders can reset invite links at any time
- **The public Clans leaderboard** shows only clan-level info, never member names or stats
- **The Global leaderboard is opt-in** and off by default
- Block anyone at any time, leave any clan at any time, and erase all your data from Settings

## Known limitations

- **No password reset:** accounts use a username, not an email, so pick a password you'll remember
- **Usernames can't be changed,** because the username is your login
- **Reminders only fire while the app is open** (a background tab is fine). Use **Add to calendar** for reminders when the app is closed.
- **Running personal timers stay on one device;** completed sessions sync everywhere
- **Event rewards are limited:** quests must be completed during the event
- **Leaderboards can't be fully cheat-proof** without a server; security rules block obvious cheating, but not every case
- **Very large live sessions** use more of the free Firebase quota, so they're best kept to small groups
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
