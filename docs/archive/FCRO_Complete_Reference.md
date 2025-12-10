# FCRO Weapon Statistics Documentation
## Frontlines Combat Realism Overhaul - Complete Weapon Reference

This document catalogs all weapon ranges, accuracy, and damage values modified by FCRO compared to vanilla.

**Mod Philosophy:** FCRO increases engagement ranges by 20-50% to create more realistic combat distances while maintaining weapon role balance. Damage has been increased to make combat more lethal and decisive.

**Scale Note:** The game uses approximately 8:1 scale. A 180m in-game range represents ~1440m real-world distance.

---

# Quick Reference - Range Summary

| Weapon Type             | Vanilla Range | FCRO Range | Change |
| ----------------------- | ------------- | ---------- | ------ |
| **Infantry Small Arms** |               |            |        |
| Bolt-Action Rifles      | 120           | 180        | +50%   |
| Semi-Auto Rifles        | 115           | 175        | +52%   |
| Auto Rifles (BAR, etc.) | 100           | 155        | +55%   |
| Submachine Guns         | 80            | 100        | +25%   |
| Pistols                 | 70            | 85         | +21%   |
| Light Machine Guns      | 110           | 140        | +27%   |
| Heavy Machine Guns      | 150           | 180        | +20%   |
| Sniper Rifles (bolt)    | 150           | 200        | +33%   |
| Sniper Rifles (semi)    | 130           | 180        | +38%   |
| **Anti-Tank Weapons**   |               |            |        |
| Anti-Tank Rifles        | 130           | 160        | +23%   |
| Bazookas/RPGs           | 72            | 90         | +25%   |
| Panzerfaust 30          | 30            | 40         | +33%   |
| Panzerfaust 60          | 40            | 55         | +38%   |
| Panzerfaust 100         | 50            | 70         | +40%   |
| Rifle Grenades (HE)     | 80            | 100        | +25%   |
| Rifle Grenades (HEAT)   | 60            | 75         | +25%   |
| **Flamethrowers**       |               |            |        |
| Infantry (typical)      | 40            | 50         | +25%   |
| Vehicle (typical)       | 60-80         | 75-100     | +25%   |
| **Mortars**             |               |            |        |
| Light (50mm)            | 140           | 175        | +25%   |
| Medium (81-82mm)        | 160           | 200        | +25%   |
| Heavy (120mm)           | 230           | 290        | +26%   |
| **Tank Guns**           |               |            |        |
| Light (37-45mm)         | 170           | 215        | +26%   |
| Medium (75-76mm)        | 180-190       | 225-240    | +25%   |
| Long (76-85mm)          | 200           | 250        | +25%   |
| Heavy (88-122mm)        | 210           | 260        | +24%   |
| Very Long (88mm L/71)   | 220           | 275        | +25%   |
| **Rocket Artillery**    |               |            |        |
| Katyusha BM-13          | 325           | 390        | +20%   |
| Nebelwerfer 150mm       | 310           | 375        | +21%   |
| Calliope                | 270           | 325        | +20%   |

---

# Table of Contents
1. [Infantry Small Arms](#infantry-small-arms)
   - [Rifles](#rifles)
   - [Sniper Rifles](#sniper-rifles)
   - [Submachine Guns](#submachine-guns)
   - [Machine Guns](#machine-guns)
   - [Pistols](#pistols)
2. [Anti-Tank Weapons](#anti-tank-weapons)
   - [Anti-Tank Rifles](#anti-tank-rifles)
   - [Bazookas & Panzerfausts](#bazookas--panzerfausts)
   - [Rifle Grenade Launchers](#rifle-grenade-launchers)
3. [Flamethrowers](#flamethrowers)
   - [Infantry Flamethrowers](#infantry-flamethrowers)
   - [Vehicle Flamethrowers](#vehicle-flamethrowers)
4. [Mortars](#mortars)
5. [Rocket Artillery](#rocket-artillery)
6. [Tank & Artillery Guns](#tank--artillery-guns)
7. [Armor Penetration Tables](#armor-penetration-tables)
   - [German Guns](#german-tank-gun-penetration)
   - [Soviet Guns](#soviet-tank-gun-penetration)
   - [American Guns](#american-tank-gun-penetration)
   - [British Guns](#british-tank-gun-penetration)
8. [Ammunition Types](#ammunition-types)
9. [Grenades & Explosives](#grenades--explosives)
   - [Hand Grenades](#hand-grenades)
   - [Satchel Charges](#satchel-charges)
   - [Mines](#mines)
10. [Veterancy System](#veterancy-system)
11. [Vehicle Damage System](#vehicle-damage-system)
12. [Vision & Spotting System](#vision--spotting-system)
    - [Human Spotting](#human-spotting-distances)
    - [Vehicle Spotting](#vehicle-spotting-categories)
    - [Aircraft Spotting](#aircraft-spotting)
13. [Faction Weapon Comparisons](#faction-weapon-comparisons)
    - [Submachine Guns](#submachine-guns-comparison)
    - [Rifles](#bolt-action-rifles-comparison)
    - [Machine Guns](#machine-gun-comparison)
    - [Sniper Rifles](#sniper-rifle-comparison)
    - [Anti-Tank](#anti-tank-rifle-comparison)
    - [Tank Guns](#tank-gun-penetration-summary)
14. [Accuracy System Notes](#accuracy-system-notes)

---

# Infantry Small Arms

## Rifles

### Bolt-Action Rifles: `rifle/.presets` → `bolt_action`

| Stat                    | Vanilla | FCRO   | Change | Notes                         |
| ----------------------- | ------- | ------ | ------ | ----------------------------- |
| Range                   | 120     | 180    | +50%   | Matches real rifle capability |
| Damage                  | 70      | 110    | +57%   | More lethal                   |
| Fire Rate               | 40 rpm  | 40 rpm | ------ | Unchanged                     |
| Accuracy Motion Penalty | ------- | 1.2x   | ------ | Less accurate while moving    |

**Zeroing Accuracy Bonus (stationary aiming):**
```
Shot 1: 95% | Shot 2: 90% | Shot 3: 85% | Shot 4: 82.5% | Shot 5: 80% | Shot 6+: 77.5-70%
```

**Applies to:**
- Mosin-Nagant M91/30 (Soviet)
- Kar98k (German)
- M1903 Springfield, M1917 Enfield (USA)
- Lee-Enfield No.1 Mk.III, No.4 Mk.I (British)
- Mosin-Nagant M39 (Finnish)

### Semi-Automatic Rifles: `rifle/.presets` → `semi_rifle`

| Stat           | Vanilla | FCRO          | Change | Notes                             |
| -------------- | ------- | ------------- | ------ | --------------------------------- |
| Range          | 120     | 180           | +50%   | Same as bolt rifles               |
| Damage         | 70      | 110           | +57%   | Same caliber = same damage        |
| Fire Rate      | 150 rpm | 150 rpm       | ------ | Unchanged                         |
| Burst Accuracy | ------- | 100→80→60→40% | ------ | Accuracy degrades with rapid fire |

**Applies to:**
- SVT-40 (Soviet)
- Gewehr 43 (German)
- M1 Garand, M1 Carbine (USA)

### Automatic Rifles: `rifle/.presets` → `auto_rifle`

| Stat           | Vanilla    | FCRO          | Change | Notes                       |
| -------------- | ---------- | ------------- | ------ | --------------------------- |
| Range          | 120        | 180           | +50%   | Full rifle range            |
| Damage         | 70         | 110           | +57%   | Rifle caliber               |
| Burst Length   | 1-2.25 rds | 1-2.25 rds    | ------ | Short controlled bursts     |
| Burst Accuracy | ---------- | 100→80→60→40% | ------ | Accuracy degrades with fire |

**Applies to:**
- AVS-36, AVT-40 (Soviet)
- FG 42 (German)

### Individual Rifle Overrides

#### De Lisle Carbine (British Suppressed)
| Stat  | Vanilla | FCRO | Change |
| ----- | ------- | ---- | ------ |
| Range | 80      | 100  | +25%   |

#### M12 Trench Shotgun (USA)
| Stat  | Vanilla | FCRO | Change |
| ----- | ------- | ---- | ------ |
| Range | 50      | 65   | +30%   |

#### Double Barrel Shotgun
| Stat  | Vanilla | FCRO | Change |
| ----- | ------- | ---- | ------ |
| Range | 50      | 65   | +30%   |

### Rifle Accuracy Curve (`rifle_range`)
*Spread radius in meters at each distance:*

| Distance | Spread | Real-World Equivalent | Notes           |
| -------- | ------ | --------------------- | --------------- |
| 0m       | 0.02m  | Point blank           | Near-perfect    |
| 40m      | 0.2m   | ~320m IRL             | Excellent       |
| 80m      | 0.4m   | ~640m IRL             | Good            |
| 120m     | 0.8m   | ~960m IRL             | Moderate        |
| 150m     | 1.6m   | ~1200m IRL            | Degraded        |
| 180m+    | 6.0m   | ~1440m IRL            | Max range, poor |

---

## Sniper Rifles

### Bolt-Action Snipers: `sniper_rifle.pattern`

| Stat                | Vanilla | FCRO   | Change | Notes                        |
| ------------------- | ------- | ------ | ------ | ---------------------------- |
| Range               | 130     | 200    | +54%   | Outranges all other infantry |
| Damage              | 100     | 130    | +30%   | One-shot kills guaranteed    |
| Fire Rate           | 24 rpm  | 24 rpm | ------ | Slow, deliberate fire        |
| Relaxation Time     | ------- | 2.0s   | ------ | Time to reset aim            |
| Aimed Shot Accuracy | ------- | 2.25x  | ------ | Special ability multiplier   |
| Aimed Shot Damage   | ------- | 5x     | ------ | Devastating headshots        |

**Zeroing Accuracy (stationary aiming):**
```
Shot 1: 90% | Shot 2: 80% | Shot 3: 70% | Shot 4: 60% | Shot 5: 50%
```

**AI Firing Timeout (delay between shots):**
| Distance   | Delay |
| ---------- | ----- |
| 40m (20%)  | 1.75s |
| 80m (40%)  | 2.8s  |
| 120m (60%) | 3.15s |
| 160m (80%) | 3.5s  |

**Applies to:**
- Mosin-Nagant PU (Soviet)
- Kar98k ZF39/ZF41 (German)
- Springfield M1903A4 (USA)
- Lee-Enfield No.4 Mk.I (T) (British)
- All Finnish sniper variants

### Semi-Auto Snipers: `semi_sniper_rifle.pattern`

| Stat                | Vanilla | FCRO                | Change | Notes                           |
| ------------------- | ------- | ------------------- | ------ | ------------------------------- |
| Range               | 120     | 180                 | +50%   | Slightly less than bolt snipers |
| Damage              | 70      | 110                 | +57%   | Same as standard rifles         |
| Fire Rate           | 175 rpm | 175 rpm             | ------ | Faster follow-up shots          |
| Relaxation Time     | ------- | 1.25s               | ------ | Faster reset than bolt          |
| Aimed Shot Accuracy | ------- | 1.5x                | ------ | Less bonus than bolt            |
| Aimed Shot Damage   | ------- | 2x                  | ------ | Less devastating                |
| Burst Accuracy      | ------- | 100→90→80→70→60→50% | ------ | Degrades with rapid fire        |

**Applies to:**
- SVT-40 w/PU scope (Soviet)
- Gewehr 43 ZF4 (German)
- M1C/M1D Garand (USA)

### Sniper Accuracy Curve (`sniper_range`)
*Spread radius in meters at each distance:*

| Distance | Spread | Real-World Equivalent | Notes            |
| -------- | ------ | --------------------- | ---------------- |
| 0m       | 0.01m  | Point blank           | Perfect          |
| 50m      | 0.05m  | ~400m IRL             | Excellent        |
| 100m     | 0.1m   | ~800m IRL             | Excellent        |
| 150m     | 0.2m   | ~1200m IRL            | Very good        |
| 200m     | 0.4m   | ~1600m IRL            | Good (max range) |
| 230m+    | 5.0m   | Beyond effective      | Unusable         |

---

## Submachine Guns

### Base Pattern: `smg.pattern`

| Stat                  | Vanilla | FCRO | Change | Notes                        |
| --------------------- | ------- | ---- | ------ | ---------------------------- |
| Range                 | 80      | 100  | +25%   | Close-quarters optimized     |
| Damage                | 55      | 70   | +27%   | Pistol caliber               |
| Reload Time           | 5.0s    | 5.0s | ------ | Magazine change              |
| Spread Tolerance      | ------- | 30%  | ------ | AI aims to 30% before firing |
| Accuracy Motion Bonus | ------- | 0.9x | ------ | Better accuracy while moving |

**Burst Accuracy Decay:**
```
Shot 1: 100% | Shot 2: 95% | Shot 3: 90% | Shot 4: 85% | Shot 5: 80% | Shot 6: 75% | Shot 7: 70% | Shot 8: 65% | Shot 9+: 60%
```

**Applies to all SMGs:**
- PPSh-41, PPS-43, PPD-40 (Soviet)
- MP40, MP38, MP28 (German)
- Thompson M1A1, M3 Grease Gun (USA)
- Sten Mk.II, Mk.III, Mk.V (British)
- Suomi KP/-31 (Finnish)

### SMG Accuracy Curve (`smg_range`)
*Spread radius in meters at each distance:*

| Distance | Spread | Real-World Equivalent | Notes           |
| -------- | ------ | --------------------- | --------------- |
| 0m       | 0.02m  | Point blank           | Near-perfect    |
| 40m      | 0.9m   | ~320m IRL             | Good            |
| 70m      | 2.2m   | ~560m IRL             | Moderate        |
| 100m+    | 4.0m   | ~800m IRL             | Max range, poor |

---

## Machine Guns

### Light/Medium MGs: `mgun_generic.pattern`

| Stat             | Vanilla | FCRO | Change | Notes                         |
| ---------------- | ------- | ---- | ------ | ----------------------------- |
| Range            | 120     | 140  | +17%   | Tanks should outrange MGs     |
| Damage           | 80      | 110  | +38%   | Rifle caliber, sustained fire |
| Reload Time      | 5.0s    | 5.0s | ------ | Belt/magazine change          |
| Trace Frequency  | 5       | 5    | ------ | Every 5th round visible       |
| Spread Tolerance | ------- | 20%  | ------ | AI aims to 20% before firing  |

**AI Firing Timeout:**
| Distance    | Delay | Notes                   |
| ----------- | ----- | ----------------------- |
| 30m (25%)   | 1.05s | Close range suppression |
| 96m (80%)   | 1.5s  | Standard engagement     |
| 120m (100%) | 1.75s | Max range               |

**Applies to:**
- DP-28, DT, SG-43 (Soviet)
- MG34, MG42 (German)
- M1919A4, M1919A6, BAR (USA)
- Bren Mk.I/II, Lewis Gun, Vickers (British)
- Lahti-Saloranta M/26 (Finnish)

### Heavy MGs: `hmgun.pattern`

| Stat             | Vanilla | FCRO | Change | Notes                        |
| ---------------- | ------- | ---- | ------ | ---------------------------- |
| Range            | 140     | 180  | +29%   | Outranges standard MGs       |
| Damage (Health)  | 180     | 220  | +22%   | Devastating anti-personnel   |
| Damage (Armor)   | 13      | 16   | +23%   | Light vehicle threat         |
| Reload Time      | 5.0s    | 5.0s | ------ | Belt change                  |
| Spread Tolerance | ------- | 20%  | ------ | AI aims to 20% before firing |

**AI Firing Timeout:**
| Distance   | Delay          |
| ---------- | -------------- |
| 45m (25%)  | 0s (immediate) |
| 135m (75%) | 1.5s           |

**Applies to:**
- DShK 12.7mm (Soviet)
- MG131 13mm (German)
- M2 Browning .50 cal (USA)
- Vickers .50 (British)

### MG Accuracy Curve (`mg_range`)
*Spread radius in meters at each distance:*

| Distance | Spread | Notes          |
| -------- | ------ | -------------- |
| 0m       | 0.02m  | Point blank    |
| 40m      | 0.3m   | Close range    |
| 100m     | 0.8m   | Medium range   |
| 150m     | 1.2m   | Extended range |
| 180m+    | 4.0m   | Max range      |

### HMG Accuracy Curve (`hmg_range`)
*Spread radius in meters at each distance:*

| Distance | Spread | Notes          |
| -------- | ------ | -------------- |
| 0m       | 0.02m  | Point blank    |
| 50m      | 0.3m   | Close range    |
| 120m     | 0.8m   | Medium range   |
| 180m     | 1.2m   | Extended range |
| 200m+    | 4.0m   | Max range      |

---

## Pistols

### Base Pattern: `pistol.pattern`

| Stat             | Vanilla | FCRO    | Change | Notes                        |
| ---------------- | ------- | ------- | ------ | ---------------------------- |
| Range            | 70      | 85      | +21%   | Emergency weapon             |
| Damage           | 60      | 75      | +25%   | Pistol caliber               |
| Fire Rate        | 300 rpm | 300 rpm | ------ | Semi-auto                    |
| Reload Time      | 3.25s   | 3.25s   | ------ | Magazine change              |
| Spread Tolerance | ------- | 30%     | ------ | AI aims to 30% before firing |

**Burst Accuracy Decay:**
```
Shot 1: 100% | Shot 2: 95% | Shot 3: 90% | Shot 4: 85% | Shot 5+: 80%
```

**AI Firing Timeout:**
| Distance   | Delay |
| ---------- | ----- |
| 25m (30%)  | 0.5s  |
| 85m (100%) | 1.0s  |

**Applies to all sidearms:**
- TT-33, Nagant M1895 (Soviet)
- Luger P08, Walther P38 (German)
- M1911A1 (USA)
- Webley Mk.VI, Enfield No.2 (British)
- Lahti L-35 (Finnish)

### Pistol Accuracy Curve (`pistol_range`)
*Spread radius in meters at each distance:*

| Distance | Spread | Notes           |
| -------- | ------ | --------------- |
| 0m       | 0.02m  | Point blank     |
| 30m      | 0.4m   | Effective range |
| 60m+     | 1.0m   | Max range       |

---

# Anti-Tank Weapons

## Anti-Tank Rifles

### Base Pattern: `at_rifle.pattern`

| Stat                    | Vanilla | FCRO  | Change | Notes                        |
| ----------------------- | ------- | ----- | ------ | ---------------------------- |
| Range                   | 120     | 160   | +33%   | Extended AT engagement       |
| Damage (Health)         | 160     | 200   | +25%   | Devastating to infantry      |
| Damage (Armor)          | 45      | 55    | +22%   | Better penetration           |
| Reload Time             | 5.0s    | 5.0s  | ------ | Single shot reload           |
| Spread Tolerance        | ------- | 20%   | ------ | AI aims to 20% before firing |
| Accuracy Motion Penalty | ------- | 0.75x | ------ | Must be stationary           |

**Zeroing Accuracy (stationary aiming):**
```
Shot 1: 90% | Shot 2: 80% | Shot 3: 75%
```

**Burst Accuracy Decay:**
```
Shot 1: 100% | Shot 2: 90% | Shot 3: 80% | Shot 4: 70% | Shot 5+: 60%
```

**AI Firing Timeout:**
| Distance   | Delay |
| ---------- | ----- |
| 48m (30%)  | 1.75s |
| 128m (80%) | 3.5s  |

**Applies to:**
- PTRD-41, PTRS-41 (Soviet)
- Panzerbüchse 39 (German)
- Boys Anti-Tank Rifle (British)
- Lahti L-39 (Finnish)

---

## Bazookas & Panzerfausts

### Base Pattern: `rpg_weapon.pattern`

| Stat                    | Vanilla | FCRO  | Change | Notes              |
| ----------------------- | ------- | ----- | ------ | ------------------ |
| Range                   | 70      | 90    | +29%   | Realistic AT range |
| Fire Rate               | 6 rpm   | 6 rpm | ------ | Slow reload        |
| Reload Time             | 10s     | 10s   | ------ | Team reload        |
| Gravity                 | 0.75    | 0.75  | ------ | Rocket drop        |
| Accuracy Motion Penalty | ------- | 0.1x  | ------ | Must be stationary |

**Zeroing Accuracy:**
```
Shot 1: 70% | Shot 2: 60% | Shot 3: 50% | Shot 4: 40%
```

**Spread Function:**
| Range % | Spread Multiplier |
| ------- | ----------------- |
| 0%      | 0                 |
| 85%     | 0.9x              |
| 100%    | 1.3x              |
| 120%    | 6x                |
| 200%    | 30x               |

**AI Firing Timeout:** 11s minimum, 3s variance

**Applies to:**
- M1/M9 Bazooka (USA)
- Panzerschreck (German)
- PIAT (British)

### Individual Overrides

#### Faustpatrone 30 (Disposable)
| Stat  | Vanilla | FCRO | Change | Notes        |
| ----- | ------- | ---- | ------ | ------------ |
| Range | 30      | 40   | +33%   | Emergency AT |

#### Panzerfaust 30
| Stat  | Vanilla | FCRO | Change | Notes       |
| ----- | ------- | ---- | ------ | ----------- |
| Range | 30      | 40   | +33%   | Short range |

#### Panzerfaust 60
| Stat  | Vanilla | FCRO | Change | Notes        |
| ----- | ------- | ---- | ------ | ------------ |
| Range | 40      | 55   | +38%   | Medium range |

#### Panzerfaust 100
| Stat  | Vanilla | FCRO | Change | Notes              |
| ----- | ------- | ---- | ------ | ------------------ |
| Range | 50      | 70   | +40%   | Long range variant |

#### M18 Recoilless Rifle (USA)
| Stat  | Vanilla | FCRO | Change | Notes              |
| ----- | ------- | ---- | ------ | ------------------ |
| Range | 90      | 115  | +28%   | Crew-served weapon |

---

## Rifle Grenade Launchers

All rifle grenade launchers follow similar patterns with FCRO increasing ranges by 25%.

### British Grenade Launchers

#### Enfield No.4 Mk.I Grenade Launcher
| Ammo Type | Vanilla Range | FCRO Range | Change |
| --------- | ------------- | ---------- | ------ |
| HE        | 80            | 100        | +25%   |
| HEAT      | 60            | 75         | +25%   |

#### Enfield No.1 Mk.III Grenade Launcher
| Ammo Type | Vanilla Range | FCRO Range | Change |
| --------- | ------------- | ---------- | ------ |
| HE        | 80            | 100        | +25%   |
| HEAT      | 60            | 75         | +25%   |

### German Grenade Launchers

#### Kar98k Grenade Launcher (Gewehrgranatgerät)
| Ammo Type | Vanilla Range | FCRO Range | Change |
| --------- | ------------- | ---------- | ------ |
| HE        | 80            | 100        | +25%   |
| HEAT      | 60            | 75         | +25%   |

#### Kar98k Anti-Tank Grenade
| Ammo Type | Vanilla Range | FCRO Range | Change |
| --------- | ------------- | ---------- | ------ |
| HEAT      | 60            | 75         | +25%   |

### American Grenade Launchers

#### M1 Garand Grenade Launcher (M7)
| Ammo Type             | Vanilla Range | FCRO Range | Change |
| --------------------- | ------------- | ---------- | ------ |
| HE                    | 80            | 100        | +25%   |
| WP (White Phosphorus) | 80            | 100        | +25%   |
| HEAT                  | 60            | 75         | +25%   |

#### M1 Carbine Grenade Launcher (M8)
| Ammo Type | Vanilla Range | FCRO Range | Change |
| --------- | ------------- | ---------- | ------ |
| HE        | 80            | 100        | +25%   |
| WP        | 80            | 100        | +25%   |
| HEAT      | 60            | 75         | +25%   |

### Soviet Grenade Launchers

#### Mosin-Nagant Grenade Launcher (Dyakonov)
| Ammo Type | Vanilla Range | FCRO Range | Change |
| --------- | ------------- | ---------- | ------ |
| HE        | 80            | 100        | +25%   |

#### Mosin-Nagant Anti-Tank Grenade (VPGS-41)
| Ammo Type | Vanilla Range | FCRO Range | Change |
| --------- | ------------- | ---------- | ------ |
| HEAT      | 60            | 75         | +25%   |

---

# Flamethrowers

All flamethrower weapons receive ~25% range increases. These weapons excel at bunker clearing and close-quarters combat.

## Infantry Flamethrowers

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

## Vehicle Flamethrowers

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

# Mortars

### Base Patterns: `mortar/.presets`

All mortar classes receive range increases while maintaining realistic accuracy degradation at range.

## Light Mortars (50mm class)

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

## Medium Mortars (81-82mm class)

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

## Medium-Heavy Mortars (107mm class)

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

## Heavy Mortars (120mm class)

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

## Super-Heavy Mortars (160mm+ class)

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

# Rocket Artillery

Rocket artillery provides devastating area saturation fire. FCRO increases range by ~20% to reflect realistic engagement distances.

## Soviet Katyusha Systems

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

## German Nebelwerfer Systems

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

## American Rocket Systems

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

## British Rocket Systems

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

## Aircraft Rockets

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

# Tank & Artillery Guns

Tank and artillery guns use standardized range macros to ensure consistent engagement distances across similar weapon types. FCRO increases all ranges by 25%+.

## Range Macros (via `gun/.presets`)

These macros define the base engagement ranges for tank and artillery guns:

| Macro Name  | Vanilla Range | FCRO Range | Change | Typical Use                                 |
| ----------- | ------------- | ---------- | ------ | ------------------------------------------- |
| `range_160` | 160           | 200        | +25%   | Short-barrel 75mm howitzers, early war guns |
| `range_170` | 170           | 215        | +26%   | Light tank guns (37mm, 40mm, 45mm)          |
| `range_180` | 180           | 225        | +25%   | Medium tank guns (76mm F-34, 75mm M3)       |
| `range_190` | 190           | 240        | +26%   | Medium-long guns (76mm ZiS-3, 75mm Pak 40)  |
| `range_200` | 200           | 250        | +25%   | Long-barrel tank guns (76mm M1, 85mm)       |
| `range_210` | 210           | 260        | +24%   | Heavy tank guns (88mm L/56, 122mm)          |
| `range_220` | 220           | 275        | +25%   | Very long-barrel guns (88mm L/71, 17-pdr)   |

## Howitzer Range Macros

Separate macros for indirect-fire capable howitzers with higher arcs:

| Macro Name           | Vanilla Range | FCRO Range | Change | Typical Use             |
| -------------------- | ------------- | ---------- | ------ | ----------------------- |
| `range_160_howitzer` | 160           | 200        | +25%   | Short assault howitzers |
| `range_170_howitzer` | 170           | 215        | +26%   | Infantry guns           |
| `range_180_howitzer` | 180           | 225        | +25%   | Medium howitzers        |
| `range_190_howitzer` | 190           | 240        | +26%   | Field howitzers         |
| `range_200_howitzer` | 200           | 250        | +25%   | Heavy howitzers         |
| `range_210_howitzer` | 210           | 260        | +24%   | Super-heavy howitzers   |

## German Tank Guns

### 75mm KwK 40 L/43 (Pz.IV F2, StuG III G early)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 190               | 240  | +26%   |
| Uses  | `range_190` macro |      |        |

### 75mm KwK 42 L/70 (Panther)
| Stat  | Vanilla                | FCRO | Change |
| ----- | ---------------------- | ---- | ------ |
| Range | 200                    | 260  | +30%   |
| Uses  | `range_200` + override |      |        |

### 88mm KwK 36 L/56 (Tiger I)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 200               | 250  | +25%   |
| Uses  | `range_200` macro |      |        |

### 88mm KwK 43 L/71 (Tiger II, Nashorn)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 220               | 275  | +25%   |
| Uses  | `range_220` macro |      |        |

### 128mm PaK 44 L/55 (Jagdtiger)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 220+              | 275+ | +25%   |
| Uses  | `range_220` macro |      |        |

## Soviet Tank Guns

### 45mm 20-K (T-70, BA-10)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 170               | 215  | +26%   |
| Uses  | `range_170` macro |      |        |

### 76mm F-34 (T-34/76, KV-1)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 180               | 225  | +25%   |
| Uses  | `range_180` macro |      |        |

### 85mm ZiS-S-53/D-5T (T-34/85, KV-85)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 200               | 250  | +25%   |
| Uses  | `range_200` macro |      |        |

### 100mm D-10T (SU-100, T-54 prototype)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 210               | 260  | +24%   |
| Uses  | `range_210` macro |      |        |

### 122mm D-25T (IS-2, ISU-122)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 210               | 260  | +24%   |
| Uses  | `range_210` macro |      |        |

### 152mm ML-20S (ISU-152)
| Stat  | Vanilla                    | FCRO | Change |
| ----- | -------------------------- | ---- | ------ |
| Range | 200                        | 250  | +25%   |
| Uses  | `range_200_howitzer` macro |      |        |

## American Tank Guns

### 37mm M6 (M3 Stuart)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 170               | 215  | +26%   |
| Uses  | `range_170` macro |      |        |

### 75mm M3 (M4 Sherman early)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 180               | 225  | +25%   |
| Uses  | `range_180` macro |      |        |

### 76mm M1A1/M1A2 (M4A1 76W, M18)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 200               | 250  | +25%   |
| Uses  | `range_200` macro |      |        |

### 90mm M3 (M26 Pershing, M36)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 210               | 260  | +24%   |
| Uses  | `range_210` macro |      |        |

### 105mm T5E1 (T26E4 Super Pershing)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 220               | 275  | +25%   |
| Uses  | `range_220` macro |      |        |

## British Tank Guns

### QF 2-pounder (40mm - Matilda, Valentine)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 160               | 200  | +25%   |
| Uses  | `range_160` macro |      |        |

### QF 6-pounder (57mm - Cromwell, Churchill III)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 180               | 225  | +25%   |
| Uses  | `range_180` macro |      |        |

### OQF 75mm (Cromwell, Churchill VI)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 180               | 225  | +25%   |
| Uses  | `range_180` macro |      |        |

### QF 77mm HV (Comet)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 200               | 250  | +25%   |
| Uses  | `range_200` macro |      |        |

### QF 17-pounder (76.2mm - Firefly, Achilles, Archer)
| Stat  | Vanilla                          | FCRO    | Change  |
| ----- | -------------------------------- | ------- | ------- |
| Range | 210-220                          | 260-275 | +24-25% |
| Uses  | `range_210` or `range_220` macro |         |         |
| Notes | APDS available                   |         |         |

### Ordnance QF 25-pounder (87.6mm - Sexton)
| Stat  | Vanilla                    | FCRO | Change |
| ----- | -------------------------- | ---- | ------ |
| Range | 190                        | 240  | +26%   |
| Uses  | `range_190_howitzer` macro |      |        |

## Japanese Tank Guns

### Type 1 47mm (Chi-Ha Kai)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 170               | 215  | +26%   |
| Uses  | `range_170` macro |      |        |

### Type 90 75mm (Chi-Nu)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 180               | 225  | +25%   |
| Uses  | `range_180` macro |      |        |

### Type 5 75mm (Chi-To, Chi-Ri)
| Stat  | Vanilla           | FCRO | Change |
| ----- | ----------------- | ---- | ------ |
| Range | 200               | 250  | +25%   |
| Uses  | `range_200` macro |      |        |

## Finnish Tank Guns

Finnish forces use captured and purchased equipment, inheriting the range values from their origin nations (Soviet, German, British, Swedish).

---

# Armor Penetration Tables

This section documents the armor penetration values at various ranges for tank guns. Penetration values are in mm of RHA (Rolled Homogeneous Armor) at 0° impact angle.

## Penetration Falloff System

FCRO uses a sophisticated penetration curve system with values at key distance brackets:
- **10m**: Point-blank (slightly higher than 30m due to velocity)
- **30m**: Close range baseline
- **100m**: Short engagement
- **155m**: Medium engagement
- **205m**: Long engagement
- **250m**: Maximum range

## German Tank Gun Penetration

### 75mm KwK 42 L/70 (Panther)
| Distance | Pzgr.39/42 (APCBC-HE) | Pzgr.40/42 (APCR) |
| -------- | --------------------- | ----------------- |
| 30m      | 185mm                 | 265mm             |
| 100m     | 168mm                 | 234mm             |
| 155m     | 149mm                 | 199mm             |
| 205m     | 132mm                 | 170mm             |
| 250m     | 116mm                 | 145mm             |

**Velocity:** AP 935 m/s | APCR 1130 m/s
**Post-Penetration Damage:** 200

### 88mm KwK 36 L/56 (Tiger I)
| Distance | Pzgr.39 (APCBC-HE) | Pzgr.40 (APCR) | Gr.39 Hl (HEAT) |
| -------- | ------------------ | -------------- | --------------- |
| 30m      | 162mm              | 219mm          | 110mm           |
| 100m     | 151mm              | 200mm          | 110mm           |
| 155m     | 138mm              | 179mm          | 110mm           |
| 205m     | 126mm              | 160mm          | 110mm           |
| 250m     | 116mm              | 143mm          | 110mm           |

**Velocity:** AP 780 m/s | APCR 930 m/s | HEAT 600 m/s
**Post-Penetration Damage:** 240

### 88mm KwK 43 L/71 (Tiger II, Nashorn)
| Distance | Pzgr.39 (APCBC-HE) | Pzgr.40 (APCR) | HEAT  |
| -------- | ------------------ | -------------- | ----- |
| 30m      | 232mm              | 304mm          | 110mm |
| 100m     | 219mm              | 282mm          | 110mm |
| 155m     | 204mm              | 257mm          | 110mm |
| 205m     | 190mm              | 234mm          | 110mm |
| 250m     | 176mm              | 213mm          | 110mm |

**Velocity:** AP 1000 m/s | APCR 1130 m/s
**Post-Penetration Damage:** 240

## Soviet Tank Gun Penetration

### 76mm F-34 (T-34/76, KV-1)
| Distance | BR-350A (APHE) | BR-350B (APHEBC) | BR-350P (APCR) | BP-350A (HEAT) |
| -------- | -------------- | ---------------- | -------------- | -------------- |
| 30m      | 75mm           | 82mm             | 130mm          | 75mm           |
| 100m     | 66mm           | 74mm             | 92mm           | 75mm           |
| 155m     | 57mm           | 65mm             | 60mm           | 75mm           |
| 205m     | 52mm           | 59mm             | 39mm           | 75mm           |

**Velocity:** APHE 655 m/s | APCR 955 m/s
**Post-Penetration Damage:** 200

### 85mm ZiS-S-53 (T-34/85)
| Distance | BR-365K (APHE) | BR-365 (APHEBC) | BR-367 (APCBC) | BR-365P (APCR) |
| -------- | -------------- | --------------- | -------------- | -------------- |
| 30m      | 142mm          | 122mm           | 164mm          | 175mm          |
| 100m     | 125mm          | 116mm           | 154mm          | 136mm          |
| 155m     | 107mm          | 105mm           | 134mm          | 100mm          |
| 205m     | 92mm           | 96mm            | 115mm          | 73mm           |
| 250m     | 78mm           | 88mm            | 96mm           | 54mm           |

**Velocity:** AP 792 m/s | APCR 1050 m/s
**Post-Penetration Damage:** 230

### 122mm D-25T (IS-2)
| Distance | BR-471 (APHE) | BR-471B (APHEBC) | BR-471D (APCBC) |
| -------- | ------------- | ---------------- | --------------- |
| 30m      | 195mm         | 196mm            | 230mm           |
| 100m     | 177mm         | 179mm            | 215mm           |
| 155m     | 157mm         | 159mm            | 200mm           |
| 205m     | 140mm         | 142mm            | 186mm           |
| 250m     | 124mm         | 126mm            | 173mm           |

**Velocity:** AP 781 m/s
**Post-Penetration Damage:** 320
**Reload:** 20 seconds

## American Tank Gun Penetration

### 75mm M3 (M4 Sherman)
| Distance | AP M72 | APC M61 (inert/HE) |
| -------- | ------ | ------------------ |
| 30m      | 109mm  | 88mm               |
| 100m     | 92mm   | 81mm               |
| 155m     | 76mm   | 73mm               |
| 205m     | 62mm   | 65mm               |

**Velocity:** AP 619 m/s
**Post-Penetration Damage:** 200

### 76mm M1A1 (M4A1 76W, M18)
| Distance | M79 AP | M62 APC | T-4/M93 HVAP |
| -------- | ------ | ------- | ------------ |
| 30m      | 154mm  | 125mm   | 239mm        |
| 100m     | 131mm  | 116mm   | 208mm        |
| 155m     | 107mm  | 105mm   | 175mm        |
| 205m     | 88mm   | 95mm    | 147mm        |
| 250m     | 72mm   | 86mm    | 124mm        |

**Velocity:** AP 792 m/s | HVAP 1036 m/s
**Post-Penetration Damage:** 200

### 90mm M3 (M26 Pershing, M36)
| Distance | M77 AP | T33 APBC | M82 APC | T30E16 HVAP |
| -------- | ------ | -------- | ------- | ----------- |
| 30m      | 188mm  | 164mm    | 169mm   | 306mm       |
| 100m     | 163mm  | 158mm    | 164mm   | 278mm       |
| 155m     | 137mm  | 152mm    | 151mm   | 246mm       |
| 205m     | 115mm  | 146mm    | 138mm   | 218mm       |
| 250m     | 96mm   | 140mm    | 127mm   | 193mm       |

**Velocity:** AP 823 m/s | APBC 853 m/s | HVAP 1018 m/s
**Post-Penetration Damage:** 240
**Note:** T33 APBC designed to defeat sloped armor (Panther glacis)

## British Tank Gun Penetration

### QF 17-pounder (Firefly, Achilles, Archer)
| Distance | Shot Mk.6 AP | Shot Mk.4 APC | Shot Mk.8 APCBC | SV Mk.1 APDS |
| -------- | ------------ | ------------- | --------------- | ------------ |
| 30m      | 171mm        | 171mm         | 190mm           | 228mm        |
| 100m     | 168mm        | 168mm         | 187mm           | 226mm        |
| 155m     | 155mm        | 155mm         | 172mm           | 207mm        |
| 205m     | 139mm        | 139mm         | 155mm           | 189mm        |
| 250m     | 126mm        | 126mm         | 140mm           | 159mm        |

**Velocity:** AP 900 m/s | APDS 1200 m/s
**Post-Penetration Damage:** 200

---

# Ammunition Types

## AP (Armor Piercing) Shell Types

| Type     | Full Name               | HE Filler | Slope Performance | Post-Pen Damage |
| -------- | ----------------------- | --------- | ----------------- | --------------- |
| AP       | Armor Piercing          | None      | Poor              | 1.0x            |
| APC      | AP Capped               | None      | Good              | 1.0x            |
| APHE     | AP High-Explosive       | Yes       | Poor              | 1.25x           |
| APBC     | AP Ballistic Cap        | None      | Good              | 1.0x            |
| APCBC    | AP Capped Ballistic Cap | None      | Excellent         | 1.0x            |
| APCBC-HE | APCBC with HE filler    | Yes       | Excellent         | 1.25x           |
| APHEBC   | APHE with Ballistic Cap | Yes       | Good              | 1.25x           |
| APCR     | AP Composite Rigid      | None      | Very Poor         | 1.0x            |
| HVAP     | High-Velocity AP        | None      | Very Poor         | 1.0x            |
| APDS     | AP Discarding Sabot     | None      | Moderate          | 1.0x            |
| HEAT     | High-Explosive AT       | Chemical  | None (fixed)      | 1.25x           |

## Slope Modifiers by Shell Type

APCR/HVAP suffers heavily against sloped armor:

| Angle | AP/APC | APCR (≤76mm) | APCR (>76mm) | APDS  | HEAT |
| ----- | ------ | ------------ | ------------ | ----- | ---- |
| 0°    | 1.0x   | 1.0x         | 1.0x         | 1.0x  | 1.0x |
| 30°   | 1.36x  | 1.36x        | 1.29x        | 1.23x | 1.0x |
| 45°   | 2.28x  | 2.28x        | 2.14x        | 1.82x | 1.0x |
| 60°   | 4.23x  | 4.23x        | 4.58x        | 3.54x | 1.0x |
| 75°   | 8.52x  | 8.52x        | 12.81x       | 9.57x | 1.0x |

**Key Insight:** HEAT shells ignore slope entirely - excellent against sloped targets but lower base penetration.

---

# Grenades & Explosives

## Hand Grenades

### Anti-Personnel Grenade (Base Pattern)
| Stat            | Vanilla | FCRO   | Notes                     |
| --------------- | ------- | ------ | ------------------------- |
| Throw Range     | 22m     | 22m    | ~176m IRL                 |
| Prep Time       | 4.75s   | 4.75s  | Pull pin + throw          |
| Lethal Radius   | 3-6m    | 2-5m   | Tighter, more lethal core |
| Wounding Radius | ------- | 5-12m  | Extended fragmentation    |
| Casualty Radius | ------- | 10-18m | Light wounds              |

**Blast Energy:**
| Zone                | Energy | Range  |
| ------------------- | ------ | ------ |
| Core (lethal)       | 2.5    | 2-5m   |
| Mid (wounding)      | 1.4    | 5-12m  |
| Outer (suppression) | 0.6    | 10-18m |

**Applies to:**
- F1 Grenade (Soviet)
- RGD-33 (Soviet)
- Model 24 Stielhandgranate (German)
- Model 39 Eihandgranate (German)
- Mk.II Pineapple (USA)
- Mills Bomb No.36 (British)

## Satchel Charges

### M32 Satchel Charge
| Stat                | Vanilla  | FCRO     | Notes          |
| ------------------- | -------- | -------- | -------------- |
| Explosive Mass      | 2.0kg    | 2.0kg    | TNT equivalent |
| Prep Time           | 5.5s     | 5.5s     | Arm + throw    |
| Vehicle Damage Zone | 0.3-0.5m | 0.3-0.5m | Direct contact |
| Lethal Radius       | 1-2m     | 1.5-3m   | +50%           |
| Casualty Radius     | 4.5-6m   | 5-9m     | +50%           |

**Blast Energy:**
| Zone  | Vanilla | FCRO | Change |
| ----- | ------- | ---- | ------ |
| Core  | 7.6     | 10.0 | +32%   |
| Mid   | 1.5     | 3.0  | +100%  |
| Outer | 1.0     | 1.5  | +50%   |

---

## Mines

### S-Mine (Bouncing Betty)
The most lethal AP mine of WWII - bounces 1m before detonating 360 steel balls.

| Stat            | Vanilla | FCRO   | Notes |
| --------------- | ------- | ------ | ----- |
| Lethal Radius   | 0.6-2m  | 0.8-3m | +50%  |
| Kill Radius     | 3-5m    | 4-10m  | +100% |
| Wounding Radius | 6-8m    | 10-18m | +125% |

**Blast Energy:**
| Zone  | Vanilla | FCRO | Change |
| ----- | ------- | ---- | ------ |
| Core  | 1.0     | 3.0  | +200%  |
| Mid   | 0.51    | 1.5  | +194%  |
| Outer | 0.25    | 0.7  | +180%  |

### Anti-Tank Mine (Tellermine)
| Stat                     | Vanilla  | FCRO     | Notes               |
| ------------------------ | -------- | -------- | ------------------- |
| Vehicle Damage Zone      | 0.6-1.0m | 0.6-1.0m | Track/wheel contact |
| Lethal Radius (infantry) | 2-3m     | 2.5-4m   | +33%                |
| Casualty Radius          | 6-8m     | 7-10m    | +25%                |

**Blast Energy:**
| Zone  | Vanilla | FCRO | Change |
| ----- | ------- | ---- | ------ |
| Core  | 9.0     | 12.0 | +33%   |
| Mid   | 3.0     | 4.5  | +50%   |
| Outer | 1.0     | 1.5  | +50%   |

---

# Veterancy System

## Experience Levels

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

## Veterancy Bonuses by Level

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

## Rifle Skill by Level & Stance

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

# Vehicle Damage System

## Penetration Effects by Shell Caliber

When a shell penetrates armor, crew casualties are calculated:

### Heavy Tanks (Tiger, IS-2, etc.)

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

### Key Changes from Vanilla:
- Crew kill chances increased across the board
- APHE shells now properly devastating
- Crew shock times extended for suppression effect
- Large caliber shells near-certain crew kills

## Blast Damage to Vehicles

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

---

# Vision & Spotting System

FCRO reduces spotting distances by ~20% to increase ambush effectiveness and reward proper concealment.

## Human Spotting Distances

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

## Silenced Weapons - Zero Detection

These weapons produce no firing signature:
- Welrod (British)
- De Lisle Carbine (British)
- HDM Pistol (USA)
- Mosin-Nagant w/Silencer (Soviet)
- Nagant M1895 w/Silencer (Soviet)

## Vehicle Spotting Categories

| Category | Examples             | Base Distance | Moving Bonus | Firing Bonus |
| -------- | -------------------- | ------------- | ------------ | ------------ |
| Level 0  | Goliath              | 100m          | +0m          | +100m        |
| Level 1  | Motorcycles, Jeeps   | 100m          | +50m         | +170m        |
| Level 2  | Armored Cars, Trucks | 100m          | +50m         | +170m        |
| Level 3  | Light Tanks          | 100m          | +50m         | +170m        |
| Level 4  | Medium Tanks, MLRS   | 100m          | +50m         | +170m        |
| Level 5  | Heavy Tanks          | 100m          | +50m         | +170m        |
| Level 6  | SPGs (105mm+)        | 100m          | +50m         | +170m        |

## Artillery Spotting (Cannons)

| Category | Gun Type  | Firing Distance | Notes             |
| -------- | --------- | --------------- | ----------------- |
| Cannon 0 | AT Rifles | 100m            | +150m when firing |
| Cannon 1 | 20-37mm   | 100m            | +150m when firing |
| Cannon 2 | 40-50mm   | 100m            | +150m when firing |
| Cannon 3 | 57-76mm   | 100m            | +150m when firing |
| Cannon 4 | 85-90mm   | 100m            | +150m when firing |
| Cannon 5 | 100-122mm | 100m            | +150m when firing |

## Aircraft Spotting

| Category | Type           | Moving | Firing | Visible |
| -------- | -------------- | ------ | ------ | ------- |
| Plane 1  | Recon          | 400m   | 400m   | 400m    |
| Plane 2  | Fighter/Bomber | 700m   | 700m   | 700m    |

## Detection Formula Summary

**Spotted Distance = Base × Stance Modifier × Movement Modifier × Cover Modifier × Stealth Modifier**

Example: Infantry in cover, prone, using stealth:
- Vanilla: 100m × 0.25 = 25m detection
- FCRO: 80m × 0.20 = 16m detection (36% harder to spot!)

---

# Faction Weapon Comparisons

## Submachine Guns Comparison

All SMGs use the same base pattern with identical core stats:

| Stat             | All SMGs     |
| ---------------- | ------------ |
| Range            | 100m         |
| Damage           | 70           |
| Spread Tolerance | 30%          |
| Motion Accuracy  | 0.9x (bonus) |

**By Nation:**

| Nation       | Weapons       | Mag Size  | Fire Rate | Notes             |
| ------------ | ------------- | --------- | --------- | ----------------- |
| **Soviet**   | PPSh-41       | 71 drum   | 900 rpm   | Highest capacity  |
|              | PPS-43        | 35 box    | 700 rpm   | More accurate     |
|              | PPD-40        | 71 drum   | 800 rpm   | Early war         |
| **German**   | MP40          | 32 box    | 500 rpm   | Very controllable |
|              | MP38          | 32 box    | 500 rpm   | Same as MP40      |
|              | MP28          | 32 box    | 500 rpm   | Early war         |
| **American** | M1A1 Thompson | 20/30 box | 700 rpm   | Heavy, accurate   |
|              | M3 Grease Gun | 30 box    | 450 rpm   | Most controllable |
| **British**  | Sten Mk.II    | 32 box    | 550 rpm   | Light, unreliable |
|              | Sten Mk.V     | 32 box    | 550 rpm   | Improved Sten     |
| **Finnish**  | Suomi KP/-31  | 71 drum   | 750 rpm   | Excellent quality |

## Bolt-Action Rifles Comparison

All bolt rifles use the same base pattern:

| Stat           | All Bolt Rifles |
| -------------- | --------------- |
| Range          | 180m            |
| Damage         | 110             |
| Fire Rate      | ~40 rpm         |
| Motion Penalty | 1.2x            |

**By Nation:**

| Nation       | Weapons                 | Mag Size | Notes                          |
| ------------ | ----------------------- | -------- | ------------------------------ |
| **Soviet**   | Mosin-Nagant M91/30     | 5        | Most common                    |
| **German**   | Kar98k                  | 5        | Excellent optics compatibility |
| **American** | M1903 Springfield       | 5        | Accurate                       |
|              | M1917 Enfield           | 6        | Higher capacity                |
| **British**  | Lee-Enfield No.1 Mk.III | 10       | Fast bolt action               |
|              | Lee-Enfield No.4 Mk.I   | 10       | Faster, more accurate          |
| **Finnish**  | Mosin-Nagant M39        | 5        | Improved accuracy              |

**British Advantage:** Lee-Enfield's 10-round magazine and fast bolt action allow trained soldiers to achieve higher practical fire rates.

## Semi-Automatic Rifles Comparison

| Nation       | Weapons           | Damage | Range | Mag Size | Notes                 |
| ------------ | ----------------- | ------ | ----- | -------- | --------------------- |
| **Soviet**   | SVT-40            | 110    | 155m  | 10       | Reliable              |
|              | AVS-36            | 110    | 155m  | 15       | Select-fire           |
| **German**   | Gewehr 43         | 110    | 155m  | 10       | Accurate              |
| **American** | M1 Garand         | 110    | 155m  | 8        | Fast reload (en-bloc) |
|              | M1 Carbine        | 70     | 130m  | 15       | Lightweight           |
|              | M1A1 Carbine      | 70     | 130m  | 15       | Folding stock         |
| **British**  | (Uses US weapons) | ------ | ----- | -------- | Lend-lease            |

## Machine Gun Comparison

| Nation       | Weapon      | Type | Range | Damage | Fire Rate | Notes          |
| ------------ | ----------- | ---- | ----- | ------ | --------- | -------------- |
| **Soviet**   | DP-28       | LMG  | 140m  | 110    | 550 rpm   | Pan magazine   |
|              | SG-43       | MMG  | 140m  | 110    | 700 rpm   | Belt fed       |
|              | DShK        | HMG  | 180m  | 220    | 600 rpm   | 12.7mm         |
| **German**   | MG34        | GPMG | 140m  | 110    | 900 rpm   | Very fast      |
|              | MG42        | GPMG | 140m  | 110    | 1200 rpm  | Fastest in war |
|              | MG131       | HMG  | 180m  | 220    | 900 rpm   | 13mm           |
| **American** | BAR         | LMG  | 155m  | 110    | 500 rpm   | Portable       |
|              | M1919A4     | MMG  | 140m  | 110    | 500 rpm   | Belt fed       |
|              | M2 Browning | HMG  | 180m  | 220    | 500 rpm   | .50 cal        |
| **British**  | Bren Mk.I   | LMG  | 140m  | 110    | 500 rpm   | Accurate       |
|              | Vickers     | MMG  | 140m  | 110    | 500 rpm   | Water cooled   |
|              | Vickers .50 | HMG  | 180m  | 220    | 500 rpm   | 12.7mm         |

**German Advantage:** MG42's 1200 rpm fire rate provides superior suppression.
**American Advantage:** BAR is more portable than other squad automatics.

## Sniper Rifle Comparison

| Nation       | Weapon         | Type | Range | Damage | Notes                 |
| ------------ | -------------- | ---- | ----- | ------ | --------------------- |
| **Soviet**   | Mosin PU       | Bolt | 200m  | 130    | Standard              |
|              | SVT-40 PU      | Semi | 180m  | 110    | Faster follow-up      |
| **German**   | Kar98k ZF39    | Bolt | 200m  | 130    | High magnification    |
|              | Kar98k ZF41    | Bolt | 200m  | 130    | Scout scope           |
|              | Gewehr 43 ZF4  | Semi | 180m  | 110    | Semi-auto             |
| **American** | M1903A4        | Bolt | 200m  | 130    | Standard              |
|              | M1C/M1D Garand | Semi | 180m  | 110    | Semi-auto             |
| **British**  | No.4 Mk.I (T)  | Bolt | 200m  | 130    | Excellent optics      |
| **Finnish**  | All variants   | Bolt | 200m  | 130    | White death tradition |

## Anti-Tank Rifle Comparison

| Nation      | Weapon          | Range | Armor Damage | Caliber | Notes              |
| ----------- | --------------- | ----- | ------------ | ------- | ------------------ |
| **Soviet**  | PTRD-41         | 160m  | 55           | 14.5mm  | Single shot        |
|             | PTRS-41         | 160m  | 55           | 14.5mm  | 5-round semi-auto  |
| **German**  | Panzerbüchse 39 | 160m  | 55           | 7.92mm  | Obsolete by '42    |
| **British** | Boys AT Rifle   | 160m  | 55           | .55 cal | Early war          |
| **Finnish** | Lahti L-39      | 160m  | 55           | 20mm    | Semi-auto, largest |

**Soviet Advantage:** 14.5mm has better penetration; PTRS allows rapid follow-up.
**Finnish Advantage:** Lahti L-39's 20mm can damage light vehicles effectively.

## Bazooka/RPG Comparison

| Nation       | Weapon          | Range | Penetration | Notes             |
| ------------ | --------------- | ----- | ----------- | ----------------- |
| **American** | M1 Bazooka      | 90m   | 80mm        | Early, 2.36"      |
|              | M9 Bazooka      | 90m   | 110mm       | Improved warhead  |
|              | M18 Recoilless  | 115m  | 90mm        | Crew-served       |
| **German**   | Panzerfaust 30  | 40m   | 200mm       | Disposable        |
|              | Panzerfaust 60  | 55m   | 200mm       | Extended range    |
|              | Panzerfaust 100 | 70m   | 220mm       | Latest model      |
|              | Panzerschreck   | 90m   | 160mm       | Reloadable        |
| **British**  | PIAT            | 90m   | 100mm       | Spring-powered    |
| **Soviet**   | RPG-6           | 25m   | 100mm       | Thrown AT grenade |

**German Advantage:** Panzerfaust has highest penetration and is disposable.
**American Advantage:** Reloadable bazookas provide sustained AT capability.

## Tank Gun Penetration Summary

Best-in-class by nation at 100m range:

| Nation       | Gun     | Caliber | Best AP (mm) | Best Premium (mm) |
| ------------ | ------- | ------- | ------------ | ----------------- |
| **German**   | KwK 43  | 88mm    | 219 (APCBC)  | 282 (APCR)        |
| **Soviet**   | D-25T   | 122mm   | 177 (APHE)   | 215 (APCBC)       |
| **American** | 90mm M3 | 90mm    | 163 (AP)     | 278 (HVAP)        |
| **British**  | 17-pdr  | 76.2mm  | 168 (APC)    | 226 (APDS)        |

**German Advantage:** KwK 43 combines high velocity with excellent penetration.
**Soviet Advantage:** 122mm has devastating post-penetration effects.
**American Advantage:** HVAP provides penetration parity with German 88mm.
**British Advantage:** APDS technology gives best velocity and penetration per caliber.

---

## How Accuracy Works in GoH

The game uses `radiusTable` to define accuracy spread at various distances:
- Lower values = more accurate
- Values represent the radius (in meters) where shots can land
- At range 0, accuracy is perfect (spread = 0)
- Spread increases with distance

### Example: Rifle Accuracy Curve
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

## FCRO Accuracy Philosophy

FCRO generally improves accuracy by:
1. Reducing spread values at each range bracket
2. Extending the effective range before accuracy degrades
3. Maintaining realistic relative accuracy between weapon types

## Spread Tolerance

`spreadTolerance` defines when AI will fire:
- Value of 0.3 = AI fires when 30% of shots will hit
- Higher values = AI fires earlier (less accurate)
- Lower values = AI waits for better shots

## AI Firing Timeout

`aiDistanceSpreadTimeout` controls how long AI waits before firing:
- `{distance% time}` format
- Longer timeouts at range = more careful aiming
- Shorter timeouts up close = faster reaction

## Damage Falloff

Many weapons use `FalloffMeter` to reduce damage at range:
- Damage starts decreasing at this distance
- `FalloffStrength` determines how quickly damage drops
- Example: SMG at 70m may do only 50% damage

## Burst Accuracy

`burstAccuracy` defines how accuracy degrades during sustained fire:
- First shot is most accurate
- Subsequent shots have increasing penalties
- Machine guns have lower penalties than rifles

---

# Weapon File Locations

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

# Document Version History

| Version | Date       | Changes                                                                                                                                                         |
| ------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1.0     | 2025-12-05 | Initial documentation - Infantry weapons, AT weapons, Flamethrowers, Mortars, Rockets, Tank guns                                                                |
| 1.1     | 2025-12-05 | Added complete accuracy curves, AI behavior parameters, flamethrower details, expanded tank gun section with Japanese/Finnish                                   |
| 2.0     | 2025-12-05 | Major expansion: Armor penetration tables, ammunition types, grenades/explosives, veterancy system, vehicle damage mechanics                                    |
| 2.5     | 2025-12-05 | Added Vision & Spotting System (human/vehicle/aircraft detection), comprehensive Faction Weapon Comparisons (SMGs, rifles, MGs, snipers, AT weapons, tank guns) |

---

*FCRO Complete Reference - Frontlines Combat Realism Overhaul*
*For Gates of Hell: Ostfront and Their Finest Hour DLC*