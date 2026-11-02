# FORGE — Build. Showcase. Inspire.

FORGE V1 interface update for GitHub Pages / Android PWA.

## What's included in this update
- Preserves the existing FORGE logo, app name, manifest identity and local project workspace.
- Adds creator dashboard, community overview, messages, notifications and settings screens.
- Adds light/dark theme toggle and local profile visibility preferences.
- Adds project visibility choices (public, unlisted, private), external live-demo links, collaborator credits and creator-controlled download preference in the project editor.
- Adds interface areas for likes, comments/replies, follows, bookmarks, reports, creator analytics, messaging, collaboration requests, account security and admin moderation.
- Adds an update-aware service worker: network-first page refresh, old cache cleanup and an in-app update prompt.

## Important: preview vs. live multi-user features
This is the **interface-first V1 preview**. The existing project data, likes and bookmarks still use this browser's local storage. It does not yet provide real accounts, phone OTP, shared cloud projects, cross-user likes/comments/follows, messaging, notifications, server-side moderation, cloud file storage or enforced permissions. Those features must be connected to Firebase and protected by Firestore/Storage security rules before public use.

The project attachment picker currently records selected file names and basic metadata only; it does not upload or persist file contents. Do not treat that as cloud storage. The creator's download preference is saved locally as a UI setting until backend enforcement is implemented.

Public / unlisted / private visibility is represented in the local preview; secure access enforcement requires Firebase rules. A project's collaborator credit does not grant editing rights. Project editing and deletion remain creator-owned in this preview.

## Deploy to GitHub Pages
1. Keep a backup of your current repository files.
2. Extract this ZIP.
3. Open the extracted `FORGE-Creat-Conquer-Rule-main` folder.
4. Upload the **contents of that folder** to the root of your existing GitHub Pages repository, replacing the old files when GitHub asks.
5. Commit the changes and wait for GitHub Pages to publish.
6. Open the same FORGE website address. The installed home-screen PWA should update its cached page when it next connects and refreshes. If the update banner appears, tap **Update**.

Keep the same repository and published URL. Do not delete the existing home-screen app. If Android continues showing an old page, close FORGE, open it again while online, and allow the service worker to refresh.
