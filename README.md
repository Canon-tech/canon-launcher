# Canon Launcher

**Canon Launcher** is a desktop launcher for **Canon**, a private, invite-only Minecraft: Java Edition server network.

> **NOT AN OFFICIAL MINECRAFT PRODUCT. NOT APPROVED BY OR ASSOCIATED WITH MOJANG OR MICROSOFT.**
> Minecraft is a trademark of Mojang Synergies AB.

**Status:** In development. The source code is private, and this repository is the project's public information page.

---

## What it does

- **Sign in with a Microsoft account** and verify ownership of Minecraft: Java Edition.
- **Launch a Fabric 1.21.11 client** with Canon's server-specific mods.
- **Keep mods and settings up to date automatically**, downloading only changed files.
- **Player access management:** a player who signs in is added to a pending list, and a server administrator approves access by Minecraft username.
- **Optional account features** for the signed-in player: view and change their own skin, switch between saved accounts, and see server status.

## How sign-in works

1. The launcher opens an in-app window that loads the **official Microsoft sign-in page** (OAuth 2.0 authorization code flow with PKCE).
2. The player enters their password **only on Microsoft's page**. The launcher never sees or stores the password.
3. After sign-in the launcher receives only a one-time authorization code and exchanges it for tokens.
4. A device-code sign-in (enter a code at microsoft.com/link in a browser) is available as a fallback.

**Requested Microsoft permissions:** `XboxLive.signin` and `offline_access` only.

**APIs called**

| Purpose | Endpoint |
|---|---|
| Microsoft sign-in | `login.microsoftonline.com/consumers/oauth2/v2.0` |
| Xbox Live / XSTS authentication | `user.auth.xboxlive.com`, `xsts.auth.xboxlive.com` |
| Minecraft login and profile | `api.minecraftservices.com/authentication/login_with_xbox`, `/minecraft/profile` |
| Skin view/change (own account only) | `api.minecraftservices.com/minecraft/profile/skins` |
| Game files | Mojang version manifest, libraries and assets (Mojang servers); Fabric meta (`meta.fabricmc.net`) |

## Privacy and security

- Vanilla game files come **only from Mojang's servers**. Canon does not redistribute Minecraft.
- Sign-in tokens are stored **only on the player's own computer**, in the operating system's secure credential store (Windows Credential Manager).
- The Canon server verifies the Minecraft access token **once** against the official `/minecraft/profile` endpoint and **does not store it**. Only the Minecraft username and UUID are kept, to manage server access.

Details: **[Privacy Policy](PRIVACY.md)** and **[Terms of Use](TERMS.md)**.

## Contact

- Email: psmileamore@gmail.com
- Discord: canon.kor

Privacy requests (access or deletion of your data) and security reports can be sent to the email above.
