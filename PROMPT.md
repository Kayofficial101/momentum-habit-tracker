# Reconstructed production prompt

This is an improved, reusable version of the prompt behind Momentum. It preserves the real product intent while making the requirements and acceptance criteria explicit.

```text
Act as a senior Android product engineer, UX designer and QA lead. Build a polished personal accountability app named Momentum for a OnePlus 13. Use native Kotlin and Jetpack Compose. This is a real installable app for one person, not a concept screen.

PRODUCT GOAL
Help me complete daily habits and one-off tasks instead of forgetting or postponing them. The app should feel calm and motivating, but accountability matters more than decoration.

CORE USERS AND EXAMPLES
The primary user is me. Example routines include a multivitamin at 12:30 PM, flexible daily GMAT study, course videos that must be completed during the day, and one-off tasks such as visiting a bank tomorrow. Some routines happen only on selected weekdays, including Sunday-only tasks.

REQUIRED EXPERIENCE
1. Provide a Today view showing only what is actionable now.
2. Support recurring habits, one-off tasks and notes.
3. Let each recurring item use selected weekdays rather than assuming every day.
4. Support a fixed reminder time or a flexible nag-until-done mode.
5. Add a morning brief, a streak-at-risk reminder and a Sunday weekly report.
6. Track completion streaks, allow one streak freeze per week and show a useful heatmap/statistics view.
7. Add a home-screen widget that lists today's items and lets the user complete each one directly.
8. Include backup export and import so the user owns the data.

DESIGN DIRECTION
Use a dark charcoal interface with warm amber accents, strong readability, generous spacing and clear completion feedback. Keep the number of screens and taps low. Avoid generic dashboard clutter, gamification noise, guilt-heavy language and decorative elements that compete with the task list. Design for a modern OnePlus-sized phone and accessibility-friendly touch targets.

TECHNICAL CONSTRAINTS
- Kotlin, Jetpack Compose and Material 3.
- Minimum Android 8 (API 26); target the current installed SDK.
- Fully offline. Do not request INTERNET permission.
- Store data safely in a local JSON model using Kotlin Serialization and atomic writes.
- Use Android notification channels, exact/inexact alarm behaviour appropriate to the OS version, boot rescheduling and runtime notification permission handling.
- Build the widget with static RemoteViews rows and a unique PendingIntent per item so tap-to-complete works reliably across launchers.
- Keep signing credentials outside source control.

WORKING METHOD
Before coding, inspect the environment and present a short architecture and risk plan. Ask only questions that materially change the product. Then implement in small, testable slices. Do not silently drop requirements. Prefer the simplest reliable native solution over extra libraries or speculative abstraction.

DELIVERY AND ACCEPTANCE TESTS
- Produce a buildable Android project and an APK installation path.
- Confirm that fixed reminders, flexible reminders, selected weekdays and boot rescheduling work.
- Confirm widget rows render and each row completes the correct item.
- Confirm data survives app restarts and backup export/import round-trips correctly.
- Confirm no internet permission or secret is present.
- Run a clean Gradle build and smoke-test the major flows on an API 35 emulator.
- Finish with exact build, install and future-update instructions.
```
