# Anti-Tank Weapons

This section covers all portable anti-tank weapons carried by infantry, including anti-tank rifles, bazookas, panzerfausts, and rifle grenade launchers.

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

## See Also

- **[Quick Reference](quick-reference.md)** - Faction comparisons for AT weapons
- **[Infantry Weapons](infantry-weapons.md)** - Small arms
- **[Vehicle Weapons](vehicle-weapons.md)** - Tank guns and penetration values
- **[Reference Tables](reference-tables.md)** - Armor penetration data
