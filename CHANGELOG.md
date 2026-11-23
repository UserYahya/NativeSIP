# Changelog

## 1.0.3 (24 November 2026)

- New: **automatic updates.** NativeSIP checks this page for new releases, downloads the right APK
  for your phone, verifies it and installs it, by default on Wi-Fi only and never during a call.
  Settings › Updates lets you check now, choose automatic / notify-only / off, and allow NativeSIP
  to install updates.

From 1.0.3 on you won't need to download new versions by hand. Install 1.0.3 over your current
version once; your accounts and settings are kept.

## 1.0.2 (18 November 2026)

- New: **Settings › About** shows who made NativeSIP (Muhammad Yahya), a contact email
  (hello@yahya.bd), a link to report a problem or suggest a feature on GitHub, and a link to the
  user guide.

Install it over 1.0.1; your accounts and settings are kept.

## 1.0.1 (18 November 2026)

- Fixed: on the auto dialer screen the Pause, Skip and Stop buttons no longer squeeze together on
  narrower phones; they wrap onto a second line instead.

Install it over 1.0.0; your accounts and settings are kept.

## 1.0.0 (18 November 2026)

First public release.

- SIP accounts appear beside the SIM cards in the phone's own dialer; incoming SIP calls use the
  native call screen and call history
- Multiple SIP accounts online at the same time
- Material You dialer with favourites, recents, contacts, T9 search and an editable number field
- Always online: boot start, background service, re-registration after network changes
- HD voice (Opus, G.722), G.711, echo cancellation, adaptive jitter buffer, SRTP
- Call quality report after every call
- Travel mode: calls go out on your home SIP number while abroad
- Routing rules for automatic SIP/SIM selection with number rewriting
- Call recording (automatic or manual)
- Block list and spam filter for SIP and SIM calls
- Auto dialer for call lists
- Optional default phone app mode with its own call screen
