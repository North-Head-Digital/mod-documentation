# Artillery & Mortars

This section covers indirect fire weapons including flamethrowers, mortars, and rocket artillery systems.

## Flamethrowers

All flamethrower weapons receive ~25% range increases. These weapons excel at bunker clearing and close-quarters combat.

### Infantry Flamethrowers

| Weapon                  | Nation  | Vanilla Range | FCRO Range | Change | Notes                  |
| ----------------------- | ------- | ------------- | ---------- | ------ | ---------------------- |
| Flammenwerfer 35        | German  | 25-27         | 32-35      | +28%   | Early war, short range |
| Flammenwerfer 41        | German  | 30-32         | 38-40      | +27%   | Improved design        |
| M1 Flamethrower         | USA     | 20-21         | 26-27      | +30%   | Early war, very short  |
| M1A1 Flamethrower       | USA     | 40-41         | 50-52      | +25%   | Standard issue         |
| M2 Flamethrower         | USA     | 40-41         | 50-52      | +25%   | Improved M1A1          |
| ROKS-2                  | Soviet  | 40-41         | 50-52      | +25%   | Disguised as backpack  |
| ROKS-3                  | Soviet  | 40-41         | 50-52      | +25%   | Improved ROKS-2        |
| Flamethrower No.2 Mk.II | British | 34-36         | 43-46      | +26%   | Lifebuoy type          |

### Vehicle Flamethrowers

| Weapon              | Vehicle/Nation        | Vanilla Range | FCRO Range | Change | Notes                   |
| ------------------- | --------------------- | ------------- | ---------- | ------ | ----------------------- |
| ATO-41              | OT-34 (Soviet)        | 60            | 75         | +25%   | Early tank flamethrower |
| ATO-42              | OT-34/85 (Soviet)     | 80            | 100        | +25%   | Improved pressurized    |
| Churchill Crocodile | British               | 80            | 100        | +25%   | Devastating trailer-fed |
| Wasp Carrier        | British               | 70            | 88         | +26%   | Universal Carrier mount |
| E4-5                | German Sd.Kfz. 251/16 | 54-55         | 68-70      | +26%   | Half-track mount        |
| Flammenwerfer B2    | Flammpanzer III       | 45            | 57         | +27%   | Panzer III conversion   |
| KS-24               | Soviet                | 35-40         | 44-50      | +26%   | Early tank mount        |
| KS-25               | Soviet/Finnish        | 45            | 57         | +27%   | Standard tank mount     |
| 14mm Flammenwerfer  | SdKfz 251/16 (German) | 60            | 75         | +25%   | Twin mount              |
| 14mm Flammenwerfer  | Flammpanzer III       | 60            | 75         | +25%   | Tank mount              |

**Flamethrower Notes:**
- Range values shown as min-max where applicable
- Vehicle flamethrowers have much larger fuel tanks (20+ shots vs 6-10)
- Crocodile can fire indefinitely while connected to trailer
- All flamethrowers cause morale damage and suppression

---

## Mortars

### Base Patterns: `mortar/.presets`

All mortar classes receive range increases while maintaining realistic accuracy degradation at range.

### Light Mortars (50mm class)

| Stat        | Vanilla | FCRO | Change | Notes               |
| ----------- | ------- | ---- | ------ | ------------------- |
| Max Range   | 140     | 175  | +25%   | ~1400m IRL          |
| Min Range   | 30      | 30   | ------ | Arming distance     |
| Reload Time | ------- | 2.7s | ------ | Fast rate of fire   |
| HE Damage   | ------- | 10   | ------ | Light fragmentation |

**Accuracy (radiusTable):**
| Distance | Spread (meters) | Notes                 |
| -------- | --------------- | --------------------- |
| 0m       | 4m              | Minimum dispersion    |
| 120m     | 14m             | Standard engagement   |
| 175m     | 20m             | Max range             |
| 175m+    | 100m            | Beyond max (unusable) |

**Applies to:**
- 50mm RM-40 (Soviet)
- 50mm Granatwerfer 36 (German)
- 2-inch Mortar (British)

### Medium Mortars (81-82mm class)

| Stat            | Vanilla | FCRO | Change | Notes                |
| --------------- | ------- | ---- | ------ | -------------------- |
| Max Range       | 160     | 200  | +25%   | ~1600m IRL           |
| Min Range       | 40      | 40   | ------ | Arming distance      |
| Reload Time     | ------- | 5.0s | ------ | Standard rate        |
| Smoke/WP Reload | ------- | 3.3s | ------ | Faster for smoke     |
| HE Damage       | ------- | 15   | ------ | Medium fragmentation |

**Accuracy (radiusTable):**
| Distance | Spread (meters) | Notes                 |
| -------- | --------------- | --------------------- |
| 0m       | 4m              | Minimum dispersion    |
| 120m     | 18m             | Standard engagement   |
| 200m     | 35m             | Max range             |
| 200m+    | 100m            | Beyond max (unusable) |

**Applies to:**
- 82mm BM-37 (Soviet)
- 81mm Granatwerfer 34 (German)
- 81mm M1 Mortar (USA)
- 3-inch Mortar (British)
- 81mm Kranaatinheitin m/38 (Finnish)

### Medium-Heavy Mortars (107mm class)

| Stat            | Vanilla | FCRO | Change | Notes               |
| --------------- | ------- | ---- | ------ | ------------------- |
| Max Range       | 180     | 225  | +25%   | ~1800m IRL          |
| Min Range       | 45      | 45   | ------ | Arming distance     |
| Reload Time     | ------- | 7.0s | ------ | Slower rate         |
| Smoke/WP Reload | ------- | 3.4s | ------ | Faster for smoke    |
| HE Damage       | ------- | 20   | ------ | Heavy fragmentation |

**Accuracy (radiusTable):**
| Distance | Spread (meters) | Notes                 |
| -------- | --------------- | --------------------- |
| 0m       | 4m              | Minimum dispersion    |
| 120m     | 18m             | Standard engagement   |
| 225m     | 35m             | Max range             |
| 225m+    | 100m            | Beyond max (unusable) |

**Applies to:**
- 107mm GVPM (Soviet)
- 4.2-inch M2 Mortar (USA)

### Heavy Mortars (120mm class)

| Stat            | Vanilla | FCRO  | Change | Notes            |
| --------------- | ------- | ----- | ------ | ---------------- |
| Max Range       | 230     | 290   | +26%   | ~2320m IRL       |
| Min Range       | 50      | 50    | ------ | Arming distance  |
| Reload Time     | ------- | 10.0s | ------ | Very slow rate   |
| Smoke/WP Reload | ------- | 3.5s  | ------ | Faster for smoke |
| HE Damage       | ------- | 30    | ------ | Devastating      |

**Accuracy (radiusTable):**
| Distance | Spread (meters) | Notes                 |
| -------- | --------------- | --------------------- |
| 0m       | 4m              | Minimum dispersion    |
| 120m     | 18m             | Close range           |
| 170m     | 30m             | Medium range          |
| 290m     | 40m             | Max range             |
| 290m+    | 100m            | Beyond max (unusable) |

**Applies to:**
- 120mm PM-38 (Soviet)
- 120mm Granatwerfer 42 (German)
- 120mm Kranaatinheitin m/40 (Finnish)

### Super-Heavy Mortars (160mm+ class)

| Stat        | Vanilla | FCRO  | Change | Notes          |
| ----------- | ------- | ----- | ------ | -------------- |
| Max Range   | 150     | 190   | +27%   | ~1520m IRL     |
| Min Range   | 25      | 25    | ------ | Close support  |
| Reload Time | ------- | 10.0s | ------ | Very slow rate |
| HE Damage   | ------- | 30    | ------ | Devastating    |

**Accuracy (radiusTable):**
| Distance | Spread (meters) | Notes                 |
| -------- | --------------- | --------------------- |
| 0m       | 4m              | Minimum dispersion    |
| 190m     | 15m             | Max range (accurate)  |
| 190m+    | 100m            | Beyond max (unusable) |

**Applies to:**
- 160mm MT-13 (Soviet)
- Japanese Type 97 150mm (via MACE)

---

## Rocket Artillery

Rocket artillery provides devastating area saturation fire. FCRO increases range by ~20% to reflect realistic engagement distances.

### Soviet Katyusha Systems

| Weapon     | Mount  | Vanilla Range | FCRO Range | Change | Rockets   |
| ---------- | ------ | ------------- | ---------- | ------ | --------- |
| BM-13      | Truck  | 325           | 390        | +20%   | 16x 132mm |
| BM-8-24    | Truck  | 290           | 350        | +21%   | 24x 82mm  |
| BM-8-48    | Truck  | 290           | 350        | +21%   | 48x 82mm  |
| BM-30      | Rail   | 275           | 330        | +20%   | 12x 300mm |
| M-30 Frame | Ground | 275           | 330        | +20%   | 4x 300mm  |
| M-31 Frame | Ground | 275           | 330        | +20%   | 4x 300mm  |

**BM-13 Katyusha Accuracy (radiusTable):**
| Distance | Spread | Notes               |
| -------- | ------ | ------------------- |
| 0m       | 4m     | Close range         |
| 350m     | 38m    | Standard engagement |
| 390m     | 40m    | Max range           |
| 390m+    | 100m   | Beyond max          |

### German Nebelwerfer Systems

| Weapon                   | Mount      | Vanilla Range | FCRO Range | Change | Rockets   |
| ------------------------ | ---------- | ------------- | ---------- | ------ | --------- |
| 150mm Nebelwerfer 41     | Towed      | 310           | 375        | +21%   | 6x 150mm  |
| 150mm Panzerwerfer 42    | Half-track | 310           | 375        | +21%   | 10x 150mm |
| 210mm Nebelwerfer 42     | Towed      | 320           | 385        | +20%   | 5x 210mm  |
| 300mm Nebelwerfer 42     | Towed      | 280           | 336        | +20%   | 6x 300mm  |
| 280mm Wurfrahmen 40 (x6) | Vehicle    | 250           | 300        | +20%   | 6x 280mm  |
| 300mm Wurfrahmen 40 (x4) | Vehicle    | 280           | 336        | +20%   | 4x 300mm  |
| 300mm Wurfrahmen 40 (x6) | Vehicle    | 280           | 336        | +20%   | 6x 300mm  |
| 380mm Sturmtiger         | SPG        | ~300          | 360        | +20%   | 1x 380mm  |

**150mm Nebelwerfer Accuracy (radiusTable):**
| Distance | Spread | Notes               |
| -------- | ------ | ------------------- |
| 0m       | 4m     | Close range         |
| 340m     | 18m    | Standard engagement |
| 375m     | 20m    | Max range           |
| 375m+    | 100m   | Beyond max          |

### American Rocket Systems

| Weapon       | Mount      | Vanilla Range | FCRO Range | Change | Rockets   |
| ------------ | ---------- | ------------- | ---------- | ------ | --------- |
| T34 Calliope | M4 Sherman | 270           | 325        | +20%   | 60x 114mm |

**Calliope Accuracy (radiusTable):**
| Distance | Spread | Notes               |
| -------- | ------ | ------------------- |
| 0m       | 4m     | Close range         |
| 300m     | 32m    | Standard engagement |
| 325m     | 35m    | Max range           |
| 325m+    | 100m   | Beyond max          |

### British Rocket Systems

| Weapon                     | Mount | Vanilla Range | FCRO Range | Change | Rockets  |
| -------------------------- | ----- | ------------- | ---------- | ------ | -------- |
| Land Mattress              | Towed | 310           | 375        | +21%   | 30x 76mm |
| 50mm Rocket Projector      | Towed | 140           | 170        | +21%   | 16x 50mm |
| 50mm Rocket Projector (x4) | Ship  | 140           | 170        | +21%   | 4x 50mm  |

**Land Mattress Accuracy (radiusTable):**
| Distance | Spread | Notes               |
| -------- | ------ | ------------------- |
| 0m       | 4m     | Close range         |
| 340m     | 27m    | Standard engagement |
| 375m     | 30m    | Max range           |
| 375m+    | 100m   | Beyond max          |

### Aircraft Rockets

| Weapon     | Nation  | Platform      | Vanilla Range | FCRO Range | Change |
| ---------- | ------- | ------------- | ------------- | ---------- | ------ |
| RP-3 (x2)  | British | Typhoon, etc. | 180           | 220        | +22%   |
| RP-3 (x4)  | British | Typhoon, etc. | 180           | 220        | +22%   |
| HVAR (x4)  | USA     | P-47, etc.    | 300           | 360        | +20%   |
| HVAR (x10) | USA     | P-47, etc.    | 300           | 360        | +20%   |
| RS-82      | Soviet  | IL-2, etc.    | 300           | 360        | +20%   |

**Aircraft Rocket Notes:**
- `unlimitedRangeTPC 0` restricts range in tactical/first-person camera
- Aircraft must dive to engage at maximum ranges
- Unguided rockets have significant spread at range

---

## See Also

- **[Quick Reference](quick-reference.md)** - At-a-glance range comparisons
- **[Vehicle Weapons](vehicle-weapons.md)** - Tank and artillery guns
- **[Game Mechanics](game-mechanics.md)** - Accuracy and damage systems
