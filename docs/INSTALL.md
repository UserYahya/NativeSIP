# Installing NativeSIP

## 1. Download the right APK

Open the [latest release](../../../releases/latest) on your phone and download one file:

| File | For |
| --- | --- |
| `NativeSIP-<version>-arm64-v8a.apk` | **Almost every phone made since 2017. Pick this if unsure.** |
| `NativeSIP-<version>-armeabi-v7a.apk` | Older 32-bit phones |
| `NativeSIP-<version>-universal.apk` | Works on any phone, but is larger |

Not sure which one? Install the **arm64-v8a** file. If Android says "App not installed" or
"not compatible", use the **universal** file instead.

## 2. Install it

1. Open the downloaded file (from the notification or your Downloads folder).
2. If Android asks, allow your browser or file manager to **install unknown apps**, then go back.
3. Tap **Install**.
4. If Google Play Protect shows a warning about an unknown developer, tap **More details →
   Install anyway**. This appears for apps that aren't from the Play Store.

**Updates install themselves** from version 1.0.3 on: NativeSIP checks for new releases and installs
them automatically (see [Automatic updates](USER_GUIDE.md#automatic-updates)). If you have an older
version, install 1.0.3 or newer once by hand; your accounts and settings are kept.

## 3. Sign in

Open NativeSIP and enter the details from your VoIP provider or PBX:

- **Username / extension**, **Password**, **SIP domain / server**
- Tap **Advanced settings** if your provider gave you a port, transport (UDP / TCP / TLS),
  outbound proxy or a separate auth ID

You can also type `user@domain` in the username field and `domain:port` in the domain field.
NativeSIP waits for the server to accept the login and tells you what went wrong if it doesn't
(wrong password, server unreachable, and so on).

## 4. Finish the setup checklist

The checklist appears after sign-in (later: **⋮ › Setup checklist**). Each step matters:

1. **Allow permissions**: microphone, phone, contacts, call log, notifications, nearby devices
   (Bluetooth).
2. **Show in your phone app**: tap **Open**, find **Calling accounts** (sometimes under
   *SIP accounts* or *Calling accounts settings*) and switch **NativeSIP** on. This is the step that
   puts NativeSIP next to your SIM cards. Android only lets you flip this switch yourself.
3. **Stay online in the background**: allow NativeSIP to ignore battery optimisation.
4. **Autostart** (Xiaomi, Redmi, POCO, Oppo, Realme, OnePlus, Vivo, Huawei, Honor, Samsung, Tecno,
   Infinix…): tap **Open** and allow NativeSIP to start automatically / run in the background.
5. **Full-screen incoming calls** (Android 14+): allow it so calls light up the locked screen.
6. **Allow installing updates**: Settings › Updates › *Allow NativeSIP to install updates*, so new
   versions can install themselves.
7. Optional: **default phone app** and **auto-route calls from any dialer**.

### Extra settings for some phone makers

Some phones stop background apps aggressively. If calls don't arrive when the screen is off:

- **Xiaomi / Redmi / POCO (HyperOS, MIUI):** Settings › Apps › NativeSIP › *Autostart* on;
  *Battery saver* → **No restrictions**. In Recents, long-press NativeSIP and tap the lock icon.
- **Samsung:** Settings › Apps › NativeSIP › Battery → **Unrestricted**. Remove it from
  *Sleeping apps* / *Deep sleeping apps* (Settings › Battery › Background usage limits).
- **Oppo / Realme / OnePlus:** Settings › Apps › NativeSIP › Battery → allow *background activity*
  and *auto launch*.
- **Vivo / iQOO:** Settings › Battery › Background power consumption → allow NativeSIP.
- **Huawei / Honor:** Settings › Battery › App launch › NativeSIP → *Manage manually*, all on.

## 5. Make a test call

Open your phone's normal dialer, dial a number, and choose **NativeSIP** when asked
**Call with**. Or use NativeSIP's own keypad.

Afterwards, **Settings › Last call quality** shows how good the connection was.

## Uninstalling

Settings › Apps › NativeSIP › Uninstall. Your SIP account is signed out and all app data,
including call recordings, is deleted.
