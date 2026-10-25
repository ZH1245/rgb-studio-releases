# Racing games: Forza rev lights

RGB Studio can turn your fans into a race car's dash lights. It reads the live telemetry Forza sends
with its own **Data Out** feature: engine revs, gear, throttle and brake. No mods, nothing injected into
the game, nothing an anti-cheat looks at: the game simply sends a small data packet to your PC every frame
while you drive.

## Supported games

| Game | Works | Notes |
| --- | --- | --- |
| Forza Horizon 6 | yes | Official Data Out format (324 bytes) |
| Forza Horizon 5 | yes | Same layout as Horizon 6 |
| Forza Motorsport (2023) | yes | "Car Dash" format |
| Forza Horizon 4 / Motorsport 7 | should work | Same Data Out family; not tested |

## Set up Data Out (once)

1. Start the game and open **Settings → HUD and Gameplay**.
2. Scroll to the bottom and set:
   - **Data Out:** On
   - **Data Out IP Address:** `127.0.0.1` (this PC)
   - **Data Out IP Port:** `5600`
3. Leave the menu. The game only sends while you are actually driving (not in menus, pause, replays or
   after the finish line).

Use a port outside **5200–5300**: Forza binds its own socket in that range. If 5600 is taken on your PC,
pick another (for example 5700) in the game **and** in RGB Studio under **Settings → Performance → Game data
port**.

## Put it on the lights

**Quickest:** in Studio, click one of the presets:

- **Forza Rev Lights**: every fan and the RAM fill with the engine revs.
- **Forza Dash**: your first fan header shows the revs, the other fans and the RAM show throttle (from one
  end) and brake (from the other).

**Your own split:** pick the effect per device. In Studio, select a device in the Devices list (for example
*Top and rear*), **Change effect → Game → Rev lights**, and set **Show** to *throttle & brake*. Select
another device (for example *Right side*) and give it Rev lights with **Show: RPM**. Each header can show
something different.

## What the lights do

| Setting | What it does |
| --- | --- |
| **Show: RPM** | Fans fill with the engine revs, from idle (start of the chain) to redline (end) |
| **Show: throttle & brake** | Throttle fills in the first color from the start, brake in the last color from the end |
| **Fill: chain / each fan** | Fill across all the fans in chain order, or around every fan at once |
| **Shift light at** | Above this share of the rev range (default 90%) the whole case blinks: time to shift |
| **Flash on gear change** | Every gear change (each paddle pull) flashes the fans white for a moment |
| **When not driving** | A soft glow in menus and pauses, or off |

**Colors:** the Colors tab offers dash looks with one tap: *Classic* (green, yellow, red), *F1* (green to
red, blinks blue to shift), *Heat*, *Ice*, *Neon* and *Horizon*. Or set your own: the first color is the
start of the rev range, the last is the redline and the shift blink.

## Check that it works

Open **Settings → Performance**. The **Game data port** row tells you what is happening:

- *Listening starts when a Game effect is on*: put Rev lights (or a Forza preset) on the lights.
- *Listening on port 5600: waiting for the game*: RGB Studio is ready, the game isn't sending yet. Drive.
- *Receiving: gear 3, 5400 rpm*: it works.

## Troubleshooting

- **Stays on "waiting for the game" while driving:** check the three Data Out settings in the game, and
  that the port matches RGB Studio's. Restart the race after changing them.
- **Steam version:** some players report Data Out sending nothing on the Steam version of a Forza game. If
  the settings are right and nothing arrives, this may be it (it's on the game's side; RGB Studio can't
  receive what isn't sent).
- **Another app uses the port** (a telemetry dashboard, SimHub): Settings → Performance shows "can't
  listen on port …". Give RGB Studio another port, or point the game at the other app and use a forwarder.
- **The lights react a little late:** that's the device update rate (Settings → Performance → Device updates
  per second, default 30). 30 updates a second is about 33 ms, quicker than you can notice; raise it if you
  like, lower it if your fans glitch.

RGB Studio only listens while a Game effect is on the lights, and only on this PC (127.0.0.1). Nothing is
sent anywhere.
