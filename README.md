# Algebra Blitz: Two-Step Equation Speed Battle ⚡

A real-time multiplayer educational web game where students solve as many two-step linear equations ($ax + b = c$) as possible within a host-controlled timer.

## Features
- **100 Synchronized Equations:** Identical sequence of equations for all players using seeded PRNG.
- **24 Unique Avatars & 8 Color Themes:** Strict uniqueness enforcement prevents duplicate avatars in the same room.
- **Interactive Scratchpad:** Built-in drawing canvas with Pen, Eraser, Undo, and Clear tools that auto-clears on each problem.
- **Live Host Controls:** Set custom duration, launch countdown, monitor real-time leaderboard, and end match at any moment.
- **Celebration Podium:** 3-tier Olympic podium with animated dancing avatars for 1st, 2nd, and 3rd place, with top 10 listed below.
- **Worked Solutions Review:** Step-by-step 4-column aligned chalkboard solutions (no separating bars) with Previous/Next navigation and "Browse All 100" mode.

---

## Part 1: Setting Up Free Firebase Realtime Database (3 Minutes)

1. Go to [Firebase Console](https://console.firebase.google.com/) and click **Add project** (name it e.g., `algebra-blitz`).
2. In the left sidebar, click **Build &rarr; Realtime Database**, then click **Create Database**.
3. Choose any location (e.g., `United States`), and when prompted for Security Rules, select **Start in test mode** (this allows read/write access so students can join without logging in), then click **Enable**.
4. In Project Overview, click the Web icon (<code>&lt;/&gt;</code>) to register an app (name it `Algebra Blitz Web`).
5. Copy the `firebaseConfig` code block that appears:
   ```javascript
   const firebaseConfig = {
     apiKey: "AIzaSy...",
     authDomain: "algebra-blitz-12345.firebaseapp.com",
     databaseURL: "https://algebra-blitz-12345-default-rtdb.firebaseio.com",
     projectId: "algebra-blitz-12345",
     storageBucket: "algebra-blitz-12345.appspot.com",
     messagingSenderId: "...",
     appId: "..."
   };
   ```
6. Open `index.html` or `host.html` in your browser, click **🔥 Firebase Setup** in the top bar, and paste this snippet. It will automatically connect and save!

---

## Part 2: Hosting on GitHub Pages for Free (2 Minutes)

1. Go to [GitHub](https://github.com) and create a new public repository (e.g. `algebra-blitz`).
2. Upload `index.html` and `host.html` to the repository.
3. Click **Settings** &rarr; **Pages** in the left sidebar.
4. Under **Build and deployment &rarr; Branch**, select `main` (or `master`) and folder `/ (root)`, then click **Save**.
5. After 30 seconds, your site is live!
   - **Student / Player Link:** `https://<your-username>.github.io/algebra-blitz/`
   - **Teacher / Host Link:** `https://<your-username>.github.io/algebra-blitz/host.html`

Both links connect to the same Room Code (`BLITZ1` by default, or any custom room code you choose)!
