# Gym Tracker

A workout tracking app hosted on GitHub Pages, with data stored as a JSON file in the same repo.

---

## How it works

- **Frontend**: `index.html` served via GitHub Pages (free, no server needed)
- **Data**: `gym-data.json` in your repo — read/written via the GitHub Contents API
- **Auth**: A Personal Access Token you enter once in the app (stored in your browser's localStorage, never committed)

---

## Setup (5 minutes)

### 1. Create a new GitHub repo

Go to https://github.com/new and create a **public** repo (e.g. `gym-tracker`).

> Private repos work too, but require a paid plan for GitHub Pages.

### 2. Add index.html

Upload `index.html` to the root of the repo (drag & drop on the repo page, or commit via git).

### 3. Enable GitHub Pages

In your repo: **Settings → Pages → Source → Deploy from branch → main / (root) → Save**

Your app will be live at: `https://YOUR_USERNAME.github.io/YOUR_REPO/`

### 4. Create a Personal Access Token

1. Go to https://github.com/settings/tokens/new (classic token)
2. Give it a name like `gym-tracker`
3. Set expiration (1 year recommended)
4. Check the **`repo`** scope (full repo access)
5. Click **Generate token** and copy it — you won't see it again

### 5. Connect the app

1. Open your GitHub Pages URL
2. Fill in the banner at the top:
   - **username**: your GitHub username
   - **repo-name**: your repo name
   - **ghp_...**: your Personal Access Token
3. Click **SAVE**

The dot in the header turns green. The app creates `gym-data.json` in your repo automatically on first save.

---

## Usage

- **Add exercises** to your library first (Exercises tab)
- **Build workouts** in the Workout tab, check off sets as you go
- **Save Workout** — writes to GitHub, visible in History tab
- **Templates** — save a workout structure to reload on future sessions
- **Analytics** — track max weight and volume over time per exercise

---

## Token security

Your token is stored **only in your browser's localStorage** — never committed to the repo.
To revoke: go to https://github.com/settings/tokens and delete the token.
