# Privacy Policy

Last updated: 2026-10-21

This policy applies to **Canon Launcher** and the Canon server network. Canon Launcher is not an official Minecraft product and is not associated with Mojang or Microsoft.

## 1. What we collect

| Data | Purpose | Where it is kept |
|---|---|---|
| Minecraft username and UUID | Identify the player and manage server access (pending, approved, blocked) | Canon server database |
| Access status and timestamps (first and last sign-in) | Access management | Canon server database |
| Device name, launcher version, device token (stored as a hash) | Keep the launcher signed in and revoke a lost device | Canon server database |
| File download records (UUID, file ID, time) | Detect misuse and leaks of server files | Canon server database, deleted after 90 days |
| Request counts per IP address | Abuse prevention (rate limiting) | Kept for about 10 minutes, then deleted |
| Administrator action log | Accountability for access changes | Canon server database |

We do **not** collect your Microsoft password, email address, real name, payment information, or any Microsoft account profile data beyond your Minecraft username and UUID.

## 2. What stays on your computer

- The Microsoft refresh token and the Canon device token are stored **only on your computer**, in the Windows Credential Manager. The Microsoft refresh token is sent only to Microsoft. The device token is sent to the Canon server only to authenticate your requests.
- The Minecraft access token is used to start the game and to verify ownership. The Canon server checks it once with Mojang's official profile endpoint and **does not store it**.
- The launcher's settings, account list (username and UUID), and downloaded game files are stored in your user folder.

## 3. Sign-in

Sign-in uses Microsoft's official sign-in page (OAuth 2.0 with PKCE). Your password is entered only on Microsoft's page and is never seen by the launcher or by Canon. The launcher requests only the `XboxLive.signin` and `offline_access` permissions.

## 4. Sharing

We do not sell your data and do not share it with third parties for advertising or any other purpose. The launcher communicates with Microsoft, Xbox Live, Mojang and Fabric services as needed to sign in and install the game. The Canon server runs on Cloudflare's infrastructure (Workers, D1, R2), which processes data on our behalf.

## 5. Retention and deletion

- Download records are deleted automatically after 90 days, and rate-limit counters after about 10 minutes.
- You can sign out of any account in the launcher at any time, which removes that account's tokens from your computer.
- To access or delete the data held on the Canon server (username, UUID, access status, device records), email **psmileamore@gmail.com** and include your Minecraft username. We will respond within 14 days. Deleting your record also ends your access to the server network.

## 6. Children

Canon Launcher is not directed to children under 13. We do not knowingly collect data from children under 13, and Microsoft's own account rules for minors apply to sign-in.

## 7. Changes and contact

If this policy changes, the updated version will be published in this repository with a new date.

Contact: psmileamore@gmail.com or Discord `canon.kor`.
