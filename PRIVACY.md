# NativeSIP privacy policy

_Last updated: 24 November 2026_

NativeSIP is a SIP calling app. It has no accounts with us, no analytics, no advertising and no
tracking. We don't run servers that receive your data.

## What stays on your phone

- **SIP account details** you enter (server, username, password). The password is encrypted with
  a key held in Android's secure Keystore.
- **Settings**, routing rules, the block list and blocked-call history, auto-dialer lists and results.
- **Call recordings**, only if you record calls. They're stored in the app's private storage and
  deleted when you uninstall the app.
- **Call quality reports** for your recent calls.

## What leaves your phone

- **Your SIP provider** (the server you sign in to) receives your login and your calls, as with
  any SIP app. Their privacy policy applies to that.
- **A STUN server** (by default `stun.l.google.com`) only if you turn on STUN or ICE. It sees your
  public IP address so calls can get through firewalls.
- **GitHub** (`api.github.com`, `github.com`), to check for and download app updates, unless you turn
  automatic updates off. These requests carry no account or personal data; GitHub sees your IP
  address and the app name, as with any download.

Nothing else is sent anywhere.

## Permissions and why

| Permission | Used for |
| --- | --- |
| Microphone | Your voice during calls, call recording |
| Phone, call log | Placing calls, showing SIM accounts, Recents, logging SIP calls |
| Contacts | Names and photos, search, favourites, the "unknown caller" filter |
| Notifications, full-screen alerts | Incoming call screen, call controls, status |
| Nearby devices (Bluetooth) | Bluetooth headsets during calls |
| Run in background, start at boot | Staying online so calls can reach you |
| Install apps | Installing NativeSIP's own updates |

Contacts and call history are read on the phone only and never uploaded.

## Contact

Questions: open an issue at <https://github.com/UserYahya/NativeSIP/issues>.
