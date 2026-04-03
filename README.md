# 💬 NiviChat

A private two-user messaging app with voice calling, built for GitHub Pages. Features an Apple Liquid Glass UI in black theme.

## 🚀 Deploy to GitHub Pages

1. Create a new **private** GitHub repository (e.g. `nivichat`)
2. Upload `index.html` and `nivichat-db.json` to the root
3. Go to **Settings → Pages → Source: main branch / root**
4. Your app is live at `https://yourusername.github.io/nivichat/`

## 🔐 Admin Login

Default credentials (change in `index.html`):
- **Username:** `admin`
- **Password:** `Admin@2024`

> ⚠️ To change the admin password, open `index.html` and edit line:
> ```js
> const ADMIN_PASSWORD = 'Admin@2024';
> ```

## 👤 Creating Users

1. Log in as admin
2. Go to **Add User** → fill in Display Name, Username, Password
3. Click **Create User**
4. Export the DB → commit `nivichat-db.json` to GitHub

## 🗄️ Database

The database lives in **browser localStorage** and is also exportable as `nivichat-db.json`.

### Keeping it synced on GitHub:
- After adding users or wanting to back up messages, click **Export DB** in the Admin panel
- Commit the downloaded `nivichat-db.json` to your repo
- On a new device, import it via **Import DB**

## 📞 Voice Calling

- Select a contact → click the 📞 green button in the header
- Uses WebRTC (peer-to-peer) — works best on the same network or with STUN
- Requires microphone permission

## ✨ Features

- 🔐 Admin panel — create/delete users, reset passwords
- 💬 Real-time-like messaging (localStorage polling every 1s)
- 📞 WebRTC voice calling with mute support
- 🖼 Profile photos (upload or auto-generated initials)
- 🎨 Apple Liquid Glass UI — deep black theme
- 💾 DB export/import for GitHub backup
- 🔍 Contact search
- 📅 Message timestamps & date dividers

## 🛠 Tech Stack

- Pure HTML/CSS/JS — zero dependencies
- WebRTC for voice calls
- localStorage as the database
- GitHub Pages for hosting
