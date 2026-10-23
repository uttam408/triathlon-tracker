# Triathlon Tracker

Live multi-athlete triathlon timing page. Static site (GitHub Pages) + Firebase Firestore for shared live state. No sign-in: anyone with the link and the race code can record times.

Open it as `https://uttam408.github.io/triathlon-tracker/#<race-code>`. The code picks the race; share the full link with the group.

## One-time setup
1. Firebase console > create a project > Build > Firestore Database > create (production mode).
2. Firestore > Rules: paste `firestore.rules`, publish.
3. Project settings > Your apps > Web app: copy the config into `firebase-config.js`.
4. Push to `main`; Pages serves the repo root.

Data layout: `rooms/<code>/meta/race`, `athletes/<name>`, `races/<id>`, `events/<auto>`.
