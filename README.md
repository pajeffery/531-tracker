# Forge - Madcow 5×5 Weightlifting Tracker

A progressive web app (PWA) for tracking Madcow 5×5 strength training workouts with intelligent deload recommendations and detailed progress analytics.

## 🎯 Overview

Forge is a minimalist, offline-capable workout tracker inspired by the **Madcow 5×5** strength training protocol, but designed with flexibility for busy schedules. 

Unlike traditional Madcow which requires strict weekly scheduling (Mon/Wed/Fri), Forge lets you train whenever your schedule allows while maintaining the periodized progression structure. It automatically calculates warm-up sets, tracks session progress, detects failed reps, and recommends deloads based on training science.

Built with vanilla JavaScript and hosted on Azure Static Web Apps, Forge works on any device with a web browser - no installation required.

**Production**: https://happy-pond-003313103.7.azurestaticapps.net  
**Development**: https://agreeable-pond-07ec37b03.7.azurestaticapps.net

---

## 📖 Origin Story

Madcow 5×5 is an excellent periodized strength program, but its rigid weekly schedule (Session A on Monday, B on Wednesday, C on Friday) didn't fit a busy lifestyle with irregular training availability.

Forge was built to solve this: take the proven training principles of Madcow (3-week periodization cycles, intelligent progression, strategic deloads) but remove the calendar constraint. Train whenever you can - Forge tracks your cycle progress, not the day of the week.

The result is a flexible, schedule-agnostic training tracker that maintains training integrity while adapting to real life.

---

## ✨ Key Features

### Training Intelligence
- **Automated Warm-up Calculation** - Generates sets at 40%, 50%, 60%, 80% based on your working weight
- **Madcow 5×5 Protocol** - Three-week cycles (Session A/B/C) with automatic progression
- **Intelligent Deload System** - Recommends deloads after 2 consecutive session failures OR every 9 weeks (3 cycles)
- **Progressive Set Unlock** - Sets 2-5 are greyed out until previous sets are marked
- **Auto-Progression** - +2.5kg added to all lifts after each C session cycle

### Workout Experience
- **Session Tracking** - Mark sets as done (✓), failed (✗), or reset
- **Rest Timer** - Customizable rest periods between sets (default: 3 minutes)
- **Plate Calculator** - Instantly see plate combinations needed for your target weight
- **Progress Indicators** - Visual progress bar showing completion percentage
- **Compact Layout** - Exercise detail fits on one screen without scrolling

### Data & Analytics
- **Progress Charts** - Track max working weight over time for each lift
- **Session History** - Calendar view of all completed workouts
- **Volume Tracking** - Total volume per session
- **Missed Reps Counter** - Auto-detect when sets aren't fully completed
- **Stall Detection** - Track consecutive failures for each lift

### Technical Features
- **Progressive Web App (PWA)** - Works offline, installable on home screen
- **Google Sheets Integration** - Sync all session data to your own Google Sheet
- **Local Storage** - All data stored locally, synced to Sheets on demand
- **Responsive Design** - Works on phones, tablets, and desktops
- **Dark/Light Mode** - System preference detection with manual toggle

---

## 🏋️ Madcow-Inspired Training Protocol

Forge implements a periodized strength training system inspired by Madcow 5×5, but with flexible scheduling. Train whenever your schedule allows - the app tracks your cycle progress, not calendar days.

### Session Structure

The program cycles through three session types (A, B, C) repeated over three weeks. You can train these in any order based on your availability.

### Session Structure

**Session A** (3x per week)
- Squat: Warm-ups → 4×5 + 1×5+ (AMRAP)
- Bench: Warm-ups → 4×5 + 1×5+ (AMRAP)
- Row: Warm-ups → 4×5 + 1×5+ (AMRAP)

**Session B** (Light squat focus)
- Squat Light (80%): Warm-ups → 1×5
- OHP: Warm-ups → 4×5 + 1×5+ (AMRAP)
- Deadlift: Warm-ups → 1×5

**Session C** (Heavy - highest intensity)
- Squat Heavy: Warm-ups → 4×5 + 1×5+ + 1×3 + 1×8
- Bench Heavy: Warm-ups → 4×5 + 1×5+ + 1×3 + 1×8
- Row Heavy: Warm-ups → 4×5 + 1×5+ + 1×3 + 1×8

### Progression
- After each **C session**: All working weights +2.5kg
- **Deload (every 9 weeks)**: All weights -10% for one full session, then resume normal progression
- **If failing on C session**: Auto-deload that specific lift by 10%, reset missed reps counter

---

## 🚀 Getting Started

### Installation
No installation needed! Visit the production URL in your browser:
```
https://happy-pond-003313103.7.azurestaticapps.net
```

### Add to Home Screen (Recommended)
1. Open Forge in your browser
2. **iOS**: Tap Share → Add to Home Screen
3. **Android**: Tap Menu → Install app (or Add to Home Screen)

### Initial Setup
1. Enter your current working weights for each lift
2. Choose your bar weight (default: 20kg)
3. Set your preferred rounding (default: 2.5kg)
4. Customize rest period (default: 180s = 3 min)

### First Workout
1. Go to "Workout" tab
2. Tap an exercise to open detail view
3. Complete warm-up sets, then working sets
4. Mark each set: ✓ (done), ✗ (failed), or leave blank
5. Sets 2-5 unlock only after previous set is marked
6. When all sets marked, "Log Session" button appears
7. Review summary and confirm

---

## 📊 Features in Detail

### Deload System

Forge recommends deloads based on two triggers:

**1. Failure-Based Deload**
- Triggered when a single lift fails 2 consecutive sessions
- Reduces that lift by 10% for the next session
- Resets missed reps counter when accepted
- User can accept or decline (skips for 2 weeks if declined)

**2. Scheduled Deload**
- Triggered every 9 weeks (after 3 complete A-B-C cycles)
- Reduces all lifts by 10% for one full session
- User can accept or decline

### Progress Tracking

The Progress tab shows:
- **Weight Progression** - Line chart of max working weight over time
- **Per-Lift Analytics** - Separate charts for each major lift
- **Missed Reps** - Counter showing consecutive failures
- **Session Count** - Total workouts logged
- **Current Cycle** - Which week of the 3-week cycle you're in

### Google Sheets Integration

Sync your workouts to a personal Google Sheet:
1. Settings → Connect to Google Sheets
2. Authenticate with your Google account
3. App creates/uses existing sheet named "Forge"
4. Every logged session automatically syncs
5. Separate sheets for dev/production versions
6. Full session data: date, session type, lifts, weights, reps, volume

---

## ⚙️ Settings

**Workout Settings**
- **Bar Weight** - Loaded bar weight (default: 20kg)
- **Rounding** - Weight increment for plates (default: 2.5kg)
- **Rest Timer** - Rest between sets in seconds (default: 180s)

**Data**
- **Reset All Data** - Clears local storage (use with caution!)
- **Google Sheets** - Connect/disconnect account

---

## 🐛 How Missed Reps Detection Works

The app automatically tracks when you don't complete all reps:

- If any working set isn't marked as done OR failed → counts as missed
- Two consecutive missed sessions on same lift → triggers deload recommendation
- Successfully completing all reps → resets missed counter to 0
- Tracked per-lift, not per-session

---

## 📱 Technical Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Storage**: LocalStorage (browser) + Google Sheets (cloud sync)
- **Hosting**: Azure Static Web Apps
- **Authentication**: Google OAuth 2.0
- **APIs**: Google Sheets API v4, Google Drive API

### Browser Requirements
- Modern browser with ES6 support
- LocalStorage enabled
- For sync: Google account (optional)

### Offline Capability
Forge works completely offline:
- All data stored locally in browser
- Workouts can be logged without internet
- Google Sheets sync happens when online
- No data loss if offline

---

## 🔄 Development

### Clone & Setup
```bash
git clone https://github.com/pajeffery/531-tracker.git
cd 531-tracker
```

### Branches
- **main** - Production (deployed to happy-pond-*.azurestaticapps.net)
- **dev** - Development (deployed to agreeable-pond-*.azurestaticapps.net)

### Local Development
1. Open `index.html` in a modern browser
2. All features work locally with LocalStorage
3. Google Sheets sync requires OAuth setup (see below)

### Google OAuth Setup (for Sheets sync)
1. Create Google Cloud project
2. Enable Google Sheets API & Google Drive API
3. Create OAuth 2.0 Client ID (Web application)
4. Add authorized JavaScript origins:
   - `https://happy-pond-003313103.7.azurestaticapps.net`
   - `https://agreeable-pond-07ec37b03.7.azurestaticapps.net`
   - `http://localhost:8000` (for local testing)
5. Update `GOOGLE_CLIENT_ID` in index.html

### Deployment
- Push to `main` → Automatically deploys to production
- Push to `dev` → Automatically deploys to dev environment
- Uses Azure Static Web Apps CI/CD

---

## 📈 Future Ideas

Possible future enhancements (not implemented):
- Full-screen workout mode
- Multiple training programs (Stronglifts 5x5, 5/3/1, etc.)
- Voice commands for marking reps
- Social features (share progress)
- Advanced analytics and body weight tracking
- Mobile app versions
- Strength standards/leaderboards

---

## 📝 License

MIT License - See LICENSE file for details

---

## 🤝 Contributing

Found a bug or have a feature request? 
- Check existing [Issues](https://github.com/pajeffery/531-tracker/issues)
- Create a new issue with details
- Pull requests welcome!

---

## 📞 Support

- **Issues**: GitHub Issues tab
- **Questions**: Open a Discussion (coming soon)

---

## 🙏 Acknowledgments

Built with the Madcow 5×5 protocol and designed for strength athletes focused on functional fitness and lean gains.

Powered by vanilla JavaScript, Azure Static Web Apps, and Google Sheets.
