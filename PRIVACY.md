# Privacy Policy / 개인정보 처리방침

Last updated: 2026-10-21 · 최종 수정일: 2026-10-21

This policy applies to **Canon Launcher** and the Canon server network. Canon Launcher is not an official Minecraft product and is not associated with Mojang or Microsoft.
이 방침은 **Canon Launcher**와 Canon 서버 네트워크에 적용됩니다. Canon Launcher는 Minecraft 공식 제품이 아니며 Mojang·Microsoft와 관련이 없습니다.

## 1. What we collect / 수집하는 정보

| Data / 항목 | Why / 목적 | Where / 보관 위치 |
|---|---|---|
| Minecraft username and UUID / 마인크래프트 닉네임, UUID | Identify the player and manage server access (pending, approved, blocked) / 플레이어 식별, 서버 이용 권한 관리 | Canon server database |
| Access status and timestamps (first and last sign-in) / 이용 상태와 접속 시각(최초·마지막 로그인) | Access management / 이용 관리 | Canon server database |
| Device name, launcher version, device token (stored as a hash) / 기기 이름, 런처 버전, 기기 토큰(해시로 저장) | Keep the launcher signed in and revoke a lost device / 로그인 유지, 분실 기기 차단 | Canon server database |
| File download records (UUID, file ID, time) / 파일 내려받기 기록 | Detect misuse and leaks of server files / 서버 파일 무단 유출 추적 | Canon server database, deleted after 90 days / 90일 후 삭제 |
| Request counts per IP address / IP 주소별 요청 횟수 | Abuse prevention (rate limiting) / 남용 방지 | Kept for about 10 minutes, then deleted / 약 10분 후 삭제 |
| Administrator action log / 관리자 작업 기록 | Accountability for access changes / 이용 권한 변경 이력 | Canon server database |

We do **not** collect your Microsoft password, email address, real name, payment information, or Microsoft account profile beyond your Minecraft username and UUID.
Microsoft 비밀번호, 이메일 주소, 실명, 결제 정보, 그리고 닉네임·UUID 이외의 Microsoft 계정 정보는 **수집하지 않습니다.**

## 2. What stays on your computer / 사용자 PC에만 저장되는 정보

- The Microsoft refresh token and the Canon device token are stored **only on your computer**, in the Windows Credential Manager. They are not sent to Canon's server (the device token is sent to authenticate requests; the Microsoft refresh token is sent only to Microsoft).
  Microsoft 갱신 토큰과 Canon 기기 토큰은 **사용자 PC**의 Windows 자격 증명 관리자에만 저장됩니다. Microsoft 갱신 토큰은 Microsoft에만 전송됩니다.
- The Minecraft access token is used to start the game and to verify ownership. The Canon server checks it once with Mojang's official profile endpoint and **does not store it**.
  마인크래프트 액세스 토큰은 게임 실행과 정품 확인에 사용됩니다. Canon 서버는 이를 Mojang 공식 프로필 API로 한 번만 확인하고 **저장하지 않습니다.**
- The launcher's settings, account list (username and UUID), and downloaded game files are stored in your user folder.
  런처 설정, 계정 목록(닉네임·UUID), 내려받은 게임 파일은 사용자 폴더에 저장됩니다.

## 3. Sign-in / 로그인

Sign-in uses Microsoft's official sign-in page (OAuth 2.0 with PKCE). Your password is entered only on Microsoft's page and is never seen by the launcher or Canon. The launcher requests only the `XboxLive.signin` and `offline_access` permissions.
로그인은 Microsoft 공식 로그인 페이지(OAuth 2.0, PKCE)로 이루어집니다. 비밀번호는 Microsoft 페이지에만 입력되며 런처와 Canon은 알 수 없습니다. 런처는 `XboxLive.signin`, `offline_access` 권한만 요청합니다.

## 4. Sharing / 제3자 제공

We do not sell your data and do not share it with third parties for advertising or any other purpose. The launcher communicates with Microsoft, Xbox Live, Mojang and Fabric services as needed to sign in and install the game, and the Canon server runs on Cloudflare's infrastructure (Workers, D1, R2), which processes data on our behalf.
개인정보를 판매하지 않으며, 광고 등 다른 목적으로 제3자에게 제공하지 않습니다. 로그인과 게임 설치를 위해 Microsoft, Xbox Live, Mojang, Fabric 서비스와 통신하며, Canon 서버는 Cloudflare 인프라(Workers, D1, R2)에서 동작합니다.

## 5. Retention and deletion / 보관 기간과 삭제

- Download records are deleted automatically after 90 days; rate-limit counters after about 10 minutes.
  내려받기 기록은 90일, 요청 횟수 기록은 약 10분 후 자동 삭제됩니다.
- You can sign out of any account in the launcher at any time, which removes its tokens from your computer.
  런처에서 언제든 계정을 로그아웃할 수 있으며, 이때 해당 계정의 토큰이 PC에서 삭제됩니다.
- To access or delete your data held on the Canon server (username, UUID, access status, device records), email **psmileamore@gmail.com** from any address and include your Minecraft username. We will respond within 14 days. Deleting your record also ends your access to the server network.
  Canon 서버에 저장된 정보(닉네임, UUID, 이용 상태, 기기 기록)의 열람·삭제는 **psmileamore@gmail.com**으로 마인크래프트 닉네임과 함께 요청해 주세요. 14일 이내에 답변합니다. 삭제하면 서버 네트워크 이용 권한도 함께 종료됩니다.

## 6. Children / 어린이

Canon Launcher is not directed to children under 13. We do not knowingly collect data from children under 13, and Microsoft's own account rules for minors apply to sign-in.
Canon Launcher는 만 13세 미만을 대상으로 하지 않으며, 만 13세 미만의 정보를 알면서 수집하지 않습니다. 미성년자 계정의 로그인에는 Microsoft의 규정이 적용됩니다.

## 7. Changes and contact / 변경과 문의

If this policy changes, the updated version will be published in this repository with a new date.
방침이 바뀌면 이 저장소에 새 날짜와 함께 공개합니다.

Contact / 문의: psmileamore@gmail.com · Discord canon.kor
