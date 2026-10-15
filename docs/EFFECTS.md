# Effects reference

RGB Studio has **39 effects**. Pick one in Studio → Effects → **Change**; its settings appear
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
- **Premium ✦** — [Relay](#relay), [Spin & orbit](#spin), [Silk tides](#silk), [Aurora](#aurora), [Pacifica](#pacifica), [Plasma](#plasma), [Neon chase](#chase), [Fire](#fire), [Ripples & fireworks](#ripple), [Spotlights](#spotlights), [Sweep & lighthouse](#sweep), [Warp galaxy](#warp), [Bouncing balls](#bouncing-balls), [Meteor shower & matrix](#meteor-shower), [Storm](#storm)
- **Classics** — [Static / Paint](#static), [Solid color](#solid), [Breathing / heartbeat](#breathing), [Color flow](#rainbow), [Strobe / flash](#strobe), [Candle](#candle), [Stack / fill / wipe](#stack), [Wave](#wave), [Comet / scanner](#comet), [Dissolve](#dissolve), [Twinkle / fairy lights](#twinkle), [Railway](#railway), [Sunrise / sunset](#sunrise)

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
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Change palette with the music | on/off | `on` |  |
| Sparkle | 0–1.5 | `0.6` |  |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |

<a id="stereo-field"></a>
### Stereo field

Bass, mids and highs glow where they sit in the stereo image: a sound moving left to right moves across the case.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `vaporwave` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Spot width | 0.1–1 | `0.35` |  |
| Stereo axis | choice: `horizontal` / `vertical` | `horizontal` |  |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |

<a id="beat-pulse"></a>
### Beat pulse

Every fan flashes on the kick and fades between beats; each beat steps to the next color.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `vaporwave` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |
| Ripple through fans | 0–0.3 | `0.0` |  |

<a id="bass-relay"></a>
### Bass relay

Each kick launches a comet. In stereo mode it starts on the side the sound comes from and crosses the case.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `sunset` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Comets start | choice: `stereo` / `chain` | `stereo` |  |
| Tail | 0.05–1 | `0.3` |  |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |

<a id="puddles"></a>
### Puddles

Every kick drops a pool of color somewhere on the case that spreads and fades; louder kicks make bigger pools.

*Inspired by:* [WLED Puddlepeak](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `aurora` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Pool size | 0.08–0.6 | `0.25` |  |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |

<a id="spectrum"></a>
### Spectrum

Level meters: each ring fills with its frequency band (clockwise or mirrored from the bottom), the spectrum spreads across the chain, or glow makes fans take turns following bass, mids, treble and volume.

*Inspired by:* [WLED sound-reactive GEQ / Gravimeter](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `toxic` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Mode | choice: `rings` / `mirror` / `chain` / `glow` | `rings` |  |
| Peak dots | on/off | `on` |  |
| Spin with music (glow) | on/off | `on` |  |
| Idle glow | 0–0.5 | `0.06` | minimum glow so lights never go fully dark |

<a id="mood-drift"></a>
### Mood drift

Colors flow faster and glow brighter as the music gets more intense; calm tracks stay calm.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `ocean` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Calm brightness | 0.05–1 | `0.35` |  |

<a id="sparkle-hits"></a>
### Sparkle hits

Hi-hats and snares fire sparkles; beats burst across every fan.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Sensitivity | 0.2–3 | `1.0` | how strongly the music drives the lights |
| Feel | choice: `smooth` / `punchy` | `smooth` | *smooth* (no flashing, default) or *punchy* (sharp, instant) |
| Base color | color | `#06060f` |  |
| Density | 0.1–4 | `1.0` |  |

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

<a id="screen-motion"></a>
### Screen motion

Lights up where the picture moves, in the moving thing's colors: a car passing on screen streaks across the fans. Still scenes fall back to a dim ambient glow.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Sensitivity | 1–15 | `5.0` | how strongly the music drives the lights |
| Trail (s) | 0.05–2 | `0.35` |  |
| Ambient glow | 0–0.6 | `0.1` |  |
| Saturation boost | 0.5–3 | `1.5` |  |

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
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Display | choice: `color` / `gauge` / `gauge-ring` | `color` |  |
| Pulse when hot | on/off | `on` |  |
| Smoothing | 0–0.99 | `0.85` |  |

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
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Laps per fan | 0.5–4 | `1.0` |  |
| Tail | 0.1–1 | `0.6` |  |
| Afterglow | 0–0.5 | `0.12` |  |

<a id="spin"></a>
### Spin & orbit

Arcs, orbs or soft spiral arms turning inside every fan. Gears makes neighbouring fans counter-rotate; twist offsets each fan so the motion flows through the chain; washing machine spins up, slows down and reverses.

*Inspired by:* [WLED Washing Machine](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Shape | choice: `arc` / `orb` / `spiral` | `arc` |  |
| Motion | choice: `steady` / `washing machine` | `steady` |  |
| Arms | 1–4 | `1` |  |
| Size | 0.05–1 | `0.45` |  |
| Fan twist | 0–1 | `0.0` |  |
| Counter-rotate neighbours | on/off | `off` |  |
| Background glow | 0–0.6 | `0.04` |  |

<a id="silk"></a>
### Silk tides

Satin-smooth color tides rolling through the chain, with a soft sheen where the light peaks.

*Inspired by:* [FastLED Pride2015](https://github.com/FastLED/FastLED/blob/master/examples/Pride2015/Pride2015.ino)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `silk` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Sheen | 0–1 | `0.35` |  |

<a id="aurora"></a>
### Aurora

Slow, organic curtains of color drifting across the whole case.

*Inspired by:* [WLED Aurora](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `aurora` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `0.6` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Detail | 0.3–5 | `1.6` |  |
| Contrast | 0.5–4 | `1.6` |  |

<a id="pacifica"></a>
### Pacifica

Layered ocean swells rolling across the case, with whitecaps where waves meet.

*Inspired by:* [FastLED Pacifica](https://github.com/FastLED/FastLED/blob/master/examples/Pacifica/Pacifica.ino)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `ocean` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `0.6` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Whitecaps | 0–1 | `0.6` |  |

<a id="plasma"></a>
### Plasma

Interfering sine fields across the case — liquid, lava-lamp motion.

*Inspired by:* [WLED Plasma](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `royal` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Scale | 0.5–10 | `3.0` |  |

<a id="chase"></a>
### Neon chase

Soft-edged neon segments marching through every fan as one continuous strip.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `vaporwave` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Segment (LEDs) | 1–16 | `4.0` |  |
| Gap (LEDs) | 0–16 | `4.0` |  |
| Softness | 0–1 | `0.5` |  |

<a id="fire"></a>
### Fire

Flickering flames that rise inside each ring (from the ring's bottom to its top).

*Inspired by:* [FastLED Fire2012](https://github.com/FastLED/FastLED/blob/master/examples/Fire2012/Fire2012.ino)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Flame | choice: `ember` / `spirit` | `ember` |  |
| Flame height | 0.2–1.2 | `0.7` |  |
| Flicker | 0–2 | `1.0` |  |

<a id="ripple"></a>
### Ripples & fireworks

Rings of light spread from random points across the case: gentle water drops, or fireworks that flash and then burst into color over neighbouring fans.

*Inspired by:* [WLED Ripple / Fireworks](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `ocean` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Style | choice: `water` / `fireworks` | `water` |  |
| Bursts / s | 0.1–4 | `0.8` |  |
| Ring width | 0.02–0.3 | `0.08` |  |
| Base glow | 0–0.3 | `0.04` |  |

<a id="spotlights"></a>
### Spotlights

Soft colored spotlights drift across the case like a stage light show.

*Inspired by:* [WLED Dancing Shadows](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `royal` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Spots | 1–6 | `3` |  |
| Spot size | 0.08–0.6 | `0.25` |  |
| Ambient | 0–0.3 | `0.04` |  |

<a id="sweep"></a>
### Sweep & lighthouse

A band of light or a flowing gradient crossing the whole case, or twin lighthouse beams rotating around its middle. Uses fan positions on the canvas.

*Inspired by:* [WLED Lighthouse / Sweep](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `aurora` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Mode | choice: `band` / `gradient` / `lighthouse` | `band` |  |
| Angle (°) | 0–360 | `0.0` |  |
| Width | 0.05–1 | `0.3` |  |
| Background glow | 0–1 | `0.0` | minimum glow so lights never go fully dark |

<a id="warp"></a>
### Warp galaxy

Stars stream outward from the centre of the case like jumping to hyperspace.

*Inspired by:* [WLED Galaxy](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Stars | 6–60 | `24` |  |

<a id="bouncing-balls"></a>
### Bouncing balls

Balls bounce under gravity inside every fan, losing height until kicked again; popcorn style pops kernels up from the bottom that fall back down.

*Inspired by:* [WLED Bouncing Balls / Popcorn](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `toxic` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Style | choice: `balls` / `popcorn` | `balls` |  |
| Balls per fan | 1–4 | `2` |  |
| Pops / s (popcorn) | 0.2–6 | `1.5` |  |

<a id="meteor-shower"></a>
### Meteor shower & matrix

Streaks falling across the whole case: meteors at any angle, or Matrix-style digital rain pouring down in columns with bright heads.

*Inspired by:* [WLED Meteor / Matrix](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Style | choice: `meteors` / `matrix` | `meteors` |  |
| Angle (meteors) | 0–360 | `60.0` |  |
| Meteors / s | 0.1–6 | `1.2` |  |
| Tail length | 0.05–1 | `0.35` |  |
| Width (meteors) | 0.02–0.3 | `0.08` |  |
| Columns (matrix) | 3–24 | `10` |  |

<a id="storm"></a>
### Storm

Brooding clouds with lightning that forks through a few fans at a time.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Cloud color | color | `#1a1f5c` |  |
| Lightning | color | `#d8e6ff` |  |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Strikes / 10 s | 0–20 | `3.0` |  |

## Classics

The everyday staples found in most RGB software.

<a id="static"></a>
### Static / Paint

Per-LED colors painted on the case canvas.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Unpainted LEDs | color | `#000000` |  |

<a id="solid"></a>
### Solid color

Steady color: one color everywhere, or a different color per fan from your colors or a palette.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `custom` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `sunset` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #05d9e8, #7b5cff` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Fill | choice: `per fan` / `all fans` | `per fan` |  |

<a id="breathing"></a>
### Breathing / heartbeat

Slow fade in and out that steps to the next color each breath, or a lub-dub heartbeat. Fan delay makes the pulse travel from fan to fan.

*Inspired by:* [WLED Breathe / Heartbeat](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `sakura` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Rhythm | choice: `breathe` / `heartbeat` | `breathe` |  |
| Resting glow | 0–0.8 | `0.0` | minimum glow so lights never go fully dark |
| Fan delay | 0–1 | `0.0` |  |

<a id="rainbow"></a>
### Color flow

Colors flowing along the chain, around each ring, across the case, or the whole case cycling together (color cycle). Speed 0 gives a still gradient; glitter adds white glints.

*Inspired by:* [FastLED DemoReel100 (rainbow with glitter)](https://github.com/FastLED/FastLED/blob/master/examples/DemoReel100/DemoReel100.ino), [WLED Colorloop](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `rainbow` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `vaporwave` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Flow | choice: `chain` / `ring` / `spatial` / `together` | `chain` |  |
| Repeats | 0.1–6 | `1.0` |  |
| Fan offset | 0–1 | `0.1` |  |
| Glitter | 0–4 | `0.0` |  |

<a id="strobe"></a>
### Strobe / flash

Sharp flashes: all fans together, alternating fans, or a random fan each flash.

*Inspired by:* [WLED Strobe](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `mono` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Flash length | 0.03–0.9 | `0.15` |  |
| Flash | choice: `all` / `alternate` / `random fan` | `all` |  |

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

<a id="stack"></a>
### Stack / fill / wipe

Fills LED by LED, holds, then drains; drop stacks falling LEDs; wipe paints each palette color over the last. Along the whole chain or inside every fan.

*Inspired by:* [WLED Wipe / Tetrix](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `aurora` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Style | choice: `fill` / `drop` / `wipe` | `fill` |  |
| Scope | choice: `chain` / `fan` | `chain` |  |
| Drain from | choice: `end` / `start` | `end` |  |
| Hold (s) | 0–5 | `0.8` |  |

<a id="wave"></a>
### Wave

Brightness waves travelling along the chain.

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `ocean` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Wavelength (LEDs) | 2–64 | `12.0` |  |
| Sharpness | 0.5–8 | `2.0` |  |
| Floor | 0–1 | `0.05` | minimum glow so lights never go fully dark |
| Scope | choice: `chain` / `fan` | `chain` |  |

<a id="comet"></a>
### Comet / scanner

Bright heads with fading tails. Loop runs them round the chain or each fan; bounce is a Larson scanner sweeping back and forth; juggle weaves several heads at different speeds.

*Inspired by:* [FastLED DemoReel100 (juggle, sinelon)](https://github.com/FastLED/FastLED/blob/master/examples/DemoReel100/DemoReel100.ino), [WLED Meteor / Scanner](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `custom` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#7df9ff` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Background | color | `#000000` |  |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Direction | choice: `forward` / `reverse` | `forward` | which way the motion runs along the chain or around each fan |
| Motion | choice: `loop` / `bounce` / `juggle` | `loop` |  |
| Tail (LEDs) | 1–40 | `8.0` |  |
| Heads | 1–8 | `1` |  |
| Scope | choice: `chain` / `fan` | `chain` |  |
| Ease at ends | on/off | `on` |  |
| Rainbow tail | on/off | `off` |  |

<a id="dissolve"></a>
### Dissolve

LEDs switch to the next color one at a time in random order until the whole case has changed.

*Inspired by:* [WLED Dissolve](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `sakura` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Fade (s) | 0–1.5 | `0.25` |  |

<a id="twinkle"></a>
### Twinkle / fairy lights

Random LEDs flash and fade over a dim background (sparkle), or each LED glows in and out on its own slow rhythm like fairy lights (gentle).

*Inspired by:* [FastLED TwinkleFox](https://github.com/FastLED/FastLED/blob/master/examples/TwinkleFox/TwinkleFox.ino), [WLED Twinkle / Sparkle](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `frost` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Background | color | `#05060f` |  |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |
| Style | choice: `sparkle` / `gentle` | `sparkle` |  |
| Density | 0.02–3 | `0.5` |  |
| Fade (sparkle) | 0.3–10 | `2.5` |  |

<a id="railway"></a>
### Railway

Neighbouring LEDs cross-fade between two colors, like a railway crossing.

*Inspired by:* [WLED Railway](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Colors | choice: `rainbow` / `palette` / `custom` / `random` | `palette` | where colors come from: *rainbow*, a named *palette*, your own *custom* colors, or *random* |
| Palette | palette | `ember` | the palette used when Colors = palette |
| Custom colors | color list | `#ff2a6d, #ffb800, #05d9e8` | your colors when Colors = custom (1–8) |
| Shuffle | 0–99999 | `7` | the 🎲 Shuffle button: picks a new random set when Colors = random |
| Speed | 0–5 | `1.0` | animation speed for this effect (multiplied by the global speed in the top bar) |

<a id="sunrise"></a>
### Sunrise / sunset

A slow sunrise (or sunset) from night through red and orange to warm daylight; lower fans brighten first.

*Inspired by:* [WLED Sunrise](https://kno.wled.ge/features/effects/)

| Setting | Values | Default | Notes |
| --- | --- | --- | --- |
| Duration (min) | 0.5–60 | `5.0` |  |
| Sunset instead | on/off | `off` |  |

## Built-in palettes

| Name | Colors |
| --- | --- |
| aurora | `#00ff87` `#00d4b4` `#3f5efb` `#a24bff` |
| ember | `#ff1a00` `#ff5a00` `#ffa000` `#b30000` |
| frost | `#d8f6ff` `#7fdcff` `#3a9bff` `#8f8cff` |
| mono | `#ffffff` `#5c6cff` |
| ocean | `#0033ff` `#0091ff` `#00e0ff` `#00ffb3` |
| royal | `#5b1fff` `#9a48ff` `#ff3df2` `#ffc400` |
| sakura | `#ff9ec4` `#ff4f8b` `#ffd6e6` `#ff6fa8` |
| silk | `#ff2d95` `#8a2be2` `#00d5ff` `#ffb347` |
| sunset | `#ff2e63` `#ff7a3d` `#ffc94a` `#b83bd6` |
| toxic | `#39ff14` `#b0ff00` `#00ff6a` `#e0ff00` |
| vaporwave | `#ff4fd8` `#01cdfe` `#05ffa1` `#b967ff` |

Make your own in Settings → Palettes (2–6 colors).
