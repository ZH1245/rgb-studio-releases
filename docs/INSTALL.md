# Installing RGB Studio

RGB Studio has two parts:

- **rgbd**, a small background service that runs your lighting (a few MB of memory, no window). It
  starts when you log in and keeps your lights going whether or not the app is open.
- **RGB Studio**, the app you open to change things, or `rgbctl` on the command line.

Nothing else to install: no Rust, Node or Python.

## Before you start

RGB Studio **requires OpenRGB**: OpenRGB talks to the hardware, RGB Studio controls the lights through it.

1. Install [OpenRGB](https://openrgb.org/releases.html) (1.0 or newer) and open it **as administrator** once so it detects
   your devices, including RAM. Check that your devices show up in OpenRGB's own window.
2. In OpenRGB: **SDK Server → Start Server**. Turn on *Start at login* and *Start server* in OpenRGB's
   settings so it's ready every time.
3. Close other RGB software (MSI Center / Mystic Light, iCUE, SignalRGB…). Two programs controlling
   the same lights will fight.

## Windows

1. Download **`RGB Studio Setup <version>.exe`** (about 2.5 MB) from the
   [Releases](https://github.com/ZH1245/rgb-studio-releases/releases) page.
2. Run it and press **Install**. No admin rights needed.
3. Open **RGB Studio** from the Start menu or the desktop. The first screen asks about your devices:
   add the fan headers, RAM and other zones you want to control, and set how many fans and LEDs each has.

What the installer does: installs the app, the service and `rgbctl` to `%LOCALAPPDATA%\RGB Studio`,
adds Start menu and desktop shortcuts, makes the service start as soon as you log in (a **Task
Scheduler** entry named *RGB Studio*, so it doesn't wait behind other startup apps; disable it there if you
ever want to), and starts it now. It installs no drivers. Your settings are kept in `%APPDATA%\RGB Studio`.

**Update:** run the new version's installer. Your settings stay.

**Uninstall:** Windows **Settings → Apps → Installed apps → RGB Studio → Uninstall** (or *Uninstall RGB
Studio* in the Start menu). It stops the service and removes the app and its start-at-login entry. Tick
**Delete the application data** to remove your settings and presets too; otherwise they stay for a
later reinstall.

Windows may show a SmartScreen warning for a new, unsigned program: **More info → Run anyway**.

## Coming from an older RGB Studio

The app offers this itself: on the welcome screen, or under **Settings → Import settings**, paste the
path of the old `data` folder (the one with `layout.json` and `state.json`) and press **Import**. From
the command line: `rgbctl import <path-to-data-folder>`.

## Command line

`rgbctl` is installed next to the app: on Windows run it as
`"%LOCALAPPDATA%\RGB Studio\rgbctl.exe"` (or add that folder to your PATH).

```
rgbctl status              what's connected, current preset, frame rate
rgbctl off | on            lights off / on
rgbctl brightness 40       master brightness in %
rgbctl load "Hearth"       apply a preset
rgbctl effect aurora palette=ocean speed=0.6
rgbctl --help              everything else
```

## Anti-cheat (Valorant, FACEIT, EAC, BattlEye…)

- **RGB Studio itself** (app, `rgbd`, `rgbctl`) runs as a normal program: no drivers, no admin rights,
  and it never opens, reads or injects into games. It only talks to OpenRGB over a local network
  socket. Anti-cheats have no reason to react to it.
- **OpenRGB** is the part to know about. USB lighting controllers need no driver, but RAM and some
  motherboard lighting are reached over SMBus, and for that OpenRGB loads a kernel driver (older
  versions: WinRing0, which Windows Defender and some anti-cheats treat as vulnerable; newer versions
  use PawnIO). The usual result is a game refusing to start until the driver is gone, not a ban, but
  anti-cheat rules change and nobody outside those companies can promise anything.
- **Optional sensors** from LibreHardwareMonitor use the same kind of driver, which is why that switch is
  off by default.
- **Safest setup for competitive games:** use an OpenRGB version without the SMBus driver (fans and other
  USB devices still work; RAM lighting won't), or close OpenRGB before you play. RGB Studio waits and
  reconnects by itself when OpenRGB comes back.

## Troubleshooting

| Problem | Fix |
| --- | --- |
| The page doesn't open | The service isn't running: start the "RGB Studio" task in Task Scheduler, or run `rgbd.exe` from the install folder. Its log is `%APPDATA%\RGB Studio\rgbd.log`. |
| "Waiting for OpenRGB" / "Can't reach OpenRGB" | Install OpenRGB, open it, and start its SDK server. RGB Studio reconnects by itself. |
| No devices, even in OpenRGB's own window (e.g. Corsair RAM) | RGB Studio only sees what OpenRGB detects. Run OpenRGB **as administrator** (RAM and many boards use SMBus, which needs it), fully quit iCUE / MSI Center / Armoury Crate / SignalRGB (also from the tray), use OpenRGB 1.0 or newer (DDR5 support), then OpenRGB → Settings → **Rescan devices**. |
| Lights flicker or fight | Another RGB program is still running. Close it. |
