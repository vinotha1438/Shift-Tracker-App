# Shift Tracker - deploy steps (all free)

## 1. Firebase project
1. https://console.firebase.google.com -> Add project.
2. Build -> Authentication -> Get started -> enable **Email/Password**.
3. Build -> Firestore Database -> Create database (production mode).
4. Firestore -> Rules tab -> paste contents of `firestore.rules` -> Publish.
5. Project settings (gear) -> Your apps -> Web app (</>) -> register -> copy the `firebaseConfig` values.
6. Open `index.html`, find `const firebaseConfig=` and replace the 4 PASTE_ values.

## 2. Host (pick one)
- Netlify: https://app.netlify.com/drop -> drag this whole folder. Done, you get a link.
- or Firebase Hosting: `npm i -g firebase-tools`, `firebase login`, `firebase init hosting` (public dir = this folder), `firebase deploy`.

## 3. Allow the domain
Authentication -> Settings -> Authorized domains -> add your Netlify/hosting domain.

## 4. Use
Open the link on any phone -> Create account with email -> Add to Home Screen.
Login with the same email on another phone and the shifts show up.
Husband and wife can each use own email, or share one email to see both profiles.
