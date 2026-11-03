# FORGE — Firebase profile integration update

## Included
- Keeps the existing FORGE PWA interface, logo, phone OTP sign-in and local project UI.
- Adds Firestore profile creation on first successful sign-in at `users/{Firebase UID}`.
- Loads the saved profile on later sign-ins.
- Saves profile name, bio and skills to Firestore.
- Adds `firestore.rules.txt` for review and manual publishing.

## Required Firebase action
1. In Firebase Console, open Firestore Database > Rules.
2. Replace the current rules with the contents of `firestore.rules.txt`.
3. Review and publish the rules.
4. Test using a Firebase Authentication test phone number.
5. After login, check Firestore Data > users > the generated UID document.

The rules allow each authenticated user to access only their own profile document. All other collections remain denied. Do not use open rules such as `allow read, write: if true`.

## Important limitations
This update implements only authentication-linked creator profile creation/loading/editing. Projects, uploads, likes, follows, messaging, notifications and admin features are not yet connected to Firestore/Storage.
The existing project data remains in browser local storage and is not automatically migrated or shared between devices.
Phone OTP with real SMS still requires a billing-enabled Firebase project; test phone numbers can be used for development.
Never add Firebase service-account private keys to browser code.
