# Game Mechanics

This section covers core FCRO game systems including veterancy, vehicle damage, vision/spotting, and accuracy mechanics.

## Veterancy System

### Experience Levels

FCRO emphasizes skill-based advantages over health bonuses. Experienced soldiers are significantly more effective, but not bullet-sponges.

| Level | Name        | Description                  |
| ----- | ----------- | ---------------------------- |
| 0     | Raw Recruit | No bonuses                   |
| 1     | Green       | Basic training, first combat |
| 2     | Experienced | Survived several engagements |
| 3     | Regular     | Battle-hardened              |
| 4     | Veteran     | Core of the army             |
| 5     | Hardened    | Elite combat effectiveness   |
| 6     | Crack       | Among the best               |
| 7     | Elite       | The best of the best         |
| 8     | Legendary   | Near superhuman              |

### Veterancy Bonuses by Level

| Level | Health | Weapon Reload | Weapon Skill | Cannon | Tank/Vehicle | Stamina |
| ----- | ------ | ------------- | ------------ | ------ | ------------ | ------- |
| 0     | +0%    | +0%           | +0           | +0%    | +0%          | +0%     |
| 1     | +0%    | +12%          | +1           | +8%    | +5%          | +10%    |
| 2     | +0%    | +18%          | +1           | +15%   | +12%         | +15%    |
| 3     | +0%    | +25%          | +2           | +22%   | +18%         | +20%    |
| 4     | +5%    | +30%          | +2           | +30%   | +25%         | +25%    |
| 5     | +8%    | +35%          | +3           | +38%   | +32%         | +35%    |
| 6     | +10%   | +38%          | +3           | +45%   | +38%         | +40%    |
| 7     | +12%   | +42%          | +4           | +52%   | +45%         | +50%    |
| 8     | +15%   | +45%          | +5           | +60%   | +50%         | +60%    |

**Key Changes from Vanilla:**
- Health bonuses drastically reduced (was up to +25%)
- Weapon skill bonuses increased (experience = accuracy)
- Weapon reload speed increased (muscle memory)
- Tank/vehicle operation bonuses increased

### Rifle Skill by Level & Stance

Accuracy multiplier (higher = more accurate):

| Level      | Standing | Crouched | Prone | Cover | Vehicle |
| ---------- | -------- | -------- | ----- | ----- | ------- |
| 1 (Green)  | 0.50     | 0.62     | 0.75  | 0.78  | 1.10    |
| 2          | 0.60     | 0.72     | 0.88  | 0.90  | 1.22    |
| 3 (Exp.)   | 0.72     | 0.85     | 1.02  | 1.05  | 1.38    |
| 4 (Vet.)   | 0.88     | 1.02     | 1.18  | 1.22  | 1.55    |
| 5          | 1.05     | 1.20     | 1.35  | 1.40  | 1.72    |
| 6 (Crack)  | 1.25     | 1.42     | 1.55  | 1.60  | 1.92    |
| 7 (Elite)  | 1.45     | 1.62     | 1.78  | 1.85  | 2.15    |
| 8 (Legend) | 1.68     | 1.85     | 2.02  | 2.10  | 2.40    |

**Key Insight:**
- A Legendary soldier in cover (2.10) is 4.2x more accurate than a Green soldier standing (0.50)
- Prone/cover provides massive benefits - always use cover!
- Vehicle accuracy is higher numerically but represents less stable platform

---

## Vehicle Damage System

### Penetration Effects by Shell Caliber

When a shell penetrates armor, crew casualties are calculated:

#### Heavy Tanks (Tiger, IS-2, etc.)

| Shell Type            | Crew Kill Chance | Crew Shock Time |
| --------------------- | ---------------- | --------------- |
| AT Rifle (14.5mm)     | 15%              | 3s              |
| 20-25mm Auto-cannon   | 20%              | 3s              |
| 37-40mm (no filler)   | 35%              | 4s              |
| 37-47mm (HE filler)   | 60%              | 6s              |
| 50-57mm (no filler)   | 60%              | 6s              |
| 50-57mm (HE filler)   | 75%              | 7s              |
| 75-76mm (no filler)   | 70%              | 7s              |
| 75-76mm (HE filler)   | 85%              | 8s              |
| 75-76mm HEAT          | 85%              | 8s              |
| 88-105mm (no filler)  | 85%              | 8s              |
| 88-105mm (HE filler)  | 95%              | 9s              |
| 122-128mm             | 100%             | 14s             |
| 150-152mm             | 100%             | 15s             |
| Bazooka/Panzerschreck | 80%              | 11s             |
| Magnetic AT Grenade   | 75%              | 9s              |

**Key Changes from Vanilla:**
- Crew kill chances increased across the board
- APHE shells now properly devastating
- Crew shock times extended for suppression effect
- Large caliber shells near-certain crew kills

### Blast Damage to Vehicles

HE shells and explosions affect buttoned-up crew:

| Blast Energy | Example              | Crew Shock Chance | Crew Kill Chance |
| ------------ | -------------------- | ----------------- | ---------------- |
| 9+           | 150mm HE, bombs      | 100%              | 70%              |
| 7-9          | 100-130mm HE         | 100%              | 40%              |
| 5-7          | 85-93mm HE, AT mines | 90%               | 15%              |
| 3.5-5        | 75-77mm HE           | 70%               | 0%               |
| 2-3.5        | 37-65mm HE, mortars  | 25%               | 0%               |
| <2           | AP mines, grenades   | 0%                | 0%               |

---

## Vision & Spotting System

FCRO reduces spotting distances by ~20% to increase ambush effectiveness and reward proper concealment.

### Human Spotting Distances

Base spotting distance multipliers (as percentage of max vision range):

| Condition               | Vanilla | FCRO | Change |
| ----------------------- | ------- | ---- | ------ |
| **Standing**            |         |      |        |
| Moving                  | 100%    | 80%  | -20%   |
| Still                   | 100%    | 80%  | -20%   |
| Stealth                 | 75%     | 60%  | -20%   |
| Still + Stealth         | 50%     | 40%  | -20%   |
| **Crouched**            |         |      |        |
| Moving                  | 100%    | 80%  | -20%   |
| Still                   | 100%    | 80%  | -20%   |
| Stealth                 | 50%     | 40%  | -20%   |
| Still + Stealth         | 50%     | 40%  | -20%   |
| **Prone**               |         |      |        |
| Moving                  | 50%     | 40%  | -20%   |
| Still                   | 50%     | 40%  | -20%   |
| Stealth                 | 30%     | 25%  | -17%   |
| Still + Stealth         | 25%     | 20%  | -20%   |
| **In Cover**            |         |      |        |
| Standing                | 100%    | 80%  | -20%   |
| Crouched                | 100%    | 80%  | -20%   |
| Prone                   | 50%     | 40%  | -20%   |
| Cover + Stealth         | 50%     | 40%  | -20%   |
| Prone + Cover + Stealth | 25%     | 20%  | -20%   |

### Silenced Weapons - Zero Detection

These weapons produce no firing signature:
- Welrod (British)
- De Lisle Carbine (British)
- HDM Pistol (USA)
- Mosin-Nagant w/Silencer (Soviet)
- Nagant M1895 w/Silencer (Soviet)

### Vehicle Spotting Categories

| Category | Examples             | Base Distance | Moving Bonus | Firing Bonus |
| -------- | -------------------- | ------------- | ------------ | ------------ |
| Level 0  | Goliath              | 100m          | +0m          | +100m        |
| Level 1  | Motorcycles, Jeeps   | 100m          | +50m         | +170m        |
| Level 2  | Armored Cars, Trucks | 100m          | +50m         | +170m        |
| Level 3  | Light Tanks          | 100m          | +50m         | +170m        |
| Level 4  | Medium Tanks, MLRS   | 100m          | +50m         | +170m        |
| Level 5  | Heavy Tanks          | 100m          | +50m         | +170m        |
| Level 6  | SPGs (105mm+)        | 100m          | +50m         | +170m        |

### Artillery Spotting (Cannons)

| Category | Gun Type  | Firing Distance | Notes             |
| -------- | --------- | --------------- | ----------------- |
| Cannon 0 | AT Rifles | 100m            | +150m when firing |
| Cannon 1 | 20-37mm   | 100m            | +150m when firing |
| Cannon 2 | 40-50mm   | 100m            | +150m when firing |
| Cannon 3 | 57-76mm   | 100m            | +150m when firing |
| Cannon 4 | 85-90mm   | 100m            | +150m when firing |
| Cannon 5 | 100-122mm | 100m            | +150m when firing |

### Aircraft Spotting

| Category | Type           | Moving | Firing | Visible |
| -------- | -------------- | ------ | ------ | ------- |
| Plane 1  | Recon          | 400m   | 400m   | 400m    |
| Plane 2  | Fighter/Bomber | 700m   | 700m   | 700m    |

### Detection Formula Summary

**Spotted Distance = Base × Stance Modifier × Movement Modifier × Cover Modifier × Stealth Modifier**

Example: Infantry in cover, prone, using stealth:
- Vanilla: 100m × 0.25 = 25m detection
- FCRO: 80m × 0.20 = 16m detection (36% harder to spot!)

---

## Accuracy System

### How Accuracy Works in GoH

The game uses `radiusTable` to define accuracy spread at various distances:
- Lower values = more accurate
- Values represent the radius (in meters) where shots can land
- At range 0, accuracy is perfect (spread = 0)
- Spread increases with distance

#### Example: Rifle Accuracy Curve
```
radiusTable {0 0.02} {40 r0} {80 r1} {120 r2} {150 r3} {180 6.0}
```
This means:
- 0m: 0.02m spread (nearly perfect)
- 40m: r0 spread (small)
- 80m: r1 spread (medium-small)
- 120m: r2 spread (medium)
- 150m: r3 spread (large)
- 180m+: 6.0m spread (very large, beyond effective range)

### FCRO Accuracy Philosophy

FCRO generally improves accuracy by:
1. Reducing spread values at each range bracket
2. Extending the effective range before accuracy degrades
3. Maintaining realistic relative accuracy between weapon types

### Spread Tolerance

`spreadTolerance` defines when AI will fire:
- Value of 0.3 = AI fires when 30% of shots will hit
- Higher values = AI fires earlier (less accurate)
- Lower values = AI waits for better shots

### AI Firing Timeout

`aiDistanceSpreadTimeout` controls how long AI waits before firing:
- `{distance% time}` format
- Longer timeouts at range = more careful aiming
- Shorter timeouts up close = faster reaction

### Damage Falloff

Many weapons use `FalloffMeter` to reduce damage at range:
- Damage starts decreasing at this distance
- `FalloffStrength` determines how quickly damage drops
- Example: SMG at 70m may do only 50% damage

### Burst Accuracy

`burstAccuracy` defines how accuracy degrades during sustained fire:
- First shot is most accurate
- Subsequent shots have increasing penalties
- Machine guns have lower penalties than rifles

---

## Weapon File Locations

All FCRO weapon overrides are located in:
```
resource/set/stuff/
├── rifle/           # Rifles, snipers, AT rifles
│   ├── .presets     # Base macros
│   ├── sniper/      # Sniper rifles
│   ├── ptr/         # Anti-tank rifles
│   └── eng/         # British weapons
├── smg/             # Submachine guns
├── mgun/            # Machine guns
├── pistol/          # Sidearms
├── mortar/          # Mortars
│   └── .presets     # Mortar range macros
├── gun/             # Tank/artillery guns
│   └── .presets     # Tank gun range macros
├── bazooka/         # RPGs, bazookas
├── flame/           # Flamethrowers
├── reactive/        # Rockets, missiles
├── grenade/         # Rifle grenades
└── explosive/       # Mines, charges
```

---

## See Also

- **[Infantry Weapons](infantry-weapons.md)** - Weapon-specific accuracy curves
- **[Vehicle Weapons](vehicle-weapons.md)** - Tank gun damage mechanics
- **[Reference Tables](reference-tables.md)** - Penetration and damage data
