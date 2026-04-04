Private Space: Firebase + Google Admin

What changed:
- Normal users still sign in with username + password
- Admin signs in with Google only
- Allowed admin Google account: karthickpraveen072@gmail.com

Important Firebase setup:
1. In Firebase Console, enable Authentication
2. Turn on Google sign-in provider
3. Add your GitHub Pages domain to Authorized domains in Firebase Authentication

This build still uses:
- Realtime Database for chat
- Storage for media
- GitHub Pages for frontend hosting

Reminder:
This is still a prototype. Since user accounts are app-managed in Realtime Database instead of full Firebase Auth for everyone, the database/storage rules remain loose for the static app to work.
