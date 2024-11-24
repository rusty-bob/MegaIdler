*The bot will read the configuration during startup and indefinitely work on the specific task.  
Any configuration updates require a bot restart to apply the changes.*

Configuration can provided by either placing a `game.toml` file next to the executable or by providing them as environment variables.  
You can find the **most basic** configuration below, but still need to configure the specific bot mode (you can find a fully runnable configuration in the respective mode documentations).

Example file
```toml
# bot mode. Either 'Crafting', 'Leveling' or 'Battling'
active_mode = "Crafting"

# idle mmo login details
[authentication.game]
email = "email@gmail.com"
password = "yourpasswordhere"

# megaidler license details
[authentication.license]
key = "3d2ca89d-ad25-4580-a008-c80a845cd485"    # your personal license key
salt = "gOfZSPhrVtrHnTPug6MlRhfoG6GsWD2B"       # a random string. define it once, but do not change it afterwards!
```

example environment variables:
```env
BOT_MODE="Leveling"
EMAIL="email@gmail.com"
PASSWORD="yourpasswordhere"
KEY="3d2ca89d-ad25-4580-a008-c80a845cd485"
SALT="gOfZSPhrVtrHnTPug6MlRhfoG6GsWD2B"
```
