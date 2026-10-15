# Third-party software

RGB Studio uses the following open-source projects. Their licenses apply to those projects; full license texts
ship with each package and are at the linked repositories.

## Service, CLI and desktop app (Rust)

| Crate | License |
| --- | --- |
| [Tauri](https://github.com/tauri-apps/tauri) | MIT or Apache-2.0 |
| [axum](https://github.com/tokio-rs/axum) | MIT |
| [Tokio](https://github.com/tokio-rs/tokio) | MIT |
| [Serde](https://github.com/serde-rs/serde) / [serde_json](https://github.com/serde-rs/json) | MIT or Apache-2.0 |
| [log](https://github.com/rust-lang/log) | MIT or Apache-2.0 |
| [windows-sys](https://github.com/microsoft/windows-rs) | MIT or Apache-2.0 |

The OpenRGB connection in the service is RGB Studio's own implementation of OpenRGB's documented SDK
protocol; no OpenRGB code is included. OpenRGB (GPL-2.0) runs as a separate program.

## Web UI

| Package | License |
| --- | --- |
| [React](https://github.com/facebook/react) | MIT |
| [Vite](https://github.com/vitejs/vite) | MIT |
| [Tailwind CSS](https://github.com/tailwindlabs/tailwindcss) | MIT |
| [TypeScript](https://github.com/microsoft/TypeScript) | Apache-2.0 |
| [@tauri-apps/api](https://github.com/tauri-apps/tauri) | MIT or Apache-2.0 |

## External programs (not bundled)

- [OpenRGB](https://openrgb.org) — GPL-2.0, required; RGB Studio talks to its SDK server.
- [LibreHardwareMonitor](https://github.com/LibreHardwareMonitor/LibreHardwareMonitor) — MPL-2.0, optional,
  for CPU/motherboard temperatures.

## Inspiration & references

Several effects are original implementations of well-known community effects (no code was copied); each one is
credited in [docs/EFFECTS.md](docs/EFFECTS.md):

- [WLED effects list](https://kno.wled.ge/features/effects/) and [WLED source](https://github.com/wled/WLED) — Bouncing Balls, Popcorn, Ripple,
  Fireworks, Meteor, Matrix, Lighthouse, Dancing Shadows, Galaxy, Washing Machine, Candle, Strobe, Dissolve,
  Railway, Sunrise, Breathe, Heartbeat, Aurora, Plasma, sound-reactive GEQ/Puddlepeak, and more.
- [FastLED examples](https://github.com/FastLED/FastLED/blob/master/examples/) — [Pacifica](https://github.com/FastLED/FastLED/blob/master/examples/Pacifica/Pacifica.ino), [TwinkleFox](https://github.com/FastLED/FastLED/blob/master/examples/TwinkleFox/TwinkleFox.ino),
  [Pride2015](https://github.com/FastLED/FastLED/blob/master/examples/Pride2015/Pride2015.ino), [DemoReel100](https://github.com/FastLED/FastLED/blob/master/examples/DemoReel100/DemoReel100.ino) (juggle, sinelon,
  glitter), [Fire2012](https://github.com/FastLED/FastLED/blob/master/examples/Fire2012/Fire2012.ino).
- [OpenRGB Effects Plugin](https://openrgb.org/plugin_effects.html) — the standard effect set (rainbow wave,
  breathing, visor, audio visualizers) used as a baseline.
