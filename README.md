# FCRO Documentation

Official documentation for **Frontlines Combat Realism Overhaul (FCRO)**, a comprehensive realism modification for Gates of Hell: Ostfront and Their Finest Hour DLC.

## About FCRO

FCRO is a total combat realism overhaul that fundamentally transforms Gates of Hell by:

- **Extended Weapon Ranges**: 20-50% increases to match historical capabilities
- **Increased Lethality**: More decisive and realistic combat outcomes
- **Enhanced Accuracy**: Improved accuracy curves with proper degradation
- **Realistic Penetration**: Historical armor penetration values
- **Improved AI**: Smarter firing behavior and tactics
- **Advanced Systems**: Vehicle damage, veterancy, and spotting mechanics

## Documentation

This repository contains the complete technical documentation for FCRO, built with MkDocs and the Material theme.

### Building the Documentation

**Prerequisites:**
- Python 3.7+
- pip

**Setup:**
```bash
# Clone the repository
git clone <repository-url>
cd mod-documentation

# Install dependencies
pip install -r requirements.txt

# Serve locally
mkdocs serve

# Build static site
mkdocs build
```

**View locally:**
Navigate to `http://127.0.0.1:8000` after running `mkdocs serve`

## Documentation Structure

```
docs/
├── index.md                    # Homepage and introduction
├── getting-started.md          # Installation and quick start guide
├── quick-reference.md          # At-a-glance weapon comparisons
├── infantry-weapons.md         # Small arms documentation
├── anti-tank-weapons.md        # Portable AT weapons
├── artillery-and-mortars.md    # Indirect fire weapons
├── vehicle-weapons.md          # Tank guns and artillery
├── reference-tables.md         # Penetration and ammunition data
└── game-mechanics.md           # Systems and mechanics
```

## Key Features

### Weapons Coverage

- **Infantry Small Arms**: Rifles, sniper rifles, SMGs, machine guns, pistols
- **Anti-Tank Weapons**: AT rifles, bazookas, panzerfausts, rifle grenades
- **Support Weapons**: Flamethrowers, mortars, rocket artillery
- **Vehicle Weapons**: Tank guns, artillery pieces, mounted weapons

### Game Systems

- **Veterancy System**: Skill-based progression with accuracy bonuses
- **Vehicle Damage**: Realistic penetration and crew casualty mechanics
- **Vision & Spotting**: Detection ranges and concealment
- **Accuracy Curves**: Weapon-specific spread and falloff

### Reference Data

- Comprehensive armor penetration tables by gun and range
- Ammunition type comparisons (AP, APCR, HEAT, APDS, etc.)
- Faction-specific weapon comparisons
- Explosive blast radius data

## Factions Covered

- 🇩🇪 Germany (Wehrmacht, Waffen-SS)
- 🇷🇺 Soviet Union (Red Army)
- 🇺🇸 United States (US Army)
- 🇬🇧 Great Britain (British Commonwealth)
- 🇯🇵 Japan (Imperial Japanese Army)
- 🇫🇮 Finland (Finnish Defense Forces)

## Version

**Current Documentation Version:** 2.5 (December 2025)

See [CHANGELOG.md](CHANGELOG.md) for version history.

## Contributing

Contributions to documentation are welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This documentation is provided for the FCRO mod community. Check with mod authors for specific licensing terms.

## Links

- **Mod Home**: [TBD - Add Steam Workshop or mod page link]
- **Community**: [TBD - Add Discord or forum link]
- **Bug Reports**: [TBD - Add issue tracker link]

---

*For Gates of Hell: Ostfront and Their Finest Hour DLC*
*Documentation built with MkDocs and Material for MkDocs*
