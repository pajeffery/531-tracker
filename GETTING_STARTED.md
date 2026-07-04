# Getting Started with Forge

A step-by-step guide to set up and start using Forge for Madcow 5×5 tracking.

## 1. Access Forge

Visit the production app:
```
https://happy-pond-003313103.7.azurestaticapps.net
```

The app loads instantly - no login required (unless syncing to Google Sheets).

## 2. Install as PWA (Recommended)

Makes Forge work offline and easier to access.

### iOS (Safari)
1. Open Forge in Safari
2. Tap the **Share** button (arrow icon)
3. Scroll down and tap **Add to Home Screen**
4. Name it "Forge" and tap **Add**
5. Forge now appears on your home screen like a native app

### Android (Chrome)
1. Open Forge in Chrome
2. Tap the **Menu** button (three dots)
3. Tap **Install app** (or **Add to Home Screen**)
4. Confirm and tap **Install**
5. Forge now appears in your app drawer

## 3. Initial Configuration

When you first open Forge, go to **Settings** to configure:

### Step 1: Working Weights
Enter your current 1-rep-max equivalent working weights for each lift:
- **Squat**: Your heaviest comfortable 5-rep weight
- **Bench**: Your heaviest comfortable 5-rep weight
- **Row**: Your heaviest comfortable 5-rep weight
- **OHP**: Your heaviest comfortable 5-rep weight
- **Deadlift**: Your heaviest comfortable 5-rep weight

*Unsure? Start conservative. You can increase them after your first session.*

### Step 2: Bar Weight
Set your barbell weight (default: 20kg)
- Standard barbell: 20kg
- Some gyms: 15kg or 16kg

### Step 3: Weight Rounding
Choose how to round calculated weights (default: 2.5kg)
- **2.5kg**: Standard (recommend for most)
- **1.25kg**: More precise, requires smaller plates
- **5kg**: Larger jumps, fewer plates to load

### Step 4: Rest Timer
Set rest period between sets (default: 180 seconds = 3 minutes)
- Adjust based on your intensity/recovery needs
- Can override per-session in the Timer section

### Step 5: Google Sheets (Optional)
To sync your workouts automatically:
1. Tap **Connect to Google Sheets**
2. Select your Google account
3. Authorize Forge to access Sheets
4. App creates/uses sheet named "Forge"

## 4. Understand the Workout Structure

Forge uses a 3-session cycle inspired by Madcow 5×5. Unlike the original program which requires strict Mon/Wed/Fri scheduling, **you can train these sessions whenever your schedule allows**. Forge tracks your cycle progression, not the calendar.

### The Three Session Types
- Squat, Bench, Row
- Moderate intensity - focus on form and consistency

### Session B
- Light Squat (80%), OHP, Deadlift
- OHP and Deadlift are once per week

### Session C
- Heavy Squat, Heavy Bench, Heavy Row
- Highest intensity - final set is AMRAP (as many reps as possible)

**Typical training pattern**: Session A → Session B → Session C → Session A (repeat)

**Flexible schedule example**: 
- Monday: Session A
- Wednesday: Session C (flexible order!)
- Friday: Session B
- Next Monday: Session A
- (Or skip a day, train twice in one day, whatever works)

The key is completing all three sessions in order before the cycle repeats.

## 5. Log Your First Workout

### Before You Start
- Warm up properly (not tracked in app)
- Have your working weight in mind
- Keep water nearby

### During the Workout
1. Open Forge → **Workout** tab
2. Tap the exercise you're about to do
3. You'll see all sets (warm-ups + working sets) with weight and reps
4. Complete each set as listed
5. After finishing a set, tap it in the app:
   - **✓ (Done)** - completed all reps
   - **✗ (Failed)** - didn't complete all reps
   - Leave blank if you haven't done it yet
   - Tap again to cycle through states

### Important Notes
- **Warm-up Sets**: Auto-calculated at 40%, 50%, 60%, 80% of your work weight
- **Working Sets**: The heavy sets at your full working weight
- **Progressive Unlock**: Sets 2-5 are greyed out until Set 1 is marked (guides your workout flow)
- **Plate Calculator**: Tap the plates display to instantly copy what to load

### After the Last Set
1. All sets marked → **Log Session** button appears
2. Tap **Log Session** → Review summary
3. Confirm → Session logged! ✓
4. Celebration message shows your progress
5. App auto-advances to next session (B, C, or A)

## 6. After Your First Session

### Check Your Progress
- **Progress** tab → See your working weight
- **History** tab → Calendar view of all sessions
- Settings shows your stats (sessions logged, current cycle)

### Weight Progression
- After each **C session**: All working weights automatically increase by 2.5kg
- The app handles this - just confirm when prompted
- If you fail reps: Deload recommendation will appear

## 7. Understanding Deload Recommendations

Forge will suggest a deload in two scenarios:

### Scenario 1: You Failed a Lift Twice
- If you miss reps on same lift 2 sessions in a row
- **Accept**: That lift reduces 10% for one session, then normal progression resumes
- **Skip**: You can skip, but Forge will ask again if it happens again

### Scenario 2: After 9 Weeks
- After 3 complete A-B-C cycles (every 9 weeks)
- **Accept**: All lifts reduce 10%, reset, then normal progression resumes
- **Skip**: Continue at current weight

*Deloads are normal and healthy - they prevent overtraining and CNS fatigue.*

## 8. Tips for Success

### Tracking Missed Reps
- Mark sets honestly - don't fudge the data
- "Failed" = didn't complete all reps (not a sign of weakness, just data)
- The app uses this to recommend deloads at the right time

### Adjusting Weight
- If struggling early in the cycle → Settings → manually reduce weights
- If feeling strong after a few sessions → increase them
- The +2.5kg jumps are targets, not dogma

### Rest Timer
- Use it between sets
- Can override in-session if needed
- Default 3 min is solid for strength training

### Google Sheets
- Highly recommended - gives you a permanent backup
- Data syncs automatically when you log sessions
- You can share the sheet with a coach for feedback

### Consistency
- Train 3x per week (Mon/Wed/Fri, Tue/Thu/Sat, etc.)
- Rest days between sessions are important
- Track every session - the data is valuable

## 9. Common Questions

**Q: What if I miss a workout?**
A: Just pick up where you left off. Forge will be ready for your next session.

**Q: Can I edit a logged session?**
A: Yes! Tap "Undo Log" on the workout page, edit the sets, and re-log.

**Q: What if my schedule doesn't match A-B-C pattern?**
A: Just log what you did. Forge tracks the session type, not the calendar.

**Q: Why isn't my weight increasing?**
A: You might be in a deload week, or not all sessions are being logged. Check your session history.

**Q: How do I backup my data?**
A: Connect to Google Sheets (syncs automatically) or export from browser settings.

**Q: Does it work offline?**
A: Yes! Forge works completely offline. Just reconnect to sync to Google Sheets.

## 10. Next Steps

- **First Week**: Just focus on learning the UI and logging accurately
- **After 2 Weeks**: You'll see weight progression trends
- **After 9 Weeks**: First deload recommendation - embrace it!
- **After 3 Months**: You'll have substantial data showing your progress

---

Good luck with your training! 💪

Questions or issues? Check the main [README](README.md) for support options.
