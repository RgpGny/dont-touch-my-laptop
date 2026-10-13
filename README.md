<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://rgpgny.github.io/dont-touch-my-laptop/assets/icon-dark.png" />
    <img src="https://rgpgny.github.io/dont-touch-my-laptop/assets/icon.png" width="112" alt="" />
  </picture>
</p>

<h1 align="center">Don't Touch My Laptop</h1>

<p align="center">
  <b>Arm it. Walk away. Anyone who touches it gets caught.</b><br />
  A free anti-theft alarm for your Mac.
</p>

<p align="center">
  <a href="https://github.com/RgpGny/dont-touch-my-laptop/releases/latest"><b>Download for macOS</b></a> ·
  <a href="https://rgpgny.github.io/dont-touch-my-laptop/">Website</a> ·
  <a href="https://buymeacoffee.com/ragipgunay">Buy me a coffee ☕</a>
</p>

<p align="center">
  <img src="https://rgpgny.github.io/dont-touch-my-laptop/assets/home.jpg" width="760" alt="The app's home screen" />
</p>

Working from a café and need the restroom or another coffee? Arm the alarm and leave your laptop on the table. If anyone opens or closes the lid, unplugs the charger, picks it up or touches the keyboard, it plays a **full-volume siren** that only stops with **your password or Touch ID**. It takes a **photo** of the person and sends it to **your phone**.

## Features

- **Watches everything:** lid, lid angle, charger, motion, keyboard/trackpad/mouse, USB and Thunderbolt devices, SD cards and disks, headphones and speakers, external displays, Bluetooth devices, network, system clock, screen lock/sleep/shutdown attempts and the volume keys. Turn each one on or off.
- **Loud and stubborn:** the volume is forced to 100%, mute is undone, and the sound goes to the built-in speakers. Closing the lid doesn't stop it.
- **A spoken warning** in your language ("This computer is being stolen!") between siren bursts. 40 languages.
- **Photo and location:** the front camera takes a photo of the thief; the location is recorded.
- **Phone alerts** with the photo through the free [ntfy](https://ntfy.sh) app (iPhone and Android). Scan a QR code in the app to connect; no account needed.
- **Lock screen:** while armed, every screen is covered and app switching, Force Quit and similar shortcuts are blocked.
- **Encrypted history** of every alarm, photos included, readable only with your password.
- **Private by design:** no accounts, no analytics, no servers of ours. Everything stays on your Mac, except the alerts you send to your own phone.
- **Automatic updates** from this page's releases.

## Install

Requires **macOS 13 Ventura or later** (Apple Silicon and Intel).

1. Download the `.dmg` from the [latest release](https://github.com/RgpGny/dont-touch-my-laptop/releases/latest).
2. Open it and drag **Don't Touch My Laptop** into **Applications**.
3. Open the app. macOS will say it can't verify the developer, because the app isn't notarized by Apple (that needs a paid Apple account). Click **Done**, then go to **System Settings → Privacy & Security**, scroll down and click **Open Anyway**. You only do this once.

   <details>
   <summary>Or use Terminal</summary>

   ```bash
   xattr -dr com.apple.quarantine "/Applications/Don't Touch My Laptop.app"
   ```

   </details>

4. The setup screen walks you through the rest: choose a PIN or password, install the protection helper (asks for your Mac password once) and grant the permissions.

Updates install themselves: the app checks this page every few hours, downloads new versions in the background and installs them when you restart it.

## How it works

1. **Arm it** from the menu bar, the main window or <kbd>⌘</kbd><kbd>⇧</kbd><kbd>L</kbd>. You get a short countdown to walk away (or close the lid).
2. **Someone touches it:** the screen wakes up, a short warning beep plays and a photo is taken. You can still enter your password during these few seconds.
3. **Full siren** if the password isn't entered. Your phone gets the photo and location. It keeps going with the lid closed or in a bag.
4. **Stop it** with your PIN/password or Touch ID. Everything goes back to how it was.

## Honest limits

- It can't stop someone from **holding the power button** to force a shutdown.
- It deters, exposes and alerts. It can't physically stop someone from walking away with your laptop.
- Motion detection uses the built-in motion sensor on Apple Silicon MacBooks. Where there isn't one, the camera watches for movement in front of the laptop instead.
- Phone alerts need an internet connection on the laptop.

## Privacy

- No accounts, telemetry or analytics.
- Photos, locations and the alarm history are stored **encrypted** on your Mac.
- Phone alerts go through [ntfy.sh](https://ntfy.sh) to a random topic only you know. You can use your own ntfy server instead.
- Without location permission, the app can use an approximate IP location during an alarm (via ipwho.is). You can turn this off.

## FAQ

**Is it really free?** Yes, no ads and no paid version. If it helps you, you can [buy me a coffee](https://buymeacoffee.com/ragipgunay).

**Why does it need my Mac password once?** To install a small helper that keeps the Mac awake with the lid closed while armed and restarts the alarm if someone kills the app.

**Can a thief stop it with my Mac password?** No. Only the app's own PIN/password or your Touch ID stops the alarm.

**Windows?** Planned for a later version.

## Feedback

Found a bug or have an idea? [Open an issue](https://github.com/RgpGny/dont-touch-my-laptop/issues/new/choose).

---

Made by [Ragıp Günay](https://github.com/RgpGny). The source code is private for now; this repository hosts the releases, the website and the issue tracker.
