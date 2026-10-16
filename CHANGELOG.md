# Changelog

Versions follow [semantic versioning](https://semver.org): `MAJOR.MINOR.PATCH`. While below 1.0, a
MINOR bump means new features or changed behaviour, a PATCH bump means fixes only.

## [0.4.0] - 2026-10-16

- Power saving (Settings → Power saving): when the screen turns off, dim the lights (with a fade), show a
  preset, or turn them off; lights off while the PC sleeps, shuts down or logs off. Your own lighting
  comes back by itself.
- "When RGB Studio closes" now also applies when Windows shuts down or logs off.
- After sleep the service reconnects to OpenRGB, so devices that reset in standby are set up again.
- Tray icon: lights on/off, presets, open the window. Closing the window can leave just the tray running
  (a few MB), and it can start in the tray at login (Settings → App & updates).
- New-version notice: a bar at the top when a newer release is out (can be turned off).
- Report a problem: one click copies a diagnostics report (versions, OpenRGB, devices, zones, recent log;
  without your user folder name) and opens a GitHub issue to paste it into.
- Links in the app open in your browser.
- Service log records late frames, slow writes to OpenRGB and any message OpenRGB sends by itself, with
  the time, to track down rare light glitches.

## [0.3.2] - 2026-10-16

- Save a built-in mode to each device's own memory (Settings → When RGB Studio isn't running): it shows
  from power-on until the service starts, and after it stops. MSI boards and Corsair RAM supported.
- Faster start at login: the service starts through Task Scheduler as soon as you log in instead of
  waiting behind other startup apps, and retries OpenRGB every second while it's starting.

## [0.3.1] - 2026-10-16

- Clear guidance when nothing can be controlled: Setup and Studio explain whether OpenRGB isn't
  reachable (install it, run as administrator, start the SDK server) or found no devices (run as
  administrator, quit iCUE and other RGB software, use OpenRGB 1.0+, rescan).
- Install guide and README state up front that OpenRGB is required, with a "no devices" fix.
- Licensed under MIT.
- Removed the original Python version (replaced by the service and app since 0.2.0).
- docs/EFFECTS.md is generated from the service's effect registry (`rgbd --effects-json`).

## [0.3.0] - 2026-10-15

- Music capture in the service: whole desktop or chosen apps (WASAPI loopback), stereo analysis with
  beats, hi-hats, tone and sections, light delay.
- Screen capture in the service: DXGI desktop duplication, shrunk on the GPU; real monitor resolutions.
- Music and screen capture run only while one of their effects is on the lights and stop by
  themselves; a minimized app gets no preview frames.
- Windows installer `RGB Studio Setup.exe` with uninstaller (Windows Settings → Apps), start at login
  via the standard Startup entry, Start menu and desktop shortcuts. Replaces `install.ps1`.
- "Saving…" / "Applying to devices…" indicator while changes reach the hardware.
- Studio layout fixed on small or scaled windows; the app opens at a size that fits scaled screens.
- App and service versions shown in Settings → Background service, with a warning if they differ.

## [0.2.0] - internal builds

- The `rgbd` service (Rust): keeps the lighting running with no app open; own OpenRGB SDK client;
  control API on 127.0.0.1:7420 with health check.
- RGB Studio desktop app (Tauri): the UI in a window; shows whether the service is running, not
  responding or stopped; start / restart / stop / kill; the lights switch follows the service.
- `rgbctl` command-line client for Windows and Linux.
- Settings import from older installs.

## [0.1.0]

- The original Python version: FastAPI server + web UI, 39 effects, presets, paint, layers, sensors,
  music and screen effects.
