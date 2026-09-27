# 📖 Kitab Al-Musiqi-al-Kabīr
## Islamic Golden Age Acoustics System for Minecraft Bedrock

> *"The Grand Book of Music"* — named after Al-Farabi's 10th-century masterpiece on music theory

A physics-based sound system that implements the acoustic principles documented by **10 Islamic Golden Age scientists** (9th–12th century CE). Every parameter is traceable to primary source documentation.

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Minecraft](https://img.shields.io/badge/Minecraft-Bedrock-green.svg)]()
[![Version](https://img.shields.io/badge/version-4.0.0-blue.svg)]()

---

## 📜 Table of Contents

1. [Overview](#-overview)
2. [The 10 Scientists](#-the-10-scientists)
3. [Features](#-features)
4. [Installation](#-installation)
5. [How It Works](#-how-it-works)
6. [Configuration](#-configuration)
7. [Player Commands](#-player-commands)
8. [Architecture](#-architecture)
9. [Testing Protocol](#-testing-protocol)
10. [Troubleshooting](#-troubleshooting)
11. [Performance Tuning](#-performance-tuning)
12. [Primary Sources](#-primary-sources)
13. [License](#-license)
14. [Credits](#-credits)

---

## 🌟 Overview

**Kitab al-Mūsīqī al-Kabīr** transforms Minecraft Bedrock into a real-time acoustic simulation based on 1,000-year-old Islamic scientific manuscripts. Instead of random ambient sounds, this addon creates invisible sound entities that:

- **Bounce** within a spherical field around the player (Al-Kindi's spherical wave theory)
- **Echo** using exact harmonic ratios (Al-Farabi's 3:2, 2:1, 4:3, 5:4, 6:5)
- **Change pitch** based on the surrounding medium (Al-Biruni's density catalog)
- **Respond** to player health with therapeutic sound (Al-Razi's music therapy)
- **Amplify** perception through repetition (Ibn al-Haytham's memory theory)
- **Cycle** through 8 rhythmic patterns (Banu Musa's mechanical devices)
- **Pulse** with compression/rarefaction waves (Ibn Sina's wave theory)
- **Inertia** motion across time (Ibn Bajjah's mayl concept)

### ✨ What's New in v4.0.0

- **Scientific Echo Environment** — real acoustic absorption coefficients (α)
- **Surface-Specific Bounce** — stone vs sand vs wool changes bounce
- **Weather & Time Acoustics** — rain muffles sound, night amplifies echo
- **Early Reflections & Late Reverberation** — full room acoustic simulation
- **Frequency-Dependent Occlusion** — bass penetrates walls, treble blocked
- **Glass Penetration** — transparent blocks don't fully block sound
- **Player Commands** — `!sawt on/off/volume/debug`
- **Multiplayer Handling** — no duplicate entities between nearby players
- **Angular Motion** — entities slowly rotate for lifelike feel
- **Save State** — settings persist using Dynamic Properties

**No custom audio files required.** Uses only vanilla Bedrock sounds.

---

## 🔬 The 10 Scientists

| # | Scientist | Arabic | Years | Primary Work | Contribution |
|---|---|---|---|---|---|
| 1 | **Al-Kindi** | الكندي | 801–873 | *Risala fi l-Musiqi* | 12 pitches, 17m echo, t=d/v formula |
| 2 | **Banu Musa** | بنو موسى | 800–870 | *Kitab al-Hiyal* | 8 mechanical cycles |
| 3 | **Thabit ibn Qurra** | ثابت بن قرة | 826–901 | *Fi l-Musiqi* | Fibonacci ratios, amicable numbers |
| 4 | **Al-Razi** | الرازي | 854–925 | *Al-Hawi fi l-Tibb* | Music therapy, psychological effects |
| 5 | **Al-Farabi** | الفارابي | 872–950 | *Kitab al-Musiqi al-Kabir* | Harmonic ratios, 8 iqa', resonance |
| 6 | **Al-Mahani** | الماهاني | 853–930 | *Fi l-Nisab* | Golden ratio, geometric angles |
| 7 | **Al-Biruni** | البيروني | 973–1048 | *Kitab al-Jamahir* | 13 medium densities |
| 8 | **Ibn Sina** | ابن سينا | 980–1037 | *Kitab al-Shifa* | Compression/rarefaction waves |
| 9 | **Ibn al-Haytham** | ابن الهيثم | 965–1040 | *Kitab al-Manazir* | Perception, acoustic memory |
| 10 | **Ibn Bajjah** | ابن باجة | 1095–1138 | *Fi l-Nafs* | Inertia, mayl (inclination) |

---

## ✨ Features

### 🎵 Acoustics
- **12-pitch system** from Al-Kindi's string experiments (1.000 → 2.000 ratios)
- **7 harmonic echoes** with exact fractions (2:1, 3:2, 4:3, 5:4, 6:5, 5:3, 8:5)
- **8 Arabic iqa' rhythms** (thaqil, ramal, hazaj, mudari, muqtaarab, khafif)
- **5-phase waveform** (compression → neutral → rarefaction) from Ibn Sina
- **Real propagation delay** using `t = d / v` (343 m/s in air)
- **Medium-aware pitch shift** across 13 materials

### 🌐 Spatial Physics
- Invisible entities bounce on a **6-block spherical boundary**
- **Vector reflection** formula: `v' = v - 2(v·n)n` (Al-Farabi)
- **Geometric attenuation**: `I ∝ (1 - d/R)²` (Al-Kindi)
- **Harmonic resonance** between entities with related pitches
- **Inertia & mayl** motion decay (Ibn Bajjah)
- **Surface-specific bounce** (stone vs sand vs wool)
- **Angular motion** — entities rotate slowly

### 🧠 Perception
- **Perception amplification** over time (Ibn al-Haytham)
- **Acoustic memory** per environment type
- **Habituation** to repetitive sounds
- **Familiarity weighting** based on past exposure

### 🌍 Environment-Aware
- **Scientific echo factor** using real α coefficients
- **13 medium densities** (air, water, stone, wood, metal...)
- **Weather acoustics** (clear, rain, thunder)
- **Time-of-day** (dawn, day, dusk, night)
- **Glass penetration** (transparent blocks don't fully block)
- **Frequency occlusion** (bass penetrates walls, treble blocked)
- **Frequency absorption** (α varies by frequency band)

### 🎭 Advanced Audio
- **Early reflections** (first-order, 5–50 ms)
- **Late reverberation** (reverb tail, 0.5–4 seconds)
- **Per-sound volumes** (100+ unique volume values)
- **Multi-bounce recoil** (louder sound = higher jump + more bounces)

### 💚 Adaptive Behavior
- **Real-time mob sound pool** — sounds match nearby mobs
- **HP-based therapy** — Al-Razi's 5 therapeutic states
- **Fallback chain** — mob → block → biome → altitude → ambient

### ⚡ Performance & Control
- **Sound budget** — max 20 sounds/tick globally
- **Wave budget** — max 80 sounds/wave
- **Occlusion cache** — reduce raycast by 90%
- **Silent despawn** — no death/impact sounds
- **Player commands** — `!sawt on/off/volume/debug/info/reset`
- **Multiplayer sharing** — no duplicate entities
- **Save state** — settings persist across sessions

## 📦 Installation

### Requirements

- **Minecraft Bedrock Edition** 1.20.80+
- **Beta APIs** enabled (for `@minecraft/server` 1.11.0)
- **3+ GB RAM** on device (recommended)

### Steps

**1. Download the addon**

Clone or download this repository:

```bash
git clone https://github.com/E4VR/kitab-al-musiqi-al-kabir.git
```

**2. Place in development folders**

| Platform | Path |
|---|---|
| **Windows** | `%localappdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\development_behavior_packs\` |
| **Android** | `/storage/emulated/0/Android/data/com.mojang.minecraftpe/files/games/com.mojang/development_behavior_packs/` |
| **iOS** | `On My iPhone/Minecraft/games/com.mojang/development_behavior_packs/` |

Copy `BP/` into `development_behavior_packs/KitabAlMusiqiAlKabir/` and `RP/` into `development_resource_packs/KitabAlMusiqiAlKabir/`.

**3. Enable in Minecraft**

1. Open Minecraft → **Create New World**
2. **Settings** → **Experiments**
3. Enable **Beta APIs** ✅
4. **Behavior Packs** → Activate **Kitab al-Musiqi al-Kabir**
5. **Resource Packs** → Activate **Kitab al-Musiqi al-Kabir RP**
6. Play!

**4. Verify Installation**

Move around for 10 seconds. You should hear:
- Sounds bouncing from different directions
- Harmonic echoes
- Volume changes when entering caves vs forests

---

## 🎯 How It Works

### The Core Loop

```
Player moves
    ↓
Spawns 10 invisible entities in sphere (radius 6)
    ↓
Each entity gets a random Al-Kindi pitch (12 options)
    ↓
Every 2 ticks: entities move & bounce on sphere boundary
    ↓
Every 1 second: trigger a "sound wave"
    ↓
Wave scans nearby mobs → builds sound pool
    ↓
30 entities play sounds with harmonic echoes
    ↓
Each sound modulated by:
    • Ibn Sina's waveform phase
    • Al-Biruni's medium pitch shift
    • Al-Razi's therapy state
    • Banu Musa's cycle multiplier
    • Ibn al-Haytham's perception
    • Al-Kindi's attenuation
    • Occlusion factor
    • Echo environment factor
    • Weather/time modifiers
    • Frequency-dependent absorption
```

### Example: TNT Explosion in a Cave

1. **Sound pool**: TNT explosion sound (volume 4.5)
2. **Medium**: Stone (density 2600 kg/m³) → pitch +0.08
3. **Occlusion**: Full clear (no walls between) → factor 1.0
4. **Echo environment**: Cave (enclosure 0.95 × reflectivity 0.85) → 0.89
5. **Weather**: Clear → ×1.0
6. **Time**: Day → ×1.0
7. **Wave triggered** with 30 entities

**Each entity plays**:
- Base pitch: 1.333 (perfect 4th)
- Final pitch: 1.413 (with stone medium + Ibn Sina phase)
- Volume: ~4.5 × attenuation × occlusion × echo
- 7 harmonic echoes at exact ratios
- Early reflections from nearby walls
- Late reverberation tail (4 seconds)
- **Recoil**: Entity jumps 5.0 units (max) + bounces 12+ times

**Result**: A deep, resonant TNT boom that echoes through the cave walls with exact musical intervals, while entities fly and bounce like a chain reaction.

---

## ⚙️ Configuration

All settings in `BP/scripts/config.js`:

### Core Settings

```javascript
VERSION: "4.0.0-full",
DEBUG: false,
DEBUG_INTERVAL_TICKS: 60,
DEBUG_VERBOSE: false,
SHOW_WELCOME: false,
```

### Entity

```javascript
ENTITY_ID: "sawt:entity",
MAX_ENTITIES: 100,          // Per player
SPAWN_BATCH_SIZE: 10,
SPAWN_COOLDOWN_TICKS: 5,
MIN_MOVE_DISTANCE: 3,
ENTITY_LIFETIME_TICKS: 600, // 30 seconds
UPDATE_INTERVAL_TICKS: 2,
```

### Sphere (Al-Kindi)

```javascript
SPHERE_RADIUS: 6.0,
SPHERE_INNER_RATIO: 0.85,
MIN_ECHO_DISTANCE: 17.0,
SPEED_OF_SOUND: 343.0,
```

### Occlusion & Diffraction

```javascript
OCCLUSION_ENABLED: true,
OCCLUSION_MIN_VOLUME: 0.15,
DIFFRACTION_ENABLED: true,
DIFFRACTION_OFFSET: 3.0,
OCCLUSION_CACHE_TICKS: 10,
GLASS_PENETRATION_ENABLED: true,
GLASS_VOLUME_REDUCTION: 0.75,
FREQUENCY_OCCLUSION_ENABLED: true,
```

### Echo Environment

```javascript
ECHO_ENVIRONMENT_ENABLED: true,
ECHO_CACHE_TICKS: 20,
ECHO_MIN_FACTOR: 0.05,
FREQUENCY_ABSORPTION_ENABLED: true,
```

### Weather & Time

```javascript
WEATHER_ACOUSTICS_ENABLED: true,
TIME_OF_DAY_ENABLED: true,
ENV_CACHE_TICKS: 100,
```

### Reflections & Reverb

```javascript
EARLY_REFLECTIONS_ENABLED: true,
EARLY_REFLECTIONS_MAX_DISTANCE: 8.0,
EARLY_REFLECTIONS_MAX_COUNT: 6,
EARLY_REFLECTIONS_STRENGTH: 0.15,

LATE_REVERB_ENABLED: true,
LATE_REVERB_DELAY_START_TICKS: 3,
LATE_REVERB_INTERVAL_TICKS: 4,
```

### Recoil

```javascript
RECOIL_BASE_FACTOR: 0.8,
RECOIL_VOLUME_EXPONENT: 1.8,
RECOIL_MAX_IMPULSE: 5.0,
RECOIL_MIN_VOLUME: 0.4,
BOUNCE_INERTIA: 0.78,
RECOIL_MAX_SPEED: 4.0,
```

### Sound

```javascript
SOUND_VOLUME_BASE: 2.0,
SOUND_VOLUME_MAX: 4.0,
SOUND_PITCH_MIN: 0.5,
SOUND_PITCH_MAX: 2.0,
SOUND_BUDGET_PER_TICK: 20,
SOUND_BUDGET_PER_WAVE: 80,
SOUNDS_PER_WAVE: 30,
SOUND_SPECIFIC_VOLUME: true,
```

### Multiplayer & Save

```javascript
MULTIPLAYER_ENABLED: true,
MULTIPLAYER_SHARE_RADIUS: 16.0,
SAVE_STATE_ENABLED: true,
SAVE_AUTO_INTERVAL_TICKS: 6000,
```

### Tuning Examples

| Want | Change |
|---|---|
| More entities | `MAX_ENTITIES: 100 → 200` |
| Bigger sphere | `SPHERE_RADIUS: 6.0 → 10.0` |
| Stronger echo | `ECHO_CACHE_TICKS: 20 → 10` |
| More frequent waves | `FARABI_WAVE_INTERVAL: 20 → 10` |
| Quieter overall | `SOUND_VOLUME_BASE: 2.0 → 1.0` |
| Bass penetrates more | `FREQUENCY_OCCLUSION_ENABLED: false` |

---

## 🎮 Player Commands

Players can control the system using chat commands:

| Command | Effect |
|---|---|
| `!sawt on` | Enable sound system |
| `!sawt off` | Disable sound system |
| `!sawt volume 0.5` | Set volume (0.0 – 2.0) |
| `!sawt debug` | Toggle debug mode |
| `!sawt info` | Show current settings |
| `!sawt reset` | Reset settings to defaults |

**Example**:
```
Player: !sawt volume 0.5
[SAWT] Volume set to 0.50
```

Settings persist across sessions using **Dynamic Properties**.

## 🏗️ Architecture

### Folder Structure

```
KitabAlMusiqiAlKabir/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── BP/
│   ├── manifest.json
│   ├── entities/
│   │   └── sawt_entity.json
│   └── scripts/
│       ├── main.js
│       ├── config.js
│       ├── utils.js
│       ├── sound_volumes.js
│       ├── sound_registry.js
│       ├── context_detector.js
│       │
│       ├── core/
│       │   ├── vector_math.js
│       │   ├── sound_budget.js
│       │   ├── sphere_physics.js
│       │   ├── entity_manager.js
│       │   ├── acoustic_memory.js
│       │   ├── perception_model.js
│       │   ├── debug_logger.js
│       │   ├── occlusion.js
│       │   ├── echo_environment.js
│       │   ├── surface_bounce.js
│       │   ├── weather_acoustics.js
│       │   ├── player_commands.js
│       │   ├── multiplayer.js
│       │   ├── angular_motion.js
│       │   ├── early_reflections.js
│       │   ├── late_reverberation.js
│       │   ├── frequency_occlusion.js
│       │   ├── frequency_absorption.js
│       │   └── save_state.js
│       │
│       └── scientists/
│           ├── al_kindi.js
│           ├── banu_musa.js
│           ├── thabit_ibn_qurra.js
│           ├── al_razi.js
│           ├── al_farabi.js
│           ├── al_mahani.js
│           ├── al_biruni.js
│           ├── ibn_sina.js
│           ├── ibn_al_haytham.js
│           └── ibn_bajjah.js
│
└── RP/
    ├── manifest.json
    ├── entity/
    │   └── sawt_entity.entity.json
    └── sounds/
        └── sound_definitions.json
```

### Statistics

| Category | Count |
|---|---|
| **Total Files** | **39** |
| BP Files | 35 |
| RP Files | 3 |
| Config Files | 1 |
| Core Modules | 19 |
| Scientists | 10 |
| Data Modules | 3 |

---

## 🧪 Testing Protocol

### Phase 1: Base Entity (5 min)

| # | Test | Expected | Status |
|---|---|---|---|
| 1.1 | Spawn entity | Appears invisible | ⬜ |
| 1.2 | Bounce behavior | Moves within 6-block radius | ⬜ |
| 1.3 | Silent despawn | No sound after 30s | ⬜ |
| 1.4 | No crash | Content log clean | ⬜ |

### Phase 2: Real-Time Sound (10 min)

| # | Test | Expected | Status |
|---|---|---|---|
| 2.1 | Near cow | Cow sound plays | ⬜ |
| 2.2 | Near zombie | Zombie sound plays | ⬜ |
| 2.3 | Near TNT | Explosion sound + big jump | ⬜ |
| 2.4 | No mobs | Fallback ambient plays | ⬜ |
| 2.5 | Underwater | Water medium pitch | ⬜ |

### Phase 3: Environmental (15 min)

| # | Test | Expected | Status |
|---|---|---|---|
| 3.1 | Forest | Echo almost none | ⬜ |
| 3.2 | Cave | Full echo | ⬜ |
| 3.3 | Stone house | Moderate echo | ⬜ |
| 3.4 | Wood house | Small echo | ⬜ |
| 3.5 | Rain | Muffled sound | ⬜ |
| 3.6 | Night | Stronger echo | ⬜ |
| 3.7 | Behind glass | Sound passes through | ⬜ |
| 3.8 | Behind stone | Sound blocked | ⬜ |

### Phase 4: Advanced (15 min)

| # | Test | Expected | Status |
|---|---|---|---|
| 4.1 | Surface bounce (stone) | High bounce | ⬜ |
| 4.2 | Surface bounce (sand) | Low bounce | ⬜ |
| 4.3 | Surface bounce (wool) | No bounce | ⬜ |
| 4.4 | Angular motion | Entities rotate slowly | ⬜ |
| 4.5 | Early reflections | Sound feels "close" | ⬜ |
| 4.6 | Late reverb in cave | Long tail | ⬜ |
| 4.7 | Bass penetrates wall | Low freq passes | ⬜ |

### Phase 5: Commands & Multiplayer (10 min)

| # | Test | Expected | Status |
|---|---|---|---|
| 5.1 | `!sawt info` | Shows settings | ⬜ |
| 5.2 | `!sawt off` | Sound stops | ⬜ |
| 5.3 | `!sawt volume 0.5` | Quieter sound | ⬜ |
| 5.4 | `!sawt reset` | Default settings | ⬜ |
| 5.5 | 2 players nearby | No duplicate entities | ⬜ |
| 5.6 | Rejoin world | Settings persist | ⬜ |

### Phase 6: Performance (10 min)

| # | Config | Expected | Status |
|---|---|---|---|
| 6.1 | 50 entities | TPS = 20 | ⬜ |
| 6.2 | 100 entities | TPS = 20 | ⬜ |
| 6.3 | 200 entities | TPS ≥ 18 | ⬜ |
| 6.4 | Phone temperature | Warm, not hot | ⬜ |
| 6.5 | Battery drain | Reasonable | ⬜ |

---

## 🔧 Troubleshooting

### Problem: Entities don't spawn

**Solutions:**
1. Ensure **Beta APIs** is enabled
2. Verify `@minecraft/server` version matches your Minecraft
3. Check that both BP and RP are activated
4. Check content log for JSON errors

### Problem: No sound plays

**Solutions:**
1. Type `!sawt info` — check if enabled
2. Type `!sawt on` — enable system
3. Increase `SOUND_VOLUME_BASE` in config
4. Verify vanilla sound IDs are correct for Bedrock

### Problem: Sound plays but wrong environment

**Solutions:**
1. Reduce `ECHO_CACHE_TICKS` from `40` to `20`
2. Check `echo_environment.js` — verify block detection
3. Verify player isn't in unloaded chunks

### Problem: TPS drops below 18

**Solutions:**
1. Reduce `MAX_ENTITIES` to `50`
2. Increase `UPDATE_INTERVAL_TICKS` from `2` to `3`
3. Increase `OCCLUSION_CACHE_TICKS` from `10` to `20`
4. Disable `EARLY_REFLECTIONS_ENABLED`
5. Disable `LATE_REVERB_ENABLED`

### Problem: Phone overheating

**Solutions:**
1. Reduce `MAX_ENTITIES` to `25`
2. Increase `UPDATE_INTERVAL_TICKS` to `4`
3. Set `SPHERE_RADIUS` to `4.0`
4. Disable `ANGULAR_MOTION_ENABLED`
5. Disable `MULTIPLAYER_ENABLED` (single player)

### Problem: Sound crackles or stutters

**Solutions:**
1. Lower `SOUND_BUDGET_PER_TICK` from `20` to `10`
2. Lower `SOUNDS_PER_WAVE` from `30` to `15`
3. Disable `LATE_REVERB_ENABLED`
4. Disable `EARLY_REFLECTIONS_ENABLED`

### Problem: Entities visible

**Solutions:**
1. Verify BP entity has `"runtime_identifier": "minecraft:arrow"`
2. Verify RP entity doesn't have textures defined
3. Restart Minecraft completely

---

## 📈 Performance Tuning

### Target Metrics

| Device Class | Max Entities | Update Interval | Sphere Radius |
|---|---|---|---|
| **Flagship** (Snapdragon 8 Gen 2+) | 200 | 2 ticks | 8.0 |
| **Upper Mid-range** (Dimensity 8450) | 150 | 2 ticks | 6.0 |
| **Mid-range** (Snapdragon 7-series) | 100 | 2 ticks | 6.0 |
| **Budget** (Snapdragon 6-series) | 50 | 3 ticks | 5.0 |
| **Low-end** (Snapdragon 4-series) | 25 | 4 ticks | 4.0 |

### Budget Formula

```
Total sounds per second =
    (entity_count × sounds_per_wave) / (wave_interval / 20)
```

**Example:**
```
100 entities × 30 sounds per wave = 3000
3000 / (20 ticks / 20) = 3000 sounds per second
```

**Recommended maximum:** 150–200 sounds per second for stable audio.

### Feature Impact

| Feature | CPU Impact | Recommended For |
|---|---|---|
| Occlusion (cached) | Low | All devices |
| Echo Environment (cached) | Low | All devices |
| Weather + Time | Negligible | All devices |
| Surface Bounce | Negligible | All devices |
| Angular Motion | Negligible | All devices |
| Early Reflections | Medium | Mid-range+ |
| Late Reverb | Medium | Mid-range+ |
| Frequency Occlusion | Low | All devices |
| Frequency Absorption | Low | All devices |

### Profiling

Enable debug messages in `config.js`:

```javascript
DEBUG: true,
DEBUG_INTERVAL_TICKS: 60,  // Every 3 seconds
```

Monitor in chat:

```
[Kitab] 87/100 | Peak: 100 | Sounds: 4218 | Drop: 12
Ibn Sina: compression | Iqa': ramal | Banu Musa: al-fath | Medium: stone
```

- **Drop count high?** → Lower `SOUND_BUDGET_PER_TICK`
- **Peak > MAX?** → Reduce `SPAWN_BATCH_SIZE`
- **Sounds too low?** → Increase `SOUNDS_PER_WAVE`

## 📚 Primary Sources

### Al-Kindi
- *Risala fi l-Musiqi* (Epistle on Music)
- *Kitab al-Musiqi* (Book of Music)

### Banu Musa
- *Kitab al-Hiyal* (Book of Ingenious Devices)

### Thabit ibn Qurra
- *Fi l-Musiqi*
- *Kitab fi l-Jabr wa-l-Muqabala*

### Al-Razi
- *Al-Hawi fi l-Tibb* (Comprehensive Book of Medicine)
- *Kitab al-Mansuri*

### Al-Farabi
- *Kitab al-Musiqi al-Kabir* (The Grand Book of Music)
- *Kitab Ihsa' al-'Ulum*

### Al-Mahani
- *Fi l-Nisab* (On Ratios)

### Al-Biruni
- *Kitab al-Jamahir fi Ma'rifat al-Jawahir* (Book of Precious Stones)
- *Kitab al-Qanun al-Mas'udi*

### Ibn Sina
- *Kitab al-Shifa* (Book of Healing)
- *Al-Qanun fi l-Tibb* (The Canon of Medicine)

### Ibn al-Haytham
- *Kitab al-Manazir* (Book of Optics)
- *Maqala fi l-Nur* (Treatise on Light)

### Ibn Bajjah
- *Fi l-Nafs* (On the Soul)
- *Fi l-Haraka* (On Motion)

### Acoustic Data Sources
- Springer Handbook of Acoustics (2020)
- Architectural Acoustics by Marshall Long
- USDA Forest Service (forest absorption data)
- TU Delft Acoustic Repository

---

## 🎓 Academic Notes

### Formulas Implemented

| Formula | Source | Implementation |
|---|---|---|
| `t = d / v` | Al-Kindi | `propagationDelayTicks()` |
| `I ∝ (1 - d/R)²` | Al-Kindi | `alKindiAttenuation()` |
| `v' = v - 2(v·n)n` | Al-Farabi | `reflectVector()` |
| `v = 343 / √(ρ/ρ₀)` | Ibn Sina & Al-Biruni | `speedInMedium()` |
| `φ = (1 + √5) / 2` | Al-Mahani | `GOLDEN_RATIO` |
| `F(n) = F(n-1) + F(n-2)` | Thabit | `fibonacci()` |

### Harmonic Ratios

| Ratio | Name | Fraction | Source |
|---|---|---|---|
| 2.000 | Octave | 2:1 | Al-Farabi |
| 1.500 | Fifth | 3:2 | Al-Farabi |
| 1.333 | Fourth | 4:3 | Al-Farabi |
| 1.250 | Major Third | 5:4 | Al-Farabi |
| 1.200 | Minor Third | 6:5 | Al-Farabi |
| 1.667 | Major Sixth | 5:3 | Al-Farabi |
| 1.600 | Minor Sixth | 8:5 | Al-Farabi |

### 12 Pitches of Al-Kindi

| Ratio | Fraction | Interval |
|---|---|---|
| 1.000 | 1:1 | Tonic |
| 1.067 | 16:15 | Minor 2nd |
| 1.125 | 9:8 | Major 2nd |
| 1.200 | 6:5 | Minor 3rd |
| 1.250 | 5:4 | Major 3rd |
| 1.333 | 4:3 | Perfect 4th |
| 1.406 | 45:32 | Tritone |
| 1.500 | 3:2 | Perfect 5th |
| 1.600 | 8:5 | Minor 6th |
| 1.667 | 5:3 | Major 6th |
| 1.875 | 15:8 | Major 7th |
| 2.000 | 2:1 | Octave |

### 8 Iqa' of Al-Farabi

| Iqa' | Arabic | Meaning | Tempo | BPM |
|---|---|---|---|---|
| Thaqil Awwal | الثقيل الأول | Heavy First | Slow | 60 |
| Thaqil Thani | الثقيل الثاني | Heavy Second | Very Slow | 48 |
| Ramal | الرمل | Sand | Moderate | 80 |
| Hazaj | الهزج | Swaying | Moderate | 80 |
| Mudari | المضارع | Similar | Moderate | 75 |
| Muqtaarab | المقتضب | Concise | Fast | 100 |
| Khafif Awwal | الخفيف الأول | Light First | Fast | 120 |
| Khafif Thani | الخفيف الثاني | Light Second | Very Fast | 144 |

### 13 Medium Densities of Al-Biruni

| Medium | Density (kg/m³) | Speed Multiplier | Pitch Shift |
|---|---|---|---|
| Air | 1.2 | 1.000 | 0.00 |
| Snow | 400 | 0.950 | -0.02 |
| Wood | 700 | 1.100 | +0.04 |
| Ice | 917 | 0.900 | -0.08 |
| Water | 997 | 0.500 | -0.15 |
| Sand | 1600 | 0.850 | -0.05 |
| Gravel | 1700 | 0.880 | +0.02 |
| Clay | 1750 | 0.920 | -0.03 |
| End Stone | 2200 | 0.600 | -0.25 |
| Netherrack | 2500 | 0.700 | -0.20 |
| Stone | 2600 | 1.400 | +0.08 |
| Lava | 3100 | 0.750 | -0.18 |
| Metal | 7800 | 1.800 | +0.12 |

---

## 📜 License

This project is licensed under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License**.

See [LICENSE](LICENSE) file for full details.

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

### What This Means

✅ **You CAN:**
- Use this addon on your world/server
- Modify and improve the code for personal use
- Share with friends
- Make videos and streams
- Use in education

❌ **You CANNOT:**
- Sell this addon as a product
- Put behind a paywall
- Bundle in a paid product
- Use in a paid service
- Claim it as your own work
- Remove the author's name

⚠️ **You MUST:**
- Credit the original author (**E4VR**)
- Share derivative works under the same license
- Link to the CC BY-NC-SA 4.0 license

### Attribution Requirement

If you use, modify, or share this project, you must provide:

- **Author's name**: E4VR
- **Link to this repository**: https://github.com/E4VR/kitab-al-musiqi-al-kabir
- **Link to the license**: https://creativecommons.org/licenses/by-nc-sa/4.0/
- **Indication of changes**: If you modified the work, state what was changed

### Report Violations

If you see this work being sold or used commercially in violation of this license, please report:

1. **GitHub Issues**: Open an issue on this repository
2. **Mojang**: Report violation of Minecraft Usage Guidelines
3. **MCPEDL / Planet Minecraft**: Report to platform admins
4. **Creative Commons**: File a report at https://creativecommons.org/legal/

### Commercial Licensing

For commercial use inquiries, please contact:

**E4VR** — via GitHub Issues on this repository

---

## 🤝 Contributing

Contributions welcome! By submitting a pull request, you agree that:

1. Your contribution will be licensed under **CC BY-NC-SA 4.0**
2. You have the right to submit the contribution
3. You will not claim any ownership over the original work

### Areas of Interest

- **Additional scientists** — Al-Zahrawi, Ibn Rushd, Andalusian scholars
- **More iqa' rhythms** — Extended Arabic rhythmic cycles
- **Multi-language support** — Arabic, Malay, Indonesian, Urdu
- **Performance optimization** — Better caching algorithms
- **New medium types** — Custom block categories

### How to Contribute

1. Fork the repository
2. Create a feature branch
3. Commit changes
4. Push to branch
5. Open a Pull Request

---

## 🗺️ Roadmap

### v4.1 (Next)
- [ ] Add Al-Zahrawi's surgical acoustics
- [ ] Add Ibn Rushd's commentary on motion
- [ ] Multi-language chat messages

### v4.2
- [ ] Custom Resource Pack audio (pre-rendered reverb)
- [ ] Advanced room detection (indoor/outdoor)
- [ ] Weather-based acoustic modulation

### v5.0
- [ ] Full HRTF spatial audio (when Bedrock supports)
- [ ] Real-time DSP (if API becomes available)
- [ ] Multiplayer resonance network

---

## 🙏 Credits

**Original Author**: **E4VR**
**Acoustics Research**: Based on 10 Islamic Golden Age manuscripts (9th–12th century CE)
**Minecraft Integration**: Bedrock Script API 1.11.0
**Inspired by**: Al-Farabi's *Kitab al-Musiqi al-Kabir*

**Special thanks to:**
- The translators who preserved these manuscripts
- The Minecraft Bedrock scripting community
- Beta testers who provided performance data

---

<div align="center">

**﷽**

*"And He it is Who created the heavens and the earth in truth."*
— Qur'an 6:73

**Built with respect for the scientific heritage of the Islamic Golden Age.**

**Original Author: E4VR**

[⬆ Back to Top](#-kitab-al-mūsīqī-al-kabīr)

</div>
