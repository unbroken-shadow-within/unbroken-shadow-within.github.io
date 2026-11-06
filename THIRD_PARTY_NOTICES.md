# Third-party notices

UNBROKEN · Shadow Within is © 2026 usw-gametech, all rights reserved (see `LICENSE`).
These parts were made by others and stay under their own licences. The same
list is shown in the game (title menu → "เครดิต / ลิขสิทธิ์", `scripts/ui/legal.gd`);
keep the two in step.

| Part | Author | Licence | Where |
|---|---|---|---|
| Godot Engine 4.7 | Juan Linietsky, Ariel Manzur and contributors | MIT (full text: in game, `Engine.get_license_text()`) | the engine (`index.wasm`, `index.js`) |
| Godot third-party components | various (FreeType, HarfBuzz, ...) | various (in game: `Engine.get_copyright_info()`) | the engine |
| netfox, netfox.internals | Gálffy Tamás | MIT (`addons/netfox/LICENSE`) | `addons/netfox*` |
| Godot Jev (community client for TypeSafe AI's Jev API; not affiliated with TypeSafe) | AlvianEka | MIT (`addons/godot_jev/LICENSE`) | `addons/godot_jev` |
| Aura Autopilot Godot addon (a playtesting tool for the editor and local runs; not in the game's builds) | RamenVR (Aura) | Apache-2.0 (github.com/ramenvr/autopilot); its bundled fonts SIL OFL 1.1 (`addons/autopilot/fonts/`) | `addons/autopilot` |
| godot-agent-harness (dev tools: `tools/shot.sh`, `tools/godot/capture.gd`, the import check in `tools/test.sh`; not in the game's builds) | caiizilaz | MIT (`docs/engine-reference/LICENSE-godot-agent-harness`) | `tools/` |
| Godot engine reference notes (4.4 to 4.7 API changes, for the coding agents; not in the game's builds) | Donchitos (Claude-Code-Game-Studios) | MIT (`docs/engine-reference/LICENSE-claude-code-game-studios`) | `docs/engine-reference/` |
| Effekseer for Godot 4 (the effects runtime) | Effekseer Project | MIT (`addons/effekseer/LICENSE`) | `addons/effekseer/` (Windows and web builds) |
| Effekseer sample effects: Light (tktk), PowerUp (NextSoft) | their authors, shipped with Effekseer 1.80.6 | free to use and remodel in games made with Effekseer (the Effekseer readme) | `assets/vfx/effekseer/` |
| pixelfx (the pixel effects, baked to sprite sheets by `tools/import_pixelfx.py`) | Patch (patch.gg); parts adapted from Hugo Duprez (Sprite Fusion) and Hollow Crown (rehan-remade) | MIT, © 2026 each | `assets/sprites/pixelfx/` |
| webrtc-native and its libraries | Godot Engine and others | see `addons/webrtc_native/LICENSE.*` | desktop builds only (not in the web build) |
| Noto Sans Thai, Noto Sans Symbols | The Noto Project Authors | SIL Open Font License 1.1 (`assets/fonts/OFL.txt`) | `assets/fonts/` |
| Press Start 2P (the arcade menus' pixel font; the web loading page loads it from Google Fonts) | The Press Start 2P Project Authors (CodeMan38) | SIL Open Font License 1.1 (`assets/fonts/PressStart2P-OFL.txt`) | `assets/fonts/PressStart2P-Regular.ttf` |
| Music: the jingles (2) | MintoDog | CC0 1.0 (`assets/audio/music/CREDITS.md`) | `assets/audio/music/` |
| Music: the main track (`stage.ogg`) | alex-morgan (Pixabay) | Pixabay Content License (`assets/audio/music/CREDITS.md`) | `assets/audio/music/` |
| Music: the boss fight (`boss.ogg`) | u_98a917e4i7 (Pixabay) | Pixabay Content License (`assets/audio/music/CREDITS.md`) | `assets/audio/music/` |
| Recorded sound effects (5: the jump grunt, the death scream, the dragon's roar, fire and death) | Pixabay uploaders | Pixabay Content License (`art_src/sfx/CREDITS.md`) | cut into `assets/audio/sfx/` |
| Sound effects (29: blades, hits, parries, dashes, landings, the dragon's growl / wings / slam, the bell, items, UI; `tools/make_sfx_set.py` `ONIKURA`) from the Onikura demo | Onikura's makers (Kazan Games) | used with the makers' permission (`art_src/sfx/CREDITS.md`) | cut into `assets/audio/sfx/` |
| Sound effects (24: the laser gunner's guns; the Thai warlock's talismans, levitation and summoning, and her spirit tiger; the menus' `ui_*` sounds; the spring pads; `tools/make_sfx_set.py` `BLADE_ASSAULT`) from Blade Assault | Team Suneat | **permission not yet confirmed**: get it before any public release (`art_src/sfx/CREDITS.md`) | cut into `assets/audio/sfx/` |
| Menu music "NeonCity_Planetboom" from Blade Assault | Team Suneat | **permission not yet confirmed**: get it before any public release (`assets/audio/music/CREDITS.md`) | `assets/audio/music/menu.ogg` |
| The fighters' voices (the Muay Thai fighter's 8 short shouts, `muay_*`; the fighters' ultimate cries, win lines and fighter-select lines, `*_ultimate` / `*_victory` / `*_select`; Twin Core's villagers' yelps, `npc_*_scared`) | generated with ElevenLabs text to speech (voices "Jessica", "Harry", "Adam", and the Voice Library's "Ake" and "Hammy", eleven_v3) on the project owner's account | ElevenLabs terms for generated audio (`art_src/sfx/CREDITS.md`) | cut into `assets/audio/sfx/` by `tools/make_muay_voice.py` |

The MIT licence of Godot Engine:

```
Copyright (c) 2014-present Godot Engine contributors.
Copyright (c) 2007-2014 Juan Linietsky, Ariel Manzur.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

The netfox licence is the same MIT text with the line
`Copyright 2023 Gálffy Tamás`; the Effekseer licence with `Copyright (c) 2020 Effekseer`.
