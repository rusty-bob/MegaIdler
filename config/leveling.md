The leveling configuration requires you to define the following additional properties:    

**Important:**  
If you decide to start any activity that requires fishing, make sure your character has enough gold to buy baits.  

**skill_type**:  
The type that should be leveled. Can be one of 
- "woodcutting"
- "mining"
- "cooking"
- "smelting"
- "fishing"
- "forge"
- "alchemy"

**batch_size**:  
the amount of items that the bot targets to craft.
(e.g. 100 Tin Bars, 100 Iron Swords, ...)


example `game.toml` addition:

```toml
# leveling mode configuration
[bot_modes.leveling]
skill_type = "smelting"      # Skill type. Check Skills.md
batch_size = 100             # Amount of items to craft in one turn (if possible). Not valid for infinite crafts (Ores, Logs)
```

example environment variables addition:
```env
SKILL_TYPE="smelting"
BATCH_SIZE="100"
```
