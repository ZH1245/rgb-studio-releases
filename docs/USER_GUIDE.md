# RGB Studio — user guide

A tour of every screen and option. For what each effect does and all of its settings, see
[EFFECTS.md](EFFECTS.md).

- [Words used in the app](#words-used-in-the-app)
- [Top bar and navigation](#top-bar-and-navigation)
- [Studio](#studio)
- [Setup](#setup)
- [Sensors](#sensors)
- [Settings](#settings)
- [How-to recipes](#how-to-recipes)
- [Troubleshooting](#troubleshooting)

## Words used in the app

| Word | Meaning |
| --- | --- |
| **Device** | A zone of an RGB device: a motherboard fan header (e.g. JRAINBOW2), one RAM stick, a GPU's LEDs, a strip. Each header counts as its own device. |
| **Item** | One thing drawn on the canvas: a **fan ring**, a **bar** (RAM, strips) or a **dot** (single-LED zones). A header with 3 daisy-chained fans has 3 items. |
| **Daisy-chain / splitter** | Daisy-chained fans each get their own data, so they can show different things. Fans on a splitter all receive the same data and always look identical, so they appear as one item marked "×5". |
| **Chain** | The order items are linked in (Setup → Chain order). Travelling effects (stack, relay, chase, comet…) flow along it, across devices. |
| **Effect** | The animation a device runs. **Layer**: a second effect drawn on top of some LEDs. |
| **Preset** | A saved look: effects for every device, layers, painted LEDs, brightness and speed. |

## Top bar and navigation

- **Left sidebar** — Studio, Setup, Sensors, Settings, and **Service** at the bottom. Its dot shows the
  background service: green = running, amber = starting / waiting for OpenRGB, red = not responding,
  grey = stopped. Click it for the service panel (see [Settings → Background service](#settings)).
- **Title line** — the controlled device(s) and the live frame rate. It turns amber while waiting for OpenRGB,
  and says *Service: stopped* (or *not responding*) when the service isn't running the lights.
- **☀ Brightness** — master brightness for everything.
- **Speed** — speeds up or slows down every effect (0.05×–4×).
- **⏻ Power** — lights on/off. It only shows *on* while the service is actually running the lights, so it's
  off whenever the service is stopped or killed. Switching on checks the service first: if it isn't running,
  the app starts it, waits until it's healthy, then turns the lights on. While off, effects stop running and
  audio/screen capture stops too.

Closing the app never stops the lights: the service keeps running in the background and starts at login.

## Studio

The main screen: device list on the left, the live canvas in the middle, and the effect controls on the right.

### Devices list

- **All devices** (selected by default) — changes here apply to every device that follows All.
- **One entry per device**, showing its name, its type and size (e.g. "RAM · 10 LEDs", "JRAINBOW2 · 3 fans"), a live
  color bar of its LEDs, and its effect ("Following All · Spin & orbit").
- **OWN** badge — the device runs its own effect. **◆ … on top** — a layer is drawn over it.
- Select a device, then change anything in the panel to give that device its own effect; nothing else changes.
  On narrow windows the list becomes a row of chips above the canvas.

### Canvas

- **Live** — the real-time preview. Clicking an item selects its device; clicking it again goes back to All devices.
- **Arrange** — drag items to where they sit in your case. Spatial effects (sweep, aurora, ripples, screen
  ambience…) use these positions.
- **Paint** — click or drag across LEDs to color them (see Paint tab below).
- The chip at the top right shows the active preset and "· modified" if you changed it.
- **Unsaved-changes bar** (appears after edits): **Revert** (reload the preset), **Save as new…**, **Save**
  (overwrite the preset). With no preset active it offers **Save as preset…**.
- **Quick presets** strip — click a card to load it; ★ = startup preset, amber dot = modified. Scroll with the
  ‹ › arrows or the mouse wheel.

### Effects tab

1. **Brightness card**
   - *Everything* — the master brightness.
   - One row per device type, e.g. **Motherboard** or **RAM ×2** (the count shows how many), with a slider and an
     on/off switch that apply to all of them. Click ▸ to expand: individual devices (RAM 1, RAM 2) or, for a
     motherboard, its headers (Cosmiq, Splitter).
   - **reset all** — every device and header back to 100% and on.
   - Device brightness and on/off are hardware settings: they stay when you switch presets. Header brightness is
     saved with presets.
2. **Device card** — what you're editing and its state: *applies to every device*, *following All devices*, or
   *own effect*.
   - **Make all follow** (All devices) — removes every device's own effect.
   - **Follow All** (a device) — removes this device's own effect.
   - A note appears if a layer covers the whole device ("its own effect isn't visible").
3. **Layers on top** — each layer with its effect, which LEDs it covers and which other devices share it.
   **+ Layer** adds one for the selected device (it starts as *Sensor reactive*). Click a layer to edit it:
   name, which items it covers, **First LED** and **Count** (e.g. only LEDs 1–3 of each fan), **Remove**.
4. **Effect card** — the effect's name, category and description, then **Change** to open the picker (search
   box and category filters: Music, Screen, Sensors, Premium, Classics). Under it, the effect's own settings
   (listed per effect in [EFFECTS.md](EFFECTS.md)). Most effects share:
   - **Colors**: rainbow / palette / custom / random, with the palette row, your color swatches (+ to add,
     × to remove) or **🎲 Shuffle random colors**.
   - **Speed** and **Direction**.

### Presets tab

- Type a name and **Save** (or leave it empty to update the active preset).
- Click a preset to load it. Hover for **rename** / **delete**. **★** makes it the startup preset.

### Paint tab (appears in Paint mode)

- Swatches, a custom color picker and **Eraser**. Click or drag on LEDs to paint.
- **Fill all**, **Clear**, **Show only paint** (switches the main effect to *Static / Paint*).
- **Paint on top of the running effect** — painted LEDs override the effect; unpainted ones keep animating.
  It switches on automatically the first time you paint.

## Setup

Every RGB device OpenRGB detects, one card per device (type badge on the right). Changes apply to the hardware
immediately.

- **+ Zone buttons** — add a zone you want to control. Headers default to a fan ring, RAM and strips to a bar,
  single-LED zones to a dot. Devices without a per-LED (Direct) mode can't be controlled and say so.
- **Zone card**:
  - *Name* — what the device is called everywhere in the app. *Remove* stops controlling the zone.
  - *Shape*: **Fan ring / Bar / strip / Dot**.
  - For fan rings: **Daisy-chain** (each fan its own) or **Splitter / mirrored** (all fans identical).
  - **Fans / Segments** count, and **LEDs per fan**. Zones with a fixed size (e.g. RAM) show "fixed by the
    device" instead.
  - **Not sure? Find the LED count →** — the LED finder: the first LED lights red and the last green. Raise
    **Zone LEDs** until the green LED disappears, step back one, then **Use N**. **Cancel** restores the effect.
- **Per item**: rename, **Identify** (lights only this item: LED 1 red, then amber, green to show direction;
  "Lit ✓" turns it off), **Rotation** (fans: which LED counts as the start) or the **↓ → ↑ ←** arrows (bars), and
  **Reverse** (direction).
- **Not detected right now** — saved zones whose device isn't connected; they resume when it's back.
- **Preview** — drag items to match your case.
- **Chain order** — ↑ ↓ to set how travelling effects flow across items and devices.
- **Welcome banner** (first run) — **Finish setup** hides it.

Test patterns (LED finder, Identify) switch themselves off when you leave Setup, close the page, or after two
minutes.

## Sensors

- **Sources** — what's being read: NVIDIA GPU (temperature, load, power, fan) and Windows CPU load, with no setup.
  The switch **CPU, motherboard & drive temperatures (LibreHardwareMonitor)** adds those after you run
  LibreHardwareMonitor with *Options → Remote Web Server* (port 8085); a status line shows whether it's reachable.
  LibreHardwareMonitor loads its own driver; RGB Studio only reads its web page.
- **Sensor cards**, grouped by part: live value, a one-minute graph, min/max, and "● drives …" when the sensor is
  in use.
- **Show on lights** — pick a **device** (or All devices), then **A few LEDs (layer)** with how many LEDs from the
  start of each item, or **Whole device**; set **Cool** and **Hot** (pre-filled: 35–80 °C for temperatures,
  0–100% for loads). Colors go blue → green → yellow → red and pulse above *Hot*. Fine-tune afterwards in Studio.

## Settings

- **Performance**
  - *Device frame rate cap* (5–60 fps).
  - *Motion smoothing*: blends frames so motion glides. It doesn't apply to music and screen-motion effects.
  - *Browser preview rate*.
  - *LED gamma* (how brightness levels map to the LEDs).
- **Background service** — the service's state (*Running*, *Not responding*, *Stopped*), OpenRGB connection,
  process ID, version and uptime, with:
  - **Start service** — starts it (through its login task when installed) and waits until it's healthy.
  - **Restart** — stop, then start.
  - **Stop** — clean stop: settings are saved and the lights do what *Startup & shutdown* says.
  - **Kill** — force-quit, for a service that stopped responding. The lights freeze on their last frame.
  These buttons are in the desktop app. *Not responding* means the process exists but doesn't answer, or
  hasn't drawn a frame for 2 seconds.
- **Status** — OpenRGB connection, controlled devices and their zones, measured frame rate, render/write time.
- **Audio** — on/off switch (off = nothing listens). Choose **Full desktop** or tick apps that currently play
  sound (they appear automatically; the dot shows which are playing). Level, bass and left/right meters.
  **Light delay** holds the lights back so they match TVs or Bluetooth speakers that play sound late.
- **Screen** — on/off; **Monitor** (detected automatically); **Area**: whole screen or center (skips taskbar and
  black bars); **Samples per second**. A swatch shows the current average screen color.
- **When RGB Studio isn't running** — RGB Studio's effects are drawn live, so they only show while the
  service runs. Each device can also store one of its own built-in modes (Static, Breathing, Rainbow wave…)
  in its memory: that's what shows from power-on until the service starts, and after it stops. Per device:
  pick the mode, its color(s) or *Random colors*, and speed, then **Save to device**. The live effect comes
  back right after. "stored: …" shows what's saved. Any brand works if its OpenRGB driver can save modes to
  the device; devices that can't (some simple controllers, many GPUs) aren't listed.
- **Startup & shutdown** — the preset the service applies when it starts (or restore the last state); when the
  service stops or Windows shuts down: keep the last frame, show a preset, or turn lights off. Closing the app
  doesn't count.
- **Power saving**
  - *When the screen turns off*: **Keep going**, **Dim** (choose how far; it fades), **Show a preset** (a
    calm one, for example), or **Lights off** (also pauses rendering). Your own lighting comes back as soon
    as the screen turns on, and changes made meanwhile go to it.
  - *Lights off when the PC sleeps, shuts down or logs off*. After sleep the service reconnects to
    OpenRGB by itself, so devices that forget their settings in standby are set up again.
- **App & updates** — *Keep in the tray when the window is closed*: the tray icon (next to the clock)
  switches the lights on/off and changes presets; click it to open the window. Closed to the tray, the app
  uses only a few MB. *Start in the tray when you log in*. *Tell me when a new version is out*: a bar at the
  top links to the download page (checked at most every 6 hours; **Check now** checks right away).
- **Report a problem** — **Report a problem on GitHub** copies a diagnostics report (versions, OpenRGB
  connection, every device OpenRGB found, your zones, the end of the service log; your user folder name is
  left out) and opens a new issue: paste it there. **Copy diagnostics** only copies it.
- **Import settings** — paste the path of another RGB Studio data folder (an older version or a backup, the
  folder with `layout.json` and `state.json`) and press **Import** to replace your layout, presets and
  settings with it. The welcome screen offers the same on first run.
- **Palettes** — all palettes; custom ones can be edited or deleted. The editor takes 2–6 colors and a name.

## How-to recipes

**Give one device its own effect** — Studio → select it in Devices → change anything (or **Change** the effect).
It gets an OWN badge. *Follow All* undoes it.

**Show GPU temperature on three LEDs of a fan** — Sensors → GPU Temperature → **Show on lights** → pick the fan's
device → *A few LEDs*, 3 → **Show…**. Or in Studio: select the device → **+ Layer** → Count = 3.

**Dim the RAM only** — Studio → Brightness card → drag **RAM ×2**, or expand it for one stick.

**React only to Spotify** — Settings → Audio → tick Spotify (it appears while it's open), then pick a Music effect.

**Make fans not flash with music** — use any Music effect with **Feel = smooth** (the default).

**Find how many LEDs a fan really has** — Setup → the header's card → *Find the LED count*.

## Troubleshooting

| Symptom | Fix |
| --- | --- |
| "Waiting for OpenRGB" | Start OpenRGB and enable its SDK server (Settings → SDK Server → Start). RGB Studio reconnects on its own. |
| No devices, even in OpenRGB's own window (e.g. Corsair RAM) | RGB Studio only sees what OpenRGB detects. Run OpenRGB **as administrator** (RAM and many boards use SMBus, which needs it), fully quit iCUE / MSI Center / Armoury Crate / SignalRGB (also from the tray), use OpenRGB 1.0 or newer (DDR5 support), then OpenRGB → Settings → **Rescan devices**. |
| A device is missing in Setup | It must be detected by OpenRGB first (rescan in OpenRGB); RGB Studio follows rescans automatically. |
| All fans on a header look identical | They're on a splitter or their pass-through is parallel; set the zone to *Splitter / mirrored*. |
| An LED stays lit after changing counts | Use the LED finder to get the real count; LEDs beyond the configured count aren't driven. |
| Lights run ahead of the music | Raise Settings → Audio → **Light delay**. |
| Flicker or fighting colors | Another RGB app (e.g. a vendor tool) is controlling the same device; close it. |
| *Service: stopped* | Press the ⏻ switch or **Start service** in the Service panel. It also starts by itself at login. |
| *Service: not responding* | Service panel → **Kill**, then **Start service**. Its log is `%APPDATA%\RGB Studio\rgbd.log`. |
| Something else | Settings → Report a problem → **Report a problem on GitHub**, and paste the report into the issue. |
| Music effects only glow dimly | Nothing is playing from the chosen source: check Settings → Audio (Full desktop, or tick the app that's playing). |
| Screen effects only glow dimly | Check Settings → Screen is on and the right monitor is chosen. Protected video (some streaming apps) shows as black to every capture program. |
