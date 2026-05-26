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

Static HTML prototype — no server, no build step.
 
**1. Get the files** — clone or download the project folder. Contains `index.html`, `login.html`, `brand.md`, and `README.md`.
 
**2. Run locally** — VS Code + Live Server is the simplest option:
 
```bash
code --install-extension ritwickdey.LiveServer
code /path/to/goodsama
```
 
Click **Go Live** in the bottom-right status bar. Runs at `http://127.0.0.1:5500` and auto-reloads on save. Or use Python: `python3 -m http.server 5500`.
 
**3. Fonts** — DM Sans + DM Serif Display load via Google Fonts CDN. An internet connection is needed for them to render; they degrade gracefully without one.
 
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
