# Infantry Small Arms

This section covers all individual weapons carried by infantry units, including rifles, sniper rifles, submachine guns, machine guns, and pistols.

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

## See Also

- **[Quick Reference](quick-reference.md)** - Faction comparisons for infantry weapons
- **[Anti-Tank Weapons](anti-tank-weapons.md)** - Portable AT weapons
- **[Game Mechanics](game-mechanics.md)** - Accuracy system explained in detail
