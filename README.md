# NativeSIP: VoIP Softphone

**Your SIP account as a real phone line on Android.**

NativeSIP puts your SIP / VoIP account right next to your SIM cards in the phone's own dialer.
Pick it in the "Call with" list like a SIM; incoming SIP calls ring on the normal call screen and
appear in your call history. It stays online in the background and starts when the phone boots.

[**Download the latest APK →**](../../releases/latest)

## Screenshots

<table>
  <tr>
    <td align="center"><img src="docs/screenshots/01-recents.png" width="200" alt="Recents"><br><sub>Recents with SIP and SIM calls</sub></td>
    <td align="center"><img src="docs/screenshots/03-keypad.png" width="200" alt="Keypad"><br><sub>Keypad with contact search</sub></td>
    <td align="center"><img src="docs/screenshots/04-chooser.png" width="200" alt="Call with"><br><sub>Pick a SIP account or SIM</sub></td>
    <td align="center"><img src="docs/screenshots/05-incall.png" width="200" alt="In call"><br><sub>Call screen with HD voice</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="docs/screenshots/06-incoming.png" width="200" alt="Incoming call"><br><sub>Incoming call</sub></td>
    <td align="center"><img src="docs/screenshots/07-settings.png" width="200" alt="Settings"><br><sub>Several accounts online at once</sub></td>
    <td align="center"><img src="docs/screenshots/08-routing.png" width="200" alt="Call routing"><br><sub>Automatic SIP/SIM routing</sub></td>
    <td align="center"><img src="docs/screenshots/09-blocked.png" width="200" alt="Blocked numbers"><br><sub>Block list and spam filter</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="docs/screenshots/10-recordings.png" width="200" alt="Call recordings"><br><sub>Call recordings</sub></td>
    <td align="center"><img src="docs/screenshots/11-autodialer.png" width="200" alt="Auto dialer"><br><sub>Auto dialer campaigns</sub></td>
    <td align="center"><img src="docs/screenshots/02-favorites.png" width="200" alt="Favourites"><br><sub>Favourites</sub></td>
    <td align="center"><img src="docs/screenshots/12-contacts.png" width="200" alt="Contacts"><br><sub>Contacts</sub></td>
  </tr>
</table>

<sub>Screenshots use made-up names, numbers and accounts.</sub>

---

## Features

**Built into the phone**
- Appears beside your SIM cards in Google Phone and other dialers
- Incoming SIP calls use the phone's own call screen, ringtone and call history
- Always online: starts at boot, survives being swiped away, re-registers after network changes
- Optional: make NativeSIP your default phone app for SIM calls too

**Dialer**
- Clean Material You design: Favourites, Recents, Contacts, search
- Slide-up keypad with contact search (T9), editable number with cursor, paste, long-press 0 for +
- Full call screen: mute, speaker / Bluetooth / headset, hold, keypad (DTMF), add call, swap, transfer

**Accounts and routing**
- Several SIP accounts online at the same time, each with its own name in the dialer
- UDP, TCP or TLS, custom ports, outbound proxy, separate auth ID
- Routing rules: pick SIP or a specific SIM automatically by prefix, length or pattern, with number rewriting
- **Travel mode**: abroad, every call goes out on your home SIP number instead of a roaming SIM

**Call quality**
- HD voice where your provider supports it (Opus, G.722), plus G.711
- Echo cancellation, adaptive jitter buffer, adaptive bitrate, optional SRTP encryption
- Quality report after every call: packet loss, late packets, delay, and what to fix

**More**
- Call recording: automatic or on demand, stored privately on the phone
- Block list and spam filter for SIP and SIM calls
- Auto dialer: call a list of numbers one after another with retries and results

## Get started

1. [Install NativeSIP](docs/INSTALL.md): download the APK and install it.
2. Sign in with the SIP details from your VoIP provider or company PBX.
3. Follow the in-app setup checklist (permissions, Calling accounts, battery).

Then read the [User guide](docs/USER_GUIDE.md) for travel mode, recording, blocking and more.
Something not working? See [Troubleshooting](docs/TROUBLESHOOTING.md).

## Requirements

- Android 8.0 or newer
- A SIP account from a VoIP provider or PBX (NativeSIP doesn't provide phone numbers)
- Internet (Wi-Fi or mobile data) for calls

## Documentation

| Guide | What's in it |
| --- | --- |
| [Installation](docs/INSTALL.md) | Which APK to pick, installing, first-run setup, phone-maker battery settings |
| [User guide](docs/USER_GUIDE.md) | Every feature, step by step |
| [Troubleshooting](docs/TROUBLESHOOTING.md) | Registration, audio, missed calls, call quality |
| [Privacy](PRIVACY.md) | What the app stores and sends |
| [Changelog](CHANGELOG.md) | What changed in each release |

## Feedback

Found a bug or have an idea? [Open an issue](../../issues).

---

© MD. IEAHHIEA. NativeSIP's source code is not published in this repository; this repository holds
documentation and release builds only. Third-party components are listed in [NOTICE.md](NOTICE.md).
