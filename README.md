# Momentum

Momentum is a private-first Android habit, task and notes app I built for my own routine. I wanted one place that could remind me about fixed-time habits, keep flexible work visible until it was done, and show whether I was actually staying consistent.

I built it with Claude after mapping the routines I wanted to follow, the reminder behaviour and how each task should appear on my OnePlus 13. I tested the APK and added selected-day routines, stronger reminders and the home-screen widget after using the first version.

## What it does

- Today view for habits and one-off tasks
- Per-task days of the week, including Sunday-only routines
- Fixed-time and nag-until-done reminders
- Morning brief, streak-at-risk nudge and Sunday report
- Home-screen widget with tap-to-complete actions
- Streaks, one weekly streak freeze and a heatmap-style stats view
- Notes plus local backup export and import
- Fully offline storage with no internet permission

## Tech stack

- Kotlin and Java 17
- Jetpack Compose with Material 3
- Android SDK 35, minimum SDK 26
- Kotlin Serialization with a local JSON data store
- Android notifications, alarms, broadcast receivers and App Widgets

## Download the app

[Download Momentum v2.0](Momentum-v2.0.apk). Android may ask you to allow installation from your browser or file manager because this is a personal APK rather than a Play Store release.

## Prompt given to Claude

[Read the complete prompt](PROMPT.md)

## Privacy

Momentum keeps its data on-device. No account, analytics service or remote database is used.
