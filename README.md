# Vault. — Personal Project Archive PWA

A mobile-first Progressive Web App for storing, showcasing, and documenting your projects.

---

## 🚀 Quick Setup

### 1. Firebase Setup
1. Go to [console.firebase.google.com](https://console.firebase.google.com)
2. Create a new project (e.g. `obinna-vault`)
3. Add a **Web App** to the project
4. Copy your Firebase config object

### 2. Plug in your config
Open `index.html` and find this block near line 350:

```js
const FIREBASE_CONFIG = {
  apiKey:            "YOUR_API_KEY",
  authDomain:        "YOUR_PROJECT.firebaseapp.com",
  projectId:         "YOUR_PROJECT_ID",
  storageBucket:     "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId:             "YOUR_APP_ID"
};
const ADMIN_PASSWORD = "vault2026"; // 👈 change this!
```

Replace every value with your actual Firebase config.
Change `ADMIN_PASSWORD` to something personal and secure.

### 3. Enable Firestore + Storage
In Firebase Console:
- **Firestore Database** → Create database → Start in **test mode** (you can secure it later)
- **Storage** → Get started → Start in test mode

### 4. Deploy to GitHub Pages
```bash
git init
git add .
git commit -m "init vault"
git remote add origin https://github.com/YOUR_USERNAME/vault.git
git push -u origin main
```
Then go to repo **Settings → Pages → Source → main branch / root**.

Your app will be live at `https://YOUR_USERNAME.github.io/vault/`

---

## 📱 Install as App

### Android (Chrome)
- Open the site in Chrome
- Tap the 3-dot menu → "Add to Home screen"

### iOS (Safari)
- Open the site in Safari
- Tap the Share icon → "Add to Home Screen"

---

## 🔐 Admin Mode

- Tap the ⚙ icon in the top-right
- Enter your password
- This unlocks: adding/editing/deleting projects, and viewing private projects
- Admin state persists in localStorage (tap ⚙ again to log out)

---

## 🔗 Public Share Links

Every project gets a shareable URL:
```
https://yoursite.com/vault/?id=PROJECT_ID
```
Tap the ↗ button on any project to copy or share the link.

---

## 📦 Features
- ✅ Add, edit, delete projects
- ✅ Cover image + screenshots gallery
- ✅ Tags, tech stack, status
- ✅ Case study write-up
- ✅ Ideas tab: Inspiration, Lessons, Next Steps, Resources
- ✅ Search + filter by tag
- ✅ Public / private visibility
- ✅ Public share links
- ✅ Offline support (Firestore persistence + Service Worker)
- ✅ Installable PWA (Android + iOS)
- ✅ Password-protected admin mode

---

## 📁 Files
```
vault/
├── index.html     ← entire app (HTML + CSS + JS)
├── manifest.json  ← PWA manifest
├── sw.js          ← service worker (offline support)
└── README.md      ← this file
```
