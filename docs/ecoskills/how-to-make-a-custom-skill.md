---
title: "How to make a custom skill"
sidebar_position: 7
---

## Default config
The default configs can be found here:

[GitHub](https://github.com/Auxilor/EcoSkills/blob/master/eco-core/core-plugin/src/main/resources/customskills/)

## How to add custom skills
Custom skills are each config files placed in the `/customskills/` folder, and you can add or remove them as you please. There's an example config called `_example.yml` to help you out!

### Example Custom Skill Config

```yaml
name: "Building" # The name of the skill, to be shown to players
description: "Place blocks to earn Building XP" # The skill description
disabled-in-worlds: [ ] # World names for this skill to not gain xp in

# Add more levels if you want
level-xp-requirements:
  - 25
  - 60
  - 100
  - 150
  - 250
  - 375
  - 500
  - 750
  - 1000
  - 1750
  - 2500
  - 3750
  - 5000
  - 7500
  - 10000
  - 15000
  - 25000
  - 37500
  - 50000
  - 100000
  - 150000
  - 200000
  - 250000
  - 300000
  - 350000
  - 400000
  - 450000
  - 500000
  - 550000
  - 600000
  - 650000
  - 700000
  - 750000
  - 800000
  - 850000
  - 900000
  - 950000
  - 1000000
  - 1050000
  - 1100000
  - 1150000
  - 1200000
  - 1250000
  - 1300000
  - 1375000
  - 1450000
  - 1550000
  - 1700000
  - 1850000
  - 2000000
  - 2500000

gui:
  name: "Building"
  item: 'player_head texture:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMTQ4Yjg5YjFhYTk4OGRhODc4MDA0ODhjMzcyNjBhYTg5OGQyYzA3YWM4NmMwOTljNDQ5NGZjMGY0ZjBkY2NhMiJ9fX0='
  position:
    row: 4
    column: 5
  lore:
    - "&fImproves Stats:"
    - "&8» &r%ecoskills_attack_speed_name%"
    - "&8» &r%ecoskills_defense_name%"

rewards:
  # The actual rewards to be given
  rewards:
    - "attack_speed::2"
    - "defense::1"

  level-commands: [ ]

  # The chat messages to send on level up
  chat-messages:
    1:
      - " &8» &r&f+2 %ecoskills_attack_speed_name%"
      - " &8» &r&f+1 %ecoskills_defense_name%"
    10:
      - " &8» &r&f+2 %ecoskills_attack_speed_name%"
      - " &8» &r&f+1 %ecoskills_defense_name%"

  # The lore to show in the levels gui
  progression-lore:
    1:
      - " &8» &r&f+2 %ecoskills_attack_speed_name%"
      - " &8» &r&f+1 %ecoskills_defense_name%"
    10:
      - " &8» &r&f+2 %ecoskills_attack_speed_name%"
      - " &8» &r&f+1 %ecoskills_defense_name%"


# An XP Gain method takes a trigger, a multiplier, conditions, and filters.
# The multiplier takes the value produced by the trigger and multiplies it
# by some value to calculate the experience that should be given
xp-gain-methods:
  - trigger: place_block
    multiplier: 1.5
    conditions: [ ]
```
