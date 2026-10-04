# Devotions
Embrace the Powers of the Divine!
Devotions is a Minecraft plugin that allows players to worship various deities, gain favor, and unlock divine powers. Embark on a spiritual journey, perform rituals, and rise through the ranks of devout followers. This plugin aims to be highly customizeable so you can create your own deities for players to worship, as well as your own rituals!

# Features
**Deity Worship:** Players can choose to worship different deities, each with configurable lore and details.<br>
**Favor System:** Gain or lose favor with your deity based on your actions.<br>
**Rituals and Offerings:** Perform rituals and make offerings to please your deity.<br>
**Dynamic Blessings and Curses:** Receive blessings or curses based on your level of favor.<br>
**Shrines/Altars:** Dedicate shrines to your chosen deity.<br>
**PlaceholderAPI Support:** Integrate with other plugins using custom placeholders.<br>
**Configurable Sounds:** Customizeable sounds.yml for certain events

https://www.spigotmc.org/resources/devotions-deities-and-blessings-⛧†.113549/


## About this fork

This fork is based on [xIdentified/Devotions](https://github.com/xIdentified/Devotions). Changes:

- **Updated to Minecraft 1.21.4**, tested on Spigot and Paper.
- **Per-deity settings** ([upstream issue #6](https://github.com/xIdentified/Devotions/issues/6)). Each deity in `deities.yml` can override the global favor settings, so some gods are harder to please than others. Any key you leave out falls back to the value in `config.yml`.

  ```yaml
  deities:
    gaia:
      blessing-threshold: 120   # favor needed for blessings
      curse-threshold: 20       # favor below which curses start
      miracle-threshold: 190    # favor needed for miracles
      blessing-chance: 0.5
      curse-chance: 0.05
      miracle-chance: 0.04
      favor-decay-rate: 3
      initial-favor: 70         # favor a new follower starts with
      max-favor: 200
      personality: "generous"
  ```

- **Deity personalities** change how favor gains and losses are applied:

  | Personality | Effect |
  |-------------|--------|
  | `vengeful` | Favor losses ×1.5 |
  | `forgiving` | Favor losses ×0.7 |
  | `generous` | Favor gains ×1.3 |
  | `demanding` | Favor gains ×0.8 |
  | `neutral` | No change (default) |

- **`/deitydiff <list|info> [deity]`** (aliases `/ddifficulty`, permission `devotions.admin`) shows each deity's difficulty settings in game.
