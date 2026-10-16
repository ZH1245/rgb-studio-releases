# RGB Studio

Per-LED lighting for fans, RAM and any other RGB device that [OpenRGB](https://openrgb.org) can control,
in the spirit of SignalRGB, with no cloud, no accounts and no telemetry. RGB Studio loads no drivers.

**[⬇ Download RGB Studio](https://github.com/ZH1245/rgb-studio-releases/releases/latest)** and
**[⬇ OpenRGB](https://openrgb.org/releases.html)** (required).
`RGB Studio Setup <version>.exe` is for Windows 10/11, about 2.5 MB. Run it, press Install. Uninstall from
Windows Settings → Apps.

## What you get

- **A tiny background service** that keeps your lighting running whether or not the app is open (a few MB
  of memory, ~0.1% of one CPU core) and starts when you log in.
- **The RGB Studio app** to change things: shows whether the service is running, and can start or stop it.
- **39 effects**, every color-based one with rainbow, palette, your own or random colors:
  - **Music ♪**: Auto DJ, Stereo field, Beat pulse, Bass relay, Puddles, Spectrum, Mood drift, Sparkle hits.
    Listens to the whole desktop or only the apps you pick (e.g. Spotify), in stereo. *Smooth* or *punchy*.
  - **Screen ▣**: Screen ambience, Screen motion.
  - **Sensors**: GPU / CPU temperature or load on a whole device or just a few LEDs.
  - **Premium**: Relay, Spin & orbit, Silk tides, Aurora, Pacifica, Plasma, Neon chase, Fire, Ripples &
    fireworks, Spotlights, Sweep & lighthouse, Warp galaxy, Bouncing balls, Meteor shower & matrix, Storm.
  - **Classics**: Static/paint, Solid, Breathing/heartbeat, Color flow, Strobe, Candle, Stack/fill/wipe, Wave,
    Comet/scanner, Dissolve, Twinkle/fairy lights, Railway, Sunrise.
- **Every device on its own or all together**: per-device effects, layers on a few LEDs, brightness per
  device type, device and header, painting single LEDs, presets.
- **Light on weak PCs**: music and screen capture only run while one of their effects is showing.
- **`rgbctl`** command line: `rgbctl off`, `rgbctl load "Hearth"`, `rgbctl brightness 40`.

## Before you install

RGB Studio **requires [OpenRGB](https://openrgb.org)**: OpenRGB talks to the hardware, RGB Studio drives the
lights through it. If OpenRGB doesn't see a device, RGB Studio can't either.

1. Install OpenRGB (1.0 or newer), open it **as administrator** so it finds everything (RAM needs this), check
   your devices show in its window, and start its **SDK Server** (also turn on *start at login*).
2. Close other RGB software (MSI Center / Mystic Light, iCUE, SignalRGB…) so they don't fight over the
   same lights.

## Documentation

- **[Install guide](docs/INSTALL.md)**: install, update, uninstall, anti-cheat notes, troubleshooting.
- **[User guide](docs/USER_GUIDE.md)**: every screen and option, recipes.
- **[Effects reference](docs/EFFECTS.md)**: every effect and all of its settings.
- **[Changelog](CHANGELOG.md)**: what changed in each version.

Found a problem? [Open an issue](https://github.com/ZH1245/rgb-studio-releases/issues).

## License

[MIT](LICENSE). Built on open-source libraries, see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
OpenRGB is a separate program (GPL-2.0) that RGB Studio talks to over its network protocol; no OpenRGB
code is included.
