The crafting configuration requires you to define the following additional properties:    

**Important:**  
If you decide to start any activity that requires fishing, make sure your character has enough gold to buy baits.  


**skill_id**:  
The game of id of the desired skill. You can find a list of most available skill ids [here](./../skills.md)

**batch_amount**:  
the amount of items that the bot targets to craft.
(e.g. 100 Tin Bars, 100 Iron Swords, ...)

**use_crystal**:  
Whether or not the bot should use a enhancing crystal (**currently not enabled!**)

example `game.toml` addition:

```toml
# leveling mode configuration
[bot_modes.crafting]
skill_id = 10                  # Skill Id (e.g. Coal Ore in this case)
batch_amount = 100             # Amount of items to craft in one turn (if possible). Not valid for infinite crafts (Ores, Logs)
use_crystal = false            # Not reconsidered by the bot right now.
```

example environment variables addition:
```env
SKILL_ID=10
BATCH_AMOUNT="100"
USE_CRYSTAL=false
```
