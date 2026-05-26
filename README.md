# 🐾 GoodSama

GoodSama dissolves the fear that stops people from helping animals in distress — instantly connecting them to a trusted, nearby network so they go from I can't do this to I'm not doing this alone.

---

## Who it's for

**Good Samaritans** — animal lovers who care but freeze: no contacts, no confidence, no network.
**NGOs** — welfare organisations that need a reliable, low-noise channel to mobilise trusted helpers fast.
**The animal** — the reason any of this exists.

> MVP: ~20 volunteers in Dehradun, linked to one NGO.

---

## Setup

Right now GoodSama is a static HTML prototype — no server required. Here's how to run it:

Step 1 — Get the files. Clone or download the project folder. It contains index.html, login.html, brand.md, and README.md.
Step 2 — Open locally. The simplest way is VS Code with the Live Server extension:
bashcode --install-extension ritwickdey.LiveServer
code /path/to/goodsama
Then click Go Live in the bottom-right of VS Code. The app runs at http://127.0.0.1:5500 and auto-reloads on every save. Alternatively, use Python's built-in server: python3 -m http.server 5500.
Step 3 — Fonts. The UI uses Google Fonts (DM Sans + DM Serif Display) loaded via CDN, so an internet connection is needed for them to render correctly. They degrade gracefully without one.

---

## Tech Stack

**Frontend:** Plain HTML, CSS, vanilla JS — no framework, no build step.

**Backend (planned):** Firebase end-to-end.

| Service | Role |
|---|---|
| Firebase Auth | Phone number OTP |
| Firestore | Users, reports, NGO links, notifications |
| Cloud Functions | Matching engine — filters by NGO + radius + active status |
| Cloud Storage | Report photos |
| FCM | Push notifications to volunteers |

---

## What's Next

**Screens:** `setup.html` (radius registration + NGO link request) → `home.html` (dashboard for Volunteer, NGO, Admin)

**Phase 2:** In-app rescue guidance · Anonymous calling · Post-resolution feedback · Case relay
