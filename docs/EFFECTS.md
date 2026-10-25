# Effects reference

RGB Studio has **41 effects**. Pick one in Studio → Effects → **Change**; its settings appear
underneath. The settings,
ranges and defaults below are exactly what the UI shows.

Terms: an **item** is one fan ring, bar or dot on the canvas; the **chain** is the order items are linked
in (Setup → Chain order), so *along the chain* means flowing from item to item across devices;
**spatial** effects use where items sit on the canvas.

Effects marked *Inspired by* are original implementations of well-known community effects from
[WLED](https://kno.wled.ge/features/effects/) and the [FastLED examples](https://github.com/FastLED/FastLED/tree/master/examples); no code
was copied. Effects without that line (Relay, Neon chase, Storm, Auto DJ, Stereo field, ...) are RGB Studio's own.

## Contents

- **Music ♪** — [Auto DJ](#auto-dj), [Stereo field](#stereo-field), [Beat pulse](#beat-pulse), [Bass relay](#bass-relay), [Puddles](#puddles), [Spectrum](#spectrum), [Mood drift](#mood-drift), [Sparkle hits](#sparkle-hits)
- **Screen ▣** — [Screen ambience](#screen), [Screen motion](#screen-motion)
- **Sensors** — [Sensor reactive](#temperature)
- **Game** — [Rev lights 🏎](#rev-lights)
- **Premium ✦** — [Relay](#relay), [Spin & orbit](#spin), [Silk tides](#silk), [Aurora](#aurora), [Pacifica](#pacifica), [Plasma](#plasma), [Neon chase](#chase), [Fire](#fire), [Ripples & fireworks](#ripple), [Spotlights](#spotlights), [Sweep & lighthouse](#sweep), [Warp galaxy](#warp), [Bouncing balls](#bouncing-balls), [Meteor shower & matrix](#meteor-shower), [Storm](#storm)
- **Classics** — [Static / Paint](#static), [Solid color](#solid), [Breathing / heartbeat](#breathing), [Color flow](#rainbow), [Strobe / flash](#strobe), [Candle](#candle), [Stack / fill / wipe](#stack), [Wave](#wave), [Comet / scanner](#comet), [Dissolve](#dissolve), [Twinkle / fairy lights](#twinkle), [Railway](#railway), [Sunrise / sunset](#sunrise)
- **Custom** — [Custom effect](#recipe)

## Music ♪

React to what your PC is playing (Settings → Audio chooses the source). Every music effect has **Feel**: *smooth* eases everything in and out (no flashing), *punchy* uses the raw, instant analysis.

<a id="auto-dj"></a>
### Auto DJ

Reacts to whatever is playing: kicks radiate from the centre, hi-hats sparkle, panned sounds move across the case, colors follow the tone, quiet parts breathe and the palette changes with the song.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `vaporwave` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Change palette with the music | on/off | `on` |  |
| Sparkle | 0–1.5 | `0.6` |  |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |
_No settings._

<a id="stereo-field"></a>
### Stereo field

Bass, mids and highs glow where they sit in the stereo image: a sound moving left to right moves across the case.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `vaporwave` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Spot width | 0.1–1 | `0.35` |  |
| Stereo axis | choice: `horizontal` / `vertical` | `horizontal` |  |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |
_No settings._

<a id="beat-pulse"></a>
### Beat pulse

Every fan flashes on the kick and fades between beats; each beat steps to the next color.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `vaporwave` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |
| Ripple through fans | 0–0.3 | `0.0` |  |
_No settings._

<a id="bass-relay"></a>
### Bass relay

Each kick launches a comet. In stereo mode it starts on the side the sound comes from and crosses the case.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `sunset` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Comets start | choice: `stereo` / `chain` | `stereo` |  |
| Tail | 0.05–1 | `0.3` |  |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |
_No settings._

<a id="puddles"></a>
### Puddles

Every kick drops a pool of color somewhere on the case that spreads and fades; louder kicks make bigger pools.

*Inspired by:* [WLED Puddlepeak](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `aurora` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Pool size | 0.08–0.6 | `0.25` |  |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |
_No settings._

<a id="spectrum"></a>
### Spectrum

Level meters: each ring fills with its frequency band (clockwise or mirrored from the bottom), the spectrum spreads across the chain, or glow makes fans take turns following bass, mids, treble and volume.

*Inspired by:* [WLED sound-reactive GEQ / Gravimeter](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `toxic` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Mode | choice: `rings` / `mirror` / `chain` / `glow` | `rings` |  |
| Peak dots | on/off | `on` |  |
| Spin with music (glow) | on/off | `on` |  |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |
_No settings._

<a id="mood-drift"></a>
### Mood drift

Colors flow faster and glow brighter as the music gets more intense; calm tracks stay calm.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `ocean` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Calm brightness | 0.05–1 | `0.35` |  |
_No settings._

<a id="sparkle-hits"></a>
### Sparkle hits

Hi-hats and snares fire sparkles; beats burst across every fan.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Base color | color | `#06060f` |  |
| Density | 0.1–4 | `1.0` |  |
_No settings._

## Screen ▣

Take colors from your monitor (Settings → Screen chooses the monitor and area).

<a id="screen"></a>
### Screen ambience

Fans take their colors from your screen: each LED from the matching spot, per fan, or the whole-screen mood.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Sampling | choice: `position` / `per-fan` / `whole` | `position` |  |
| Saturation boost | 0.5–3 | `1.4` |  |
| Brightness boost | 0.3–3 | `1.3` |  |
| Ignore dark below | 0–0.4 | `0.06` |  |
| Sample area | 0.02–0.5 | `0.12` |  |
_No settings._

<a id="screen-motion"></a>
### Screen motion

Lights up where the picture moves, in the moving thing's colors: a car passing on screen streaks across the fans. Still scenes fall back to a dim ambient glow.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Sensitivity | 1–15 | `5.0` | how strongly the music drives the lights |
| Trail (s) | 0.05–2 | `0.35` |  |
| Ambient glow | 0–0.6 | `0.1` |  |
| Saturation boost | 0.5–3 | `1.5` |  |
_No settings._

## Sensors

Driven by a temperature or load reading (see the Sensors page).

<a id="temperature"></a>
### Sensor reactive

Color or fill driven by a CPU/GPU/board sensor. Put it on a whole fan or just an LED range.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Sensor | sensor | `nvidia:0:temp` |  |
| Low (cool) | 0–120 | `35.0` |  |
| High (hot) | 0–120 | `80.0` |  |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `custom` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `ember` | the palette used when Colors = palette |
| Custom colors | color list | `#00a2ff, #00ff88, #ffd000, #ff2200` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Display | choice: `color` / `gauge` / `gauge-ring` | `color` |  |
| Pulse when hot | on/off | `on` |  |
| Smoothing | 0–0.99 | `0.85` |  |
_No settings._

## Game

Driven by a racing game's live telemetry: Forza Horizon 5 / 6 and Forza Motorsport "Data Out" (in the game: Settings > HUD and Gameplay > Data Out On, IP 127.0.0.1, port 5600; RGB Studio listens only while a Game effect is on).

<a id="rev-lights"></a>
### Rev lights 🏎

Forza Horizon / Motorsport: the fans fill with engine RPM like a dash's shift lights, green to red along the chain, blink at the shift point and flash on every gear change. Throttle & brake shows the pedals instead. Turn on Data Out in the game (127.0.0.1, port 5600); in menus a soft glow shows.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `custom` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `rgb` | the palette used when Colors = palette |
| Custom colors | color list | `#00ff40, #ffd000, #ff1020` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Show | choice: `rpm` / `throttle & brake` | `rpm` |  |
| Fill | choice: `chain` / `each fan` | `chain` |  |
| Shift light at | 0.5–1 | `0.9` |  |
| Flash on gear change | on/off | `on` |  |
| When not driving | choice: `glow` / `off` | `glow` |  |
_No settings._

## Premium ✦

Richer, mostly spatial effects that use where items sit on the canvas.

<a id="relay"></a>
### Relay

A glowing comet laps each fan, then hands off to the next fan down the chain.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `vaporwave` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Laps per fan | 0.5–4 | `1.0` |  |
| Tail | 0.1–1 | `0.6` |  |
| Afterglow | 0–0.5 | `0.12` |  |
_No settings._

<a id="spin"></a>
### Spin & orbit

Arcs, orbs or soft spiral arms turning inside every fan. Gears makes neighbouring fans counter-rotate; twist offsets each fan so the motion flows through the chain; washing machine spins up, slows down and reverses.

*Inspired by:* [WLED Washing Machine](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Shape | choice: `arc` / `orb` / `spiral` | `arc` |  |
| Motion | choice: `steady` / `washing machine` | `steady` |  |
| Arms | 1–4 | `1` |  |
| Size | 0.05–1 | `0.45` |  |
| Fan twist | 0–1 | `0.0` |  |
| Counter-rotate neighbours | on/off | `off` |  |
| Background glow | 0–0.6 | `0.04` |  |
_No settings._

<a id="silk"></a>
### Silk tides

Satin-smooth color tides rolling through the chain, with a soft sheen where the light peaks.

*Inspired by:* [FastLED Pride2015](https://github.com/FastLED/FastLED/blob/master/examples/Pride2015/Pride2015.ino)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `silk` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Sheen | 0–1 | `0.35` |  |
_No settings._

<a id="aurora"></a>
### Aurora

Slow, organic curtains of color drifting across the whole case.

*Inspired by:* [WLED Aurora](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `aurora` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `0.6` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Detail | 0.3–5 | `1.6` |  |
| Contrast | 0.5–4 | `1.6` |  |
_No settings._

<a id="pacifica"></a>
### Pacifica

Layered ocean swells rolling across the case, with whitecaps where waves meet.

*Inspired by:* [FastLED Pacifica](https://github.com/FastLED/FastLED/blob/master/examples/Pacifica/Pacifica.ino)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `ocean` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `0.6` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Whitecaps | 0–1 | `0.6` |  |
_No settings._

<a id="plasma"></a>
### Plasma

Interfering sine fields across the case — liquid, lava-lamp motion.

*Inspired by:* [WLED Plasma](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `royal` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Scale | 0.5–10 | `3.0` |  |
_No settings._

<a id="chase"></a>
### Neon chase

Soft-edged neon segments marching through every fan as one continuous strip.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `vaporwave` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Segment (LEDs) | 1–16 | `4.0` |  |
| Gap (LEDs) | 0–16 | `4.0` |  |
| Softness | 0–1 | `0.5` |  |
_No settings._

<a id="fire"></a>
### Fire

Flickering flames that rise inside each ring (from the ring's bottom to its top). Flame: classic embers, blue spirit, or any palette (cool to hot along the palette).

*Inspired by:* [FastLED Fire2012](https://github.com/FastLED/FastLED/blob/master/examples/Fire2012/Fire2012.ino)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Flame | choice: `ember` / `spirit` / `palette` | `ember` |  |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `lava` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Flame height | 0.2–1.2 | `0.7` |  |
| Flicker | 0–2 | `1.0` |  |
_No settings._

<a id="ripple"></a>
### Ripples & fireworks

Rings of light spread from random points across the case: gentle water drops, or fireworks that flash and then burst into color over neighbouring fans.

*Inspired by:* [WLED Ripple / Fireworks](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `ocean` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Style | choice: `water` / `fireworks` | `water` |  |
| Bursts / s | 0.1–4 | `0.8` |  |
| Ring width | 0.02–0.3 | `0.08` |  |
| Base glow | 0–0.3 | `0.04` |  |
_No settings._

<a id="spotlights"></a>
### Spotlights

Soft colored spotlights drift across the case like a stage light show.

*Inspired by:* [WLED Dancing Shadows](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `royal` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Spots | 1–6 | `3` |  |
| Spot size | 0.08–0.6 | `0.25` |  |
| Ambient | 0–0.3 | `0.04` |  |
_No settings._

<a id="sweep"></a>
### Sweep & lighthouse

A band of light or a flowing gradient crossing the whole case, or twin lighthouse beams rotating around its middle. Uses fan positions on the canvas.

*Inspired by:* [WLED Lighthouse / Sweep](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `aurora` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Mode | choice: `band` / `gradient` / `lighthouse` | `band` |  |
| Angle (°) | 0–360 | `0.0` |  |
| Width | 0.05–1 | `0.3` |  |
| Background glow | 0–1 | `0.0` | minimum glow so lights never go fully dark |
_No settings._

<a id="warp"></a>
### Warp galaxy

Stars stream outward from the centre of the case like jumping to hyperspace.

*Inspired by:* [WLED Galaxy](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Stars | 6–60 | `24` |  |
_No settings._

<a id="bouncing-balls"></a>
### Bouncing balls

Balls bounce under gravity inside every fan, losing height until kicked again; popcorn style pops kernels up from the bottom that fall back down.

*Inspired by:* [WLED Bouncing Balls / Popcorn](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `toxic` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Style | choice: `balls` / `popcorn` | `balls` |  |
| Balls per fan | 1–4 | `2` |  |
| Pops / s (popcorn) | 0.2–6 | `1.5` |  |
_No settings._

<a id="meteor-shower"></a>
### Meteor shower & matrix

Streaks falling across the whole case: meteors at any angle, or Matrix-style digital rain pouring down in columns with bright heads.

*Inspired by:* [WLED Meteor / Matrix](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Style | choice: `meteors` / `matrix` | `meteors` |  |
| Angle (meteors) | 0–360 | `60.0` |  |
| Meteors / s | 0.1–6 | `1.2` |  |
| Tail length | 0.05–1 | `0.35` |  |
| Width (meteors) | 0.02–0.3 | `0.08` |  |
| Columns (matrix) | 3–24 | `10` |  |
_No settings._

<a id="storm"></a>
### Storm

Brooding clouds with lightning that forks through a few fans at a time.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Cloud color | color | `#1a1f5c` |  |
| Lightning | color | `#d8e6ff` |  |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Strikes / 10 s | 0–20 | `3.0` |  |
_No settings._

## Classics

The everyday staples found in most RGB software.

<a id="static"></a>
### Static / Paint

Per-LED colors painted on the case canvas.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Unpainted LEDs | color | `#000000` |  |
_No settings._

<a id="solid"></a>
### Solid color

Steady color: one color everywhere, or a different color per fan from your colors or a palette.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `custom` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `sunset` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #05d9e8, #7b5cff` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Fill | choice: `per fan` / `all fans` | `per fan` |  |
_No settings._

<a id="breathing"></a>
### Breathing / heartbeat

Slow fade in and out that steps to the next color each breath, or a lub-dub heartbeat. Fan delay makes the pulse travel from fan to fan.

*Inspired by:* [WLED Breathe / Heartbeat](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `sakura` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Rhythm | choice: `breathe` / `heartbeat` | `breathe` |  |
| Resting glow | 0–0.8 | `0.0` | minimum glow so lights never go fully dark |
| Fan delay | 0–1 | `0.0` |  |
_No settings._

<a id="rainbow"></a>
### Color flow

Colors flowing along the chain, around each ring, across the case, or the whole case cycling together (color cycle). Speed 0 gives a still gradient; glitter adds white glints.

*Inspired by:* [FastLED DemoReel100 (rainbow with glitter)](https://github.com/FastLED/FastLED/blob/master/examples/DemoReel100/DemoReel100.ino), [WLED Colorloop](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `rainbow` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `vaporwave` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Flow | choice: `chain` / `ring` / `spatial` / `together` | `chain` |  |
| Repeats | 0.1–6 | `1.0` |  |
| Fan offset | 0–1 | `0.1` |  |
| Glitter | 0–4 | `0.0` |  |
_No settings._

<a id="strobe"></a>
### Strobe / flash

Sharp flashes: all fans together, alternating fans, or a random fan each flash.

*Inspired by:* [WLED Strobe](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `mono` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Flash length | 0.03–0.9 | `0.15` |  |
| Flash | choice: `all` / `alternate` / `random fan` | `all` |  |
_No settings._

<a id="candle"></a>
### Candle

Warm flame flicker, per LED or per fan.

*Inspired by:* [WLED Candle](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Flame | color | `#ff8a1f` |  |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Flicker | 0–1 | `0.5` |  |
| Flicker | choice: `per-led` / `per-fan` | `per-led` |  |
_No settings._

<a id="stack"></a>
### Stack / fill / wipe

Fills LED by LED, holds, then drains; drop stacks falling LEDs; wipe paints each palette color over the last. Along the whole chain or inside every fan.

*Inspired by:* [WLED Wipe / Tetrix](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `aurora` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Style | choice: `fill` / `drop` / `wipe` | `fill` |  |
| Scope | choice: `chain` / `fan` | `chain` |  |
| Drain from | choice: `end` / `start` | `end` |  |
| Hold (s) | 0–5 | `0.8` |  |
_No settings._

<a id="wave"></a>
### Wave

Brightness waves travelling along the chain.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `ocean` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Wavelength (LEDs) | 2–64 | `12.0` |  |
| Sharpness | 0.5–8 | `2.0` |  |
| Floor | 0–1 | `0.05` | minimum glow so lights never go fully dark |
| Scope | choice: `chain` / `fan` | `chain` |  |
_No settings._

<a id="comet"></a>
### Comet / scanner

Bright heads with fading tails. Loop runs them round the chain or each fan; bounce is a Larson scanner sweeping back and forth; juggle weaves several heads at different speeds.

*Inspired by:* [FastLED DemoReel100 (juggle, sinelon)](https://github.com/FastLED/FastLED/blob/master/examples/DemoReel100/DemoReel100.ino), [WLED Meteor / Scanner](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `custom` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#7df9ff` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Background | color | `#000000` |  |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Motion | choice: `loop` / `bounce` / `juggle` | `loop` |  |
| Tail (LEDs) | 1–40 | `8.0` |  |
| Heads | 1–8 | `1` |  |
| Scope | choice: `chain` / `fan` | `chain` |  |
| Ease at ends | on/off | `on` |  |
| Rainbow tail | on/off | `off` |  |
_No settings._

<a id="dissolve"></a>
### Dissolve

LEDs switch to the next color one at a time in random order until the whole case has changed.

*Inspired by:* [WLED Dissolve](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `sakura` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Fade (s) | 0–1.5 | `0.25` |  |
_No settings._

<a id="twinkle"></a>
### Twinkle / fairy lights

Random LEDs flash and fade over a dim background (sparkle), or each LED glows in and out on its own slow rhythm like fairy lights (gentle).

*Inspired by:* [FastLED TwinkleFox](https://github.com/FastLED/FastLED/blob/master/examples/TwinkleFox/TwinkleFox.ino), [WLED Twinkle / Sparkle](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Background | color | `#05060f` |  |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Style | choice: `sparkle` / `gentle` | `sparkle` |  |
| Density | 0.02–3 | `0.5` |  |
| Fade (sparkle) | 0.3–10 | `2.5` |  |
_No settings._

<a id="railway"></a>
### Railway

Neighbouring LEDs cross-fade between two colors, like a railway crossing.

*Inspired by:* [WLED Railway](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `lava` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
_No settings._

<a id="sunrise"></a>
### Sunrise / sunset

A slow sunrise (or sunset) from night through red and orange to warm daylight; lower fans brighten first.

*Inspired by:* [WLED Sunrise](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Duration (min) | 0.5–60 | `5.0` |  |
| Sunset instead | on/off | `off` |  |
_No settings._

## Custom

Your own effects, made of layers of building blocks. Make one with Studio → ✨ AI → *A new effect* (any chat AI designs it from a prompt RGB Studio writes); saved ones are under Change → Custom. A recipe is data, not code: RGB Studio checks every value before using it.

<a id="recipe"></a>
### Custom effect

An effect built from layers (wave, chase, sparkle…), made with ✨ AI or shared as a recipe.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `aurora` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | picks a new random set when Colors = random (older settings; 🎲 Shuffle new colors now makes custom colors) |
| Color cycle | 0–1 | `0.0` | the colors travel through the palette while the effect keeps its motion (1 = once every 10 s) |
| Palette playlist | list of palettes | `` | Palette playlist: 2 or more palettes take turns on the lights, crossfading |
| Next palette every (min) | 0.5–30 | `3.0` | minutes each palette of the playlist plays |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |

**Building blocks** (one per layer, up to 6 layers drawn bottom to top):

| Block | What it does |
| --- | --- |
| `solid` | every LED lit; with palette colors, *fan offset* gives each fan its own color and *color drift* cycles them |
| `gradient` | palette colors spread along the axis; *speed* moves them |
| `wave` | soft bright bands moving along the axis (*scale* = number of bands, *width* = band size) |
| `pulse` | the axis breathes in and out; *fan offset* makes fans pulse one after another |
| `chase` | *count* heads with fading tails (*width* = tail length); around each fan by default |
| `sparkle` | random LEDs flash and fade (*count* = how many, *width* = how long they last) |
| `noise` | organic drifting blobs (*scale* = blob size, *width* = how much is lit) |
| `fill` | the axis fills up and starts over, like a loading bar |

**Layer settings** (all optional):

| Setting | Values |
| --- | --- |
| `along` | chain / fan / x / y / center: through all fans in order, around each fan, left to right, top to bottom, out from the middle |
| `color` | `palette` (the effect's Colors) or a fixed `#RRGGBB` |
| `color_drift` | -2–2: palette colors shift over time |
| `speed` | -5–5 cycles per second (negative = the other way), times the effect's Speed slider |
| `scale` | 0.1–8: repeats along the axis |
| `width` | 0.02–1: size of the lit part |
| `count` | 1–16: chase heads / sparkle amount |
| `fan_offset` | -1–1: each next fan runs this much of a cycle later |
| `phase` | -1–1: where in its cycle the layer starts (two layers 0.5 apart take turns) |
| `blend` | over / add / max / multiply (multiply darkens what's below: a moving mask) |
| `opacity` | 0–1 |
| `react` | none / level / bass / mid / treble / beat: music drives the layer's brightness |
| `floor` | 0–1: brightness kept while the music is quiet |

## Built-in palettes (84)

Colors are tuned for LEDs (pale colors read as white on fans), and no two palettes look alike
(checked by a test). The name in parentheses is what presets and the ✨ AI use.


### One color

| Palette | Colors |
| --- | --- |
| Amber (`amber`) | `#ffb000` `#ff7800` `#ffe040` `#a06000` |
| Blue (`blue`) | `#0018ff` `#0068ff` `#00b0ff` `#0828a0` |
| Frost (`frost`) | `#bff0ff` `#30c0ff` `#0068ff` `#7a78ff` |
| Green (`green`) | `#00ff40` `#00a030` `#80ff50` `#005c1a` |
| Lemon (`lemon`) | `#ffe600` `#fff6a8` `#8a7a00` |
| Lime (`lime`) | `#b8ff00` `#6aff00` `#e0ff70` `#4a7a00` |
| Mint (`mint`) | `#30ffb0` `#00c87a` `#a0ffd8` |
| White (`mono`) | `#ffffff` `#6a6a6a` |
| Pink (`pink`) | `#ff0a80` `#ff5cb0` `#b8005a` `#ff8ac8` |
| Purple (`purple`) | `#5a00ff` `#9a3cff` `#c88aff` `#34009a` |
| Red (`red`) | `#ff0000` `#c0001a` `#ff4848` `#700008` |
| Rose gold (`rosegold`) | `#ff5a60` `#ff9070` `#ffc0a0` `#d04870` |
| Sakura (`sakura`) | `#ffb0d0` `#ff3a80` `#ffe4ee` `#e0609a` |
| Teal (`teal`) | `#00ffd0` `#00a898` `#30fff0` `#006a68` |
| Warm white (`warmwhite`) | `#ffd49a` `#ff9a40` `#fff0d8` |

### Two colors

| Palette | Colors |
| --- | --- |
| Blue & white (`bluewhite`) | `#0040ff` `#ffffff` |
| Cobalt & lime (`cobalt`) | `#0040a0` `#00e040` `#0080ff` `#a0ff00` |
| Green & gold (`greengold`) | `#00c040` `#ffb800` |
| Green & purple (`greenpurple`) | `#20ff30` `#9000ff` |
| Green & white (`greenwhite`) | `#00ff40` `#ffffff` |
| Gunmetal & red (`gunmetal`) | `#3a3a40` `#ff2020` `#8a8a90` `#1a1a20` |
| Navy & brass (`navygold`) | `#0a1a4a` `#ffc040` `#1a3a8a` `#ffe0a0` |
| Orange & white (`orangewhite`) | `#ff6400` `#ffffff` |
| Pink & blue (`pinkblue`) | `#ff1a8c` `#1a40ff` |
| Police (`police`) | `#ff0020` `#0030ff` |
| Purple & cyan (`purplecyan`) | `#8000ff` `#00e5ff` |
| Red & gold (`redgold`) | `#ff0018` `#ffb800` |
| Red & white (`redwhite`) | `#ff0010` `#ffffff` |
| Royal (`royal`) | `#4800e0` `#8a30ff` `#ffb000` `#ffd860` |
| White & gold (`whitegold`) | `#ffffff` `#ffc800` |

### Warm

| Palette | Colors |
| --- | --- |
| Autumn (`autumn`) | `#ff6a00` `#c81400` `#ffc000` `#5a8a00` |
| Canyon (`canyon`) | `#c05020` `#e8a060` `#4a2010` `#8a3010` |
| Cherry (`cherry`) | `#bf0030` `#ffe9cd` `#ff475e` |
| Desert Dusk (`desert`) | `#f0d8b0` `#eea860` `#8a5428` `#404858` |
| Diner (`diner`) | `#ffe547` `#ff4747` `#ffffff` |
| Ember (`ember`) | `#ff3c00` `#5a0800` `#ff8a10` `#200000` |
| Lava (`lava`) | `#700000` `#ff1000` `#ff7000` `#fff0a0` |
| Mango (`mango`) | `#ff6a1c` `#ffd447` `#ff4763` |
| Mocha (`mocha`) | `#ff8a3c` `#a04a1e` `#ffc890` `#ff5a2a` |
| Mustard (`mustard`) | `#d0a020` `#8a5a10` `#f0d060` `#5a3a00` |
| Sunset (`sunset`) | `#ff2020` `#ff6a1a` `#ffb020` `#a0102a` |

### Nature

| Palette | Colors |
| --- | --- |
| Beach (`beach`) | `#00c8ff` `#2dffb8` `#ffe066` `#ff5e7e` |
| Citrus (`citrus`) | `#b8ff00` `#ffe600` `#ff8c00` |
| Forest (`forest`) | `#0b5d1e` `#2fbf4a` `#a8e63c` `#ffd23f` |
| Jade (`jade`) | `#0a8a5a` `#60e0a0` `#c8f0d8` `#064a34` |
| Lavender Fields (`lavender`) | `#b8a0f0` `#8060c0` `#f0e8ff` `#402060` |
| Moss (`moss`) | `#4a7a20` `#a8ff50` `#d8ffa0` `#203010` |
| Orchard (`orchard`) | `#ff9f47` `#fff247` `#9aff47` |
| Orchid (`orchid`) | `#d060c0` `#ffb0e0` `#8020a0` `#401050` |
| Reef (`reef`) | `#00bfad` `#47ffb5` `#ffc700` `#fff347` |
| Spring (`spring`) | `#00ff9c` `#70ff47` `#fdff47` `#ffe700` |
| Sunflower (`sunflower`) | `#ffbf00` `#fff247` `#5cbf36` |
| Tropical (`tropical`) | `#ff6a00` `#ffd000` `#30ff60` `#ff2e4e` |
| Watermelon (`watermelon`) | `#76bf36` `#89ff47` `#d4ff47` `#ff4747` |

### Cool

| Palette | Colors |
| --- | --- |
| Abyss (`abyss`) | `#000c8a` `#0040ff` `#00897b` `#00e5c0` |
| Aurora (`aurora`) | `#00ff87` `#00d4b4` `#3f5efb` `#a24bff` |
| Galaxy (`galaxy`) | `#1a00b0` `#9000ff` `#ff00c8` `#4060ff` |
| Lagoon (`lagoon`) | `#00c0b0` `#0060a0` `#80ffe0` `#002040` |
| Nord (`nord`) | `#1fa0c8` `#3a5cff` `#8fe0f0` `#d04a5a` |
| Ocean (`ocean`) | `#0033ff` `#0091ff` `#00e0ff` `#00ffb3` |
| Slate Storm (`slate`) | `#5a6a7a` `#a0b4c8` `#1a2430` `#c8d8e8` |
| Tide (`tide`) | `#00a0c0` `#004060` `#60e0f0` `#c0f8ff` |
| Tokyo night (`tokyo`) | `#3d6bff` `#9b5cff` `#ff3d6e` `#20b0ff` |

### Neon

| Palette | Colors |
| --- | --- |
| Arcade (`arcade`) | `#46d8ff` `#d3ff47` `#ff8a0c` `#ff4747` |
| Cyberpunk (`cyberpunk`) | `#fcee0a` `#00f0ff` `#ff003c` |
| Dracula (`dracula`) | `#8a3cff` `#ff2fa6` `#20ff6a` `#5a10d0` |
| Miami (`miami`) | `#ff2fa6` `#00e6d2` `#ff7ac8` `#00a8c8` |
| Outrun (`outrun`) | `#ff2975` `#ff8c1a` `#ffd319` `#8c1eff` |
| Party (`party`) | `#7400ff` `#ff007a` `#ff8a00` `#ffe600` `#00c2ff` |
| RGB (`rgb`) | `#ff0000` `#00ff00` `#0000ff` |
| Toxic (`toxic`) | `#39ff14` `#e6ff00` `#00ffb0` `#9d00ff` |
| Vaporwave (`vaporwave`) | `#ff4fd8` `#01cdfe` `#05ffa1` `#b967ff` |

### Themed

| Palette | Colors |
| --- | --- |
| Candy (`candy`) | `#ffe100` `#ff2ec4` `#ff7a6b` `#7aff5a` |
| Christmas (`christmas`) | `#ff0018` `#00c83c` `#ffd700` `#ffffff` |
| Cinematic (`cinematic`) | `#ff7b00` `#00b8a9` `#ffc078` `#005f73` |
| Copper patina (`copper`) | `#b85c38` `#2f8a7a` `#e0a070` `#144a44` |
| Fiesta (`fiesta`) | `#1dffa5` `#ffd147` `#ff9d23` `#ff3928` |
| Halloween (`halloween`) | `#ff6a00` `#8a00ff` `#39ff14` |
| Ice & fire (`icefire`) | `#0040ff` `#00d5ff` `#ffffff` `#ff6a00` `#ff1a00` |
| Pastel (`pastel`) | `#ff8a9a` `#ffc48a` `#7affc0` `#80b0ff` `#c890ff` |
| Rasta (`rasta`) | `#ff0010` `#ffe000` `#00a020` `#7a0008` |
| Jewels (`silk`) | `#d4006a` `#ffa000` `#00a860` `#7a00d4` |
| Summer (`summer`) | `#ff9847` `#fff5c1` `#22f3ff` `#47ff7e` |
| Void (`void`) | `#05050a` `#2a0a4a` `#7a20c0` `#0a2a6a` |

Make your own: Colors → **+ New palette** or **🎲 Shuffle new colors**, then **Save palette**;
or in Settings → Palettes (2–6 colors).
