# Canon Launcher

**Canon Launcher** is a desktop launcher for **Canon**, a private, invite-only Minecraft: Java Edition server network.
Canon Launcher는 초대받은 사용자만 이용하는 마인크래프트 자바 에디션 서버 네트워크 **Canon**의 전용 런처입니다.

> **NOT AN OFFICIAL MINECRAFT PRODUCT. NOT APPROVED BY OR ASSOCIATED WITH MOJANG OR MICROSOFT.**
> Minecraft is a trademark of Mojang Synergies AB. / Minecraft는 Mojang Synergies AB의 상표입니다.

**Status / 상태:** In development. The source code is private, and this repository is the project's public information page. / 개발 중이며 소스 코드는 비공개입니다. 이 저장소는 프로젝트 정보를 공개하는 용도입니다.

---

## What it does / 기능

- **Sign in with a Microsoft account** and verify ownership of Minecraft: Java Edition.
  Microsoft 계정으로 로그인하고 마인크래프트 자바 에디션 보유 여부를 확인합니다.
- **Launch a Fabric 1.21.11 client** with Canon's server-specific mods.
  Canon 서버 전용 모드가 포함된 Fabric 1.21.11 클라이언트를 실행합니다.
- **Keep mods and settings up to date automatically**, downloading only changed files.
  변경된 파일만 내려받아 모드와 설정을 자동으로 최신 상태로 유지합니다.
- **Player access management:** a player who signs in is added to a pending list, and a server administrator approves access by Minecraft username.
  로그인한 플레이어는 대기 목록에 올라가고, 서버 관리자가 닉네임으로 이용을 승인합니다.
- **Optional account features** for the signed-in player: view and change their own skin, switch between saved accounts, and see server status.
  로그인한 플레이어 본인의 스킨 확인·변경, 계정 전환, 서버 상태 표시.

## How sign-in works / 로그인 방식

1. The launcher opens an in-app window that loads the **official Microsoft sign-in page** (OAuth 2.0 authorization code flow with PKCE).
   런처 안의 창에 **Microsoft 공식 로그인 페이지**를 띄웁니다 (OAuth 2.0 Authorization Code + PKCE).
2. The player enters their password **only on Microsoft's page**. The launcher never sees or stores the password.
   비밀번호는 Microsoft 페이지에만 입력되며, 런처는 비밀번호를 보거나 저장하지 않습니다.
3. After sign-in the launcher receives only a one-time authorization code and exchanges it for tokens.
   로그인이 끝나면 일회용 인증 코드만 받아 토큰으로 교환합니다.
4. A device-code sign-in (enter a code at microsoft.com/link in a browser) is available as a fallback.
   창을 열 수 없는 환경을 위해 브라우저에서 코드를 입력하는 방식도 제공합니다.

**Requested Microsoft permission / 요청하는 권한:** `XboxLive.signin` and `offline_access` only.

**APIs called / 호출하는 API**

| Purpose | Endpoint |
|---|---|
| Microsoft sign-in | `login.microsoftonline.com/consumers/oauth2/v2.0` |
| Xbox Live / XSTS authentication | `user.auth.xboxlive.com`, `xsts.auth.xboxlive.com` |
| Minecraft login and profile | `api.minecraftservices.com/authentication/login_with_xbox`, `/minecraft/profile` |
| Skin view/change (own account only) | `api.minecraftservices.com/minecraft/profile/skins` |
| Game files | Mojang version manifest, libraries and assets (Mojang servers); Fabric meta (`meta.fabricmc.net`) |

## Privacy and security / 개인정보와 보안

- Vanilla game files come **only from Mojang's servers**. Canon does not redistribute Minecraft.
  게임 본체 파일은 **Mojang 서버에서만** 받으며, Canon은 Minecraft를 재배포하지 않습니다.
- Sign-in tokens are stored **only on the player's own computer**, in the operating system's secure credential store (Windows Credential Manager).
  로그인 토큰은 **플레이어 본인의 PC**, 운영체제 보안 저장소(Windows 자격 증명 관리자)에만 저장됩니다.
- The Canon server verifies the Minecraft access token **once** against the official `/minecraft/profile` endpoint and **does not store it**. Only the Minecraft username and UUID are kept, to manage server access.
  Canon 서버는 마인크래프트 액세스 토큰을 공식 `/minecraft/profile`로 **한 번만 검증하고 저장하지 않습니다.** 서버 이용 관리를 위해 닉네임과 UUID만 보관합니다.

Details: **[Privacy Policy](PRIVACY.md)** · **[Terms of Use](TERMS.md)**

## Contact / 연락처

- Email: psmileamore@gmail.com
- Discord: canon.kor

Privacy requests (access or deletion of your data) and security reports can be sent to the email above.
개인정보 열람·삭제 요청과 보안 제보는 위 이메일로 보내 주세요.
