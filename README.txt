Private Space: Firebase Edition

This package keeps your frontend on GitHub Pages and uses Firebase for:
- cross-device sync
- media uploads
- unread dot
- remembered session on device
- voice notes
- calculator-style PIN gate

Files:
- index.html
- manifest.json
- sw.js
- firebase-database-rules.json
- firebase-storage-rules.txt
- firebase-seed-example.json
- icons/

Setup:
1. Create a Firebase project and register a Web app.
2. Enable Realtime Database.
3. Enable Cloud Storage.
4. Upload the files to your GitHub Pages repo.
5. Open the app and paste your Firebase web config into the setup screen.
6. Seed an admin user using the example file or the Firebase console.

Default ideas:
- secret PIN: 0303
- admin username: admin
- admin password: Welcome@123

Important:
This build is a working prototype. Because it uses a custom app login stored in Realtime Database and not Firebase Authentication,
the security rules have to stay broad for the browser to work. Do not treat it as hardened production security.

Recommended first admin seed:
Path:
users/admin

Value:
{
  "username": "admin",
  "displayName": "Admin",
  "passwordHash": "71cbf8f6f5998b01f4c1f6871e3c87c9d6f73770d4af3f2af5f1aaf3217f7e60",
  "avatarUrl": "",
  "colorIndex": 0,
  "isAdmin": true
}

That password hash matches: Welcome@123
