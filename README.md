# API-to-Cloud Trivia Showdown

CSC 4360 Activity #15

This Flutter app fetches five easy multiple-choice questions from Open Trivia DB. It shows loading and error states, shuffles the choices, gives immediate answer feedback, and displays the final score. The score-sync button simulates a submission. It sends no backend request.

## How to run

```bash
flutter pub get
flutter run
```

## Critical Thinking

**What should happen if the internet drops after the questions load?**

I would let the player finish the round because all five questions are already in memory. Answer feedback and scoring happen inside the app. If the player taps Replay while offline, the app should show a loading state while it tries to fetch a new round, then show an error if the request fails so the player knows to try again once connected.

**What would you save locally?**

I would save the player's best score so they can see the score they want to beat the next time they open the app. This would be a personal record stored on that device. A shared leaderboard would need a backend that collects scores from different players.