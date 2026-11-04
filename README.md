# 🍅 Pomodorolist

**A free Pomodoro study timer that grows a garden while you focus.**
No ads. No tracking. Runs in your browser.

👉 **Try it:** https://siverieg.github.io/Pomodorolist-V1.0/
🎬 **Watch the trailer:** https://youtu.be/Ir033JoyJ5Q

Current version: **v1.19.1**

---

## What is it?

Pomodorolist is a focus timer built for students. You study in focused blocks, take short breaks, and everything you do feeds back into your progress: your garden grows, your streak climbs, your rank goes up, and Pomeo (the little tomato) evolves with you.

You can use it on your own, or study with friends, clans and strangers in live study sessions.

---

## Features

### ⏱️ Focus
- Custom Pomodoro timers with named sessions and subjects
- Recently used presets and favourites for one-tap starts
- Finish early (partial focus still counts after 5 minutes)
- Focus graphs by day, week, month and year
- Weekly subject plan with target hours per subject
- Break flashcards with spaced repetition
- To-do list and reminders
- True Minimalist mode for distraction-free studying

### 🌱 Garden
- 18+ plant species across 4 rarities, growing from seed to fruit as you focus
- Rotating seed shop, rare seed of the day and clan-exclusive seeds
- Garden pets that hatch from focus eggs and give boosts
- Crop weights, Giant harvests and personal records
- Focus-weather mutations (late-night Moonlit, long-session Shocked, and more)
- Harvest collection with star ratings, trophy shelf and compost
- Pomeo's room to decorate with items you earn

### 👥 Study together
- **Study sessions:** host or join live sessions, with or without a clan
  - *Focus together*: everyone runs their own timer at a shared table
  - *Synced timer*: one shared timer for the whole group
- Ask to join a friend's session, invite friends in the app, or share an invite link
- Friends tab with Friends, Study sessions and Challenges
- Kudos and nudges
- Weekly challenges with friends
- **Clans:** create a study group, level it up to 30, unlock clan cosmetics, beat monthly raid bosses and complete weekly clan quests

### 🏆 Progress and rewards
- XP and levels (Novice → Legend)
- **Ranks:** monthly seasons from Bronze to Grandmaster, based on how much you focus this month
- **Streak milestones** at 3, 7, 14, 30, 50, 100, 200 and 365 days
- Leaderboards for focus time, garden, ranks and streaks (Friends / Global / Clans)
- Achievements, weekly quest board and a free monthly reward track
- Weekly boss battles and seasonal questlines
- Pomeo evolves as your lifetime focus hours grow
- Collection log showing every cosmetic and how to get it
- Monthly recap of your study month
- Cosmetic shop: themes, sounds, timer styles, fonts, avatars, frames and auras

### 🔒 Privacy
- No ads and no tracking
- You sign up with just a username
- Works without an account too, with data saved in your browser
- Other people only see what you choose to share

---

## Built with

- **HTML, CSS and plain JavaScript** in a single `index.html`
- **Firebase Authentication** for accounts
- **Cloud Firestore** for syncing, friends, sessions and leaderboards
- **GitHub Pages** for hosting

There's no server or backend code. Firestore security rules (`firestore.rules`) protect everyone's data and block the obvious ways of cheating.

---

## Running your own copy

1. **Create a Firebase project** at https://console.firebase.google.com (the free Spark plan is enough).
2. **Turn on Authentication** with the Email/Password sign-in method. The app uses usernames, which it turns into emails behind the scenes.
3. **Create a Cloud Firestore database.**
4. **Publish the rules:** go to Firestore → Rules, then paste and publish the contents of `firestore.rules`.
5. **Create the indexes:** go to Firestore → Indexes, then create every composite index listed in `firestore.indexes.json`. All of them use Collection scope. Wait until they all say *Enabled*.
6. **Add your config:** in Project settings → Your apps, register a web app and copy its config. In `index.html`, search for `EDIT HERE` and paste your values in.
7. **Host it:** upload `index.html` to GitHub Pages (or any static host) and open it.

The setup order matters: rules first, then indexes, then the app files.

---

## Version history (short)

| Version | Highlights |
|---|---|
| v1.0 – v1.9 | Timer, streaks, graphs, accounts, XP, shop, friends, leaderboards, bosses, Pomeo |
| v1.10 – v1.13 | Sounds, faster loading, boss rework, inventory, new navigation, intro animation |
| v1.14 | Clans, to-do list, clan study sessions, raids and quests |
| v1.15 – v1.16 | Garden overhaul, pets, Pomeo's room, flashcards, subject plan, leaderboard v2 |
| v1.17 | Bug fixes, finish early, harvest collection, garden tour, daily rewards |
| v1.18 | Study sessions without clans, friends tab rework, streak milestones, new achievements, minimal Pomeo, quest board, monthly track, collection log |
| v1.19 | Ranks (monthly seasons) and streak leaderboards |

---

## Feedback

Found a bug or have an idea? I'd love to hear it.

- 📧 siverieg.p@gmail.com
- 💬 Join the Pomodorolist Discord server
- 🐛 Or open an issue on this repo

---

Made by **siverieg** 🍅
