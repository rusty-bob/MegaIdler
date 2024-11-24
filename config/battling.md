The leveling configuration requires you to define the following additional properties:    


**location_id**:  
The location where the bot should battle enemies. You can find a list of all available location ids [here](./../locations.md)

**stance**:  
battle stance. can be one of: 
- "BALANCED"
- "OFFENSIVE"
- "DEFENSIVE"
- "AGILE"
- "DEXTEROUS"

**food_id**:  
The type of food that should be brought to battle.  
 You can find a list of all available food ids [here](./../food.md)

**food_amount_carry**:  
The threshold amount of food (for the given id above) that the character must have in its inventory.  
If the actual amount is below the threshold, the bot will begin crafting it.

**food_amount_craft**:  
The amount of food (for the given id) that will be targeted to carft. Ideally this number is a multiple of `food_amount_carry`.  


example `game.toml` addition:

```toml
# battling mode configuration
[bot_modes.battling]
location_id = 1                  # Battle enemies at Bluebell Hollow
stance = "BALANCED"              # Balanced battle stance
food_id = 61                     # Bring Cooked Cod to the battle
food_amount_carry = 100          # Begin a battle if the bot has at least 100 Cooked Cod in his inventory
food_amount_craft = 500          # If the inventory amount of "Cooked Cod" falls below 100, the bot will craft up to 500 of it. 
```

example environment variables addition:
```env
LOCATION_ID="1"
STANCE="BALANCED"
FOOD_ID="61"
FOOD_AMOUNT_CARRY="100"
FOOD_AMOUNT_CRAFT="500"
```
