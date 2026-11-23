# NativeSIP user guide

- [Making and receiving calls](#making-and-receiving-calls)
- [The dialer](#the-dialer)
- [SIP accounts](#sip-accounts)
- [Routing rules: SIP or SIM automatically](#routing-rules-sip-or-sim-automatically)
- [Travel mode](#travel-mode)
- [Call recording](#call-recording)
- [Block list and spam filter](#block-list-and-spam-filter)
- [Auto dialer](#auto-dialer)
- [Call quality](#call-quality)
- [Default phone app mode](#default-phone-app-mode)
- [Background and battery](#background-and-battery)
- [Automatic updates](#automatic-updates)

---

## Making and receiving calls

**From your phone's normal dialer:** dial as usual. When Android asks **Call with**, pick
**NativeSIP** (or the account name you gave it). To skip the question, set a default in your
dialer's settings under *Calling accounts*.

**From NativeSIP:** tap the keypad button, dial, and press the green call button. The chip above
the keypad shows which account will be used. Tap it to choose a different one for this call.

**Incoming SIP calls** ring like normal calls, on the lock screen too, and use your phone's own
call screen. They show up in your call history with the account name.

> If the **Calling accounts** switch for NativeSIP is off, NativeSIP still works but shows its own
> call screen instead of the phone's. A banner in the app reminds you to switch it on.

## The dialer

- **Tabs:** Favourites (starred contacts and people you call often), Recents, Contacts.
- **Search bar:** find contacts by name or number.
- **Keypad:** type digits or letters (T9) to find contacts. Tap the number to move the cursor,
  long-press to select or paste. Backspace deletes; long-press backspace clears.
- **Long-press keys:** `0` adds `+`, `*` adds a pause (`,`), `#` adds a wait (`;`),
  `1` calls voicemail.
- **Empty call button:** pressing call with no number fills in the last number you dialled.
- **Recents:** filter by All / Missed / SIP / SIM. Tap a call to expand it: call back from a
  specific account, message, copy, add to contacts, block, or delete.

## SIP accounts

**Settings › SIP accounts** lists every account with a status dot:
green = registered, orange = connecting, red = problem.

- **Add another account:** all accounts stay online at the same time. Give each a name
  (e.g. *Office*, *Personal*); that name is what you'll see in the phone's **Call with** list.
  Each new account must be switched on once in **Calling accounts**.
- **Tap an account** to edit it, make it the **default for calls**, **switch it off** (it stays
  saved but stops receiving calls), or **remove** it.
- Incoming calls are matched to the account they arrived on.

## Routing rules: SIP or SIM automatically

**⋮ › Call routing.** Rules are checked top to bottom; the first match decides which account
places the call.

| Example rule | Effect |
| --- | --- |
| Length at most 4 → Office (SIP) | Office extensions always go over SIP |
| Starts with `+880` → SIM 1 | Local mobile numbers use your SIM |
| Starts with `00` → SIP, remove `00`, add `+` | International calls over SIP, rewritten |

Also on this screen:
- **When no rule matches:** ask every time, the default SIP account, or a specific SIM.
- **Use a SIM when SIP is offline.**
- **Apply to calls from other dialers:** after you allow *call redirection*, rules also apply
  when you dial in the Google Phone app.
- **Test a number:** type a number to see which account it would use.

## Travel mode

**What it's for:** you have a home SIP number (for example a Bangladeshi IP-telephony number)
and you travel abroad. You want every call to go out on that number instead of your SIM, which
would charge roaming rates.

**How it works:** your SIP account lives on your provider's server at home. NativeSIP reaches
that server over any internet connection: hotel Wi-Fi, a local data SIM, anything. When you
call from abroad:

1. Your phone sends the call over the internet to your provider's server at home.
2. The server places the call from your home country, exactly as when you're home.
3. The person you call sees your home SIP number; your provider charges its normal home rate.
   Your phone only uses internet data (roughly 0.3–0.7 MB per minute).

Calls to your SIP number reach you abroad the same way.

**What travel mode adds:** SIP calls always travel over the internet anyway. Travel mode makes
sure you never place a call through the roaming SIM by mistake:

| | Travel mode off | Travel mode on |
| --- | --- | --- |
| Calls from NativeSIP | Follow your routing rules | Always your default SIP account |
| Calls from the Google Phone app | Whatever you pick (SIM = roaming charges) | Moved to SIP automatically* |
| Number saved as `+8801712…` | Sent as is | Sent as `01712…` (local format) |
| Emergency numbers | SIM | Still SIM |

\* Needs *call redirection* allowed (NativeSIP asks when you turn travel mode on).

**Settings › Travel:**
- **Travel mode:** *Automatic when abroad* (default), *Always on*, or *Off*. Automatic switches
  on when your phone connects to a mobile network outside your home country. With the SIM
  switched off (Wi-Fi only) the phone can't tell where you are, so use *Always on*.
- **Home country:** country code (`bd`), calling code (`880`) and local prefix (`0`).
- **Dial home numbers in local format:** sends `+8801712…` as `01712…`.

A ✈ banner on the home screen shows when travel mode is active.

> **Check with your provider before you travel.** Some providers only accept connections from
> home-country internet addresses. If NativeSIP shows *Offline* abroad although your internet
> works, that's the likely reason. Ask your provider, or use a VPN with a server in your home
> country.

## Call recording

- **Manual:** during a SIP call, tap **Record call** in the NativeSIP notification (works while the
  phone's own call screen is showing) or the **Record** button on NativeSIP's call screen.
  Tap again to stop.
- **Automatic:** Settings › Call recording › Record automatically → *All SIP calls* or *Only
  selected numbers*.
- **Recordings:** ⋮ › Call recordings: play, share or delete. Files stay in the app's private
  storage and are deleted if you uninstall.
- Only SIP calls can be recorded; Android doesn't allow apps to record normal SIM calls.

> Recording laws differ by country. In many places you must tell the other person, or get their
> consent, before recording.

## Block list and spam filter

**⋮ › Blocked numbers.**

- **Block a number** or **every number starting with** a prefix (e.g. `+92`, `0960`).
- **Block hidden numbers:** private, withheld, anonymous callers.
- **Block callers not in your contacts.**
- **Block international callers:** numbers from outside your home country.
- From **Recents**, expand a call and tap **Block** / **Unblock**.
- **Recently blocked** lists every blocked attempt with the reason; tap **Allow** to undo.

SIP calls are rejected before they ring (the caller hears *busy*). To filter **SIM calls** too,
tap **Allow** on the banner so NativeSIP becomes your *caller ID & spam app*.

## Auto dialer

**⋮ › Auto dialer** calls a list of numbers one after another over SIP.

1. Paste numbers (one per line, or `Name, number`) or **Import file** (CSV / TXT).
2. Choose settings: pause between calls, ring timeout, retries for busy / no answer, retry delay,
   optional hang-up after a talk time, and which SIP account to call from.
3. Tap **Start**. **Pause**, **Resume**, **Skip** or **Stop** at any time.

Each number shows its result (Answered, No answer, Busy, Failed) with talk time. The dialer never
calls while you're on another call. Progress is saved if the app restarts.

## Call quality

- **Settings › Last call quality:** codec, packet loss in each direction, late packets, round-trip
  delay, score, and plain-language findings about what to fix.
- During a call the NativeSIP notification shows live quality.
- **Settings › Call quality:** codecs, echo cancellation and calibration, jitter buffer (raise it to
  150 ms on busy Wi-Fi or with Bluetooth), adaptive bitrate, SRTP encryption.

Tips for choppy audio: use 5 GHz Wi-Fi rather than 2.4 GHz (especially with a Bluetooth headset),
move closer to the router, or try mobile data.

## Default phone app mode

Optional: **Settings › Default phone app**. NativeSIP then handles **all** calls, SIM and SIP,
with its own call screen (mute, speaker, Bluetooth, hold, keypad, add/merge/swap calls, call
waiting). Switch back any time in Android Settings › Apps › Default apps › Phone app.

## Background and battery

- **Always stay online** keeps a small notification so Android doesn't stop NativeSIP; it shows
  your accounts' status.
- **Start when the phone boots** brings everything back after a restart. Open the app once after a
  reboot so calls answered from the lock screen get microphone access.
- Battery use is low. NativeSIP keeps a light connection to your SIP server.

## Automatic updates

NativeSIP keeps itself up to date from its GitHub releases.

- It checks for a new version about every 6 hours, and whenever you tap **Settings › Updates ›
  Check for updates**.
- **Automatic updates:** *Download and install automatically* (default), *Tell me when an update is
  out*, or *Off*.
- **Download updates on Wi-Fi only** (default on) avoids using mobile data, which matters when
  roaming. On mobile data you get a notification instead and can tap to update.
- **Allow NativeSIP to install updates** must be switched on once (Settings › Updates shows it if
  it isn't).
- Updates never install during a call or while the auto dialer is running; they wait until you're
  done. Your accounts, settings and recordings are kept, and NativeSIP reconnects by itself a few
  seconds later.
- On Android 12 and newer updates install without asking. Some phones (for example Xiaomi) still show
  their own confirmation screen; tap **Install** or **Update**.
- Every download is checked against the published checksum, and Android only accepts an update signed
  with the same NativeSIP key as the app you have.
