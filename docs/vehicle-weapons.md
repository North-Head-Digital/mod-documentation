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

## See Also

- **[Reference Tables](reference-tables.md)** - Detailed armor penetration values by gun type
- **[Quick Reference](quick-reference.md)** - Tank gun penetration summary by nation
- **[Anti-Tank Weapons](anti-tank-weapons.md)** - Portable AT weapons
- **[Game Mechanics](game-mechanics.md)** - Vehicle damage system
