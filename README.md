# Momentum

Momentum is a private-first Android habit, task and notes app I built for my own routine. I wanted one place that could remind me about fixed-time habits, keep flexible work visible until it was done, and show whether I was actually staying consistent.

I vibecoded the app with Claude: I described the problem and my OnePlus 13 setup, reviewed the proposed product plan, chose the reminder behaviour and then iterated on the working APK. The finished app is native Android code rather than a generated mockup.

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
- Gradle 8.10.2 / Android Gradle Plugin 8.7.3

## Download the app

[Download Momentum v2.0](Momentum-v2.0.apk). Android may ask you to allow installation from your browser or file manager because this is a personal APK rather than a Play Store release.

This repository is a project showcase and download page. The source code and private signing key remain private.

## AI build prompt

The first brief was conversational: a personal Android to-do and notes app that would keep me accountable for medication, study and everyday tasks. I later added day-specific routines, widgets and stronger reminder logic.

[Read the reconstructed production prompt](PROMPT.md). It captures the complete requirements in a cleaner format and is not presented as a verbatim transcript.

## Privacy

Momentum keeps its data on-device. No account, analytics service or remote database is used.
