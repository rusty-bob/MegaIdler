The headless version can be found as a docker image here: https://hub.docker.com/r/megaidler/headless

You can either mount a valid `game.toml` file or configure it through environment variables.

required env vars:
```
BOT_MODE: Leveling
EMAIL: youremail@google.com
PASSWORD: yourpassword
KEY: 3d2ca89d-ad25-4580-0000-c80a845cd487
SALT: gOfZSPhrVtrHnTPug6MlRhfoG6GsWD2B
```

Leveling env vars:
```
SKILL_TYPE: smelting
BATCH_SIZE: 100
```

crafting env vars:
```
SKILL_ID: 10
BATCH_AMOUNT: 100
USE_CRYSTAL: FALSE
```

sample leveling config
```yml
version: '3.8'

services:
  headless:
    image: megaidler/headless:latest
    environment:
      BOT_MODE: Leveling
      EMAIL: youremail@google.com
      PASSWORD: yourpassword
      KEY: 3d2ca89d-ad25-4580-0000-c80a845cd487
      SALT: GH13KJASDG9S9Fjgha65
      SKILL_TYPE: smelting
      BATCH_SIZE: 100
```
