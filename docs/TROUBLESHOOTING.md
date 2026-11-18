# Troubleshooting

## "Wrong username or password" / "Account not found"

Check the username, password and domain from your provider. Some providers need a separate
**Auth ID** (Advanced settings). Copy the password carefully; it's case-sensitive.

## "Can't reach the SIP server" / stays on "Connecting…"

- Check the **domain** and **port** (Advanced settings). Common ports: 5060 (UDP/TCP), 5061 (TLS).
- Try another **transport**: some networks block UDP; switch to TCP.
- Some Wi-Fi networks (offices, hotels) block SIP. Try mobile data to compare.
- Abroad: your provider may only accept connections from your home country. See
  [Travel mode](USER_GUIDE.md#travel-mode).

## NativeSIP doesn't appear in the "Call with" list

Switch it on in **Calling accounts** (setup checklist step 2, or Settings › Calling accounts).
Each additional SIP account must be switched on separately.

## Incoming calls don't arrive when the phone is idle

1. Settings › Background: **Always stay online** and **Start when the phone boots** on.
2. **Battery optimisation** off for NativeSIP.
3. Your phone maker's **autostart / background** setting on. See the
   [installation guide](INSTALL.md#extra-settings-for-some-phone-makers).
4. Check the NativeSIP notification shows **Online**.

## Choppy or robotic audio

1. After the call, open **Settings › Last call quality**. It says whether the network or the
   device is the problem.
2. Lost or late packets → network: use 5 GHz Wi-Fi, move closer to the router, or try mobile data.
   Raise **Settings › Jitter buffer** to 150 ms.
3. Network clean but audio still choppy on a Bluetooth headset → Bluetooth link: keep the phone
   close to the headset, or try the earpiece.

## One-way audio or no audio

- Turn on **STUN** (Settings › Network); if your provider supports it, also **ICE**.
- Try **TCP** transport.
- After a reboot, open NativeSIP once so the microphone can be used in the background.
- Make sure the microphone permission is allowed.

## Echo

Settings › Call quality › **Calibrate echo canceller** in a quiet room, and keep **Echo
cancellation** on.

## Calls show the wrong number format at the provider

Settings › Travel › **Dial home numbers in local format** converts `+8801712…` to `01712…`.
Settings › Calls › **International "+" prefix** can send `+` as `00`. Routing rules can remove or
add prefixes for specific numbers.

## Still stuck?

[Open an issue](../../../issues) with your phone model, Android version, what you tried, and the
text from **Settings › Last call quality** if it's a call problem. Never post your SIP password.
