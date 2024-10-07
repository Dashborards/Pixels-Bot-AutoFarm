# PixelsBot

PixelsBot is designed as an automated farm bot for an agriculture game. This bot automatically harvests, plants, waters and fertilizes the crops in the game. It also performs operations such as refilling energy and navigating the map.

## Features

- **Automatic Harvest**: Harvests mature plants.
- **Automatic Planting**: Plants new plants in empty areas.
- **Automatic Watering**: Water plants.
- **Automatic Fertilization**: Applies fertilizer to plants.
- **Energy Refill**: Fills by checking the energy level.
- **Map Navigation**: Navigate the map and reach specific areas.

## Requirements

- Operating System Windows 10 recommended

- Python 3.6 or high
- PyAutoGUI
- Pillow
- python-dotenv

## Installation

1. Clone the repository to a folder on your computer.

2. Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Create `config.txt` file and define the following variables:
    ```ini
    PLANT_TYPE=carrot
    START_MAP_WALK_DIR=down
    START_MAP_WALK_STEP=0.1
    WARP_NEAR_DECISION=150
    WARP_NEAR_STEP=0.3
    WARP_NEAR_TRY_LIMIT=100
    EMPTY_CONFIDENCE=0.6
    GROW1_CONFIDENCE=0.8
    GROW2_CONFIDENCE=0.8
    FULL_CONFIDENCE=0.75
    DRY_CONFIDENCE=0.75
    ROTTEN_CONFIDENCE=0.75
    ROTTEN2_CONFIDENCE=0.8
    FERTILIZE_CONFIDENCE=0.9
    WARP_CONFIDENCE=0.7
    AVATAR_CONFIDENCE=0.9
    AVATAR2_CONFIDENCE=0.9
    REFILL_AMOUNT_PER_MAP=10
    WAIT_DURATION_AFTER_WARP=10
    WAIT_DURATION_AFTER_WATER=0
    MOVEMENT_DURATION=1
    RANDOM_CLICK_SIZE=5
    WALK_TO_ENABLED=0
    KEY_SHORTCUT_ENABLED=0
    KEY_SHORTCUT_WATERING=1
    KEY_SHORTCUT_SCISSOR=2
    KEY_SHORTCUT_SEED=3
    KEY_SHORTCUT_FRUIT=4
    KEY_SHORTCUT_FERTILIZE=5
    ```


**Notes:**
- You need to walk your avatar close enough to the farm area (currently the bot does not automatically walk to farm areas).

## Usage

Use the following command to run the bot:
```bash
python pixels.py
```
(This step requires the game to be full screen).

The bot will automatically perform the specified actions.

Note: If the bot is not working correctly, adjust the configurations in the `config.txt` file to make it suitable for your screen. You may need to try this several times.


## Configuration

Default configurations are set for the Default display, but you can adjust the values in the `config.txt` file to suit your display.

--------------------------------------
- Name: **PLANT_TYPE**
- Description: Type of plant to be used
- Type: Option
- Default: popberry
- Options: popberry, carrot, butterberry, grainbow
--------------------------------------
- Name: **START_MAP_WALK_DIR**
- Description: Direction to move when starting a new map
- Type: Option
- Default: down
- Options: down, up, left, right
--------------------------------------
- Name: **START_MAP_WALK_STEP**
- Description: Number of seconds to walk initially on a new map
- Type: Second
- Default: 0.1
--------------------------------------
- Name: **WARP_NEAR_DECISION**
- Description: Number of screen pixels to determine if near a warp point
- Type: Pixel
- Default: 150
--------------------------------------
- Name: **WARP_NEAR_STEP**
- Description: Number of seconds to walk on each attempt to reach a warp point
- Type: Second
- Default: 0.3
--------------------------------------
- Name: **WARP_NEAR_TRY_LIMIT**
- Description: Maximum number of attempts to reach a warp point
- Type: Number
- Default: 100
--------------------------------------
- Name: **EMPTY_CONFIDENCE**
- Description: Matching percentage required to find empty space on the screen
- Type: Percentage
- Default: 0.6
--------------------------------------
- Name: **GROW1_CONFIDENCE**
- Description: Matching percentage required to find growth stage 1 image on the screen
- Type: Percentage
- Default: 0.8
--------------------------------------
- Name: **GROW2_CONFIDENCE**
- Description: Matching percentage required to find growth stage 2 image on the screen
- Type: Percentage
- Default: 0.8
--------------------------------------
- Name: **FULL_CONFIDENCE**
- Description: Matching percentage required to find fully grown plant image on the screen
- Type: Percentage
- Default: 0.75
--------------------------------------
- Name: **DRY_CONFIDENCE**
- Description: Matching percentage required to find dried plant image on the screen
- Type: Percentage
- Default: 0.75
--------------------------------------
- Name: **ROTTEN_CONFIDENCE**
- Description: Matching percentage required to find rotten plant image on the screen
- Type: Percentage
- Default: 0.8
--------------------------------------
- Name: **ROTTEN2_CONFIDENCE**
- Description: Matching percentage required to find second rotten plant image on the screen
- Type: Percentage
- Default: 0.9
--------------------------------------
- Name: **FERTILIZE_CONFIDENCE**
- Description: Matching percentage required to find fertilize image on the screen
- Type: Percentage
- Default: 0.9
--------------------------------------
- Name: **WARP_CONFIDENCE**
- Description: Matching percentage required to find warp point image on the screen
- Type: Percentage
- Default: 0.7
--------------------------------------
- Name: **AVATAR_CONFIDENCE**
- Description: Matching percentage required to find avatar image on the screen
- Type: Percentage
- Default: 0.9
--------------------------------------
- Name: **AVATAR2_CONFIDENCE**
- Description: Matching percentage required to find second avatar image on the screen
- Type: Percentage
- Default: 0.9
--------------------------------------
- Name: **REFILL_AMOUNT_PER_MAP**
- Description: Specifies how many times energy will be refilled per map
- Type: Number
- Default: 10
--------------------------------------
- Name: **WAIT_DURATION_AFTER_WARP**
- Description: Waiting time after warp
- Type: Second
- Default: 10
--------------------------------------
- Name: **WAIT_DURATION_AFTER_WATER**
- Description: Waiting time after watering
- Type: Second
- Default: 60
--------------------------------------
- Name: **MOVEMENT_DURATION**
- Description: Time taken to move the mouse from one position to another (For smooth movement)
- Type: Second
- Default: 0.3
--------------------------------------
- Name: **RANDOM_CLICK_SIZE**
- Description: Slightly randomizes the click position to prevent bot detection
- Type: Pixel
- Default: 5
--------------------------------------
- Name: **WALK_TO_ENABLED**
- Description: Enable walking to target (planting, watering, harvesting, fertilizing)
- Type: Enable
- Default: 0
- Options: 0, 1
--------------------------------------
- Name: **KEY_SHORTCUT_ENABLED**
- Description: Enable using keyboard shortcuts to select tools (Makes these actions faster but requires specific configuration)
- Type: Enable
- Default: 0
- Options: 0, 1
--------------------------------------
- Name: **KEY_SHORTCUT_WATERING**
- Description: Shortcut key for watering can (Position of watering can in your inventory)
- Type: Number
- Default: 1
- Options: 1-6
--------------------------------------
- Name: **KEY_SHORTCUT_SCISSOR**
- Description: Shortcut key for scissors (Position of scissors in your inventory)
- Type: Number
- Default: 2
- Options: 1-6
--------------------------------------
- Name: **KEY_SHORTCUT_SEED**
- Description: Shortcut key for seed (Position of seed in your inventory)
- Type: Number
- Default: 3
- Options: 1-6
--------------------------------------
- Name: **KEY_SHORTCUT_FRUIT**
- Description: Shortcut key for fruit (Position of fruit in your inventory)
- Type: Number
- Default: 4
- Options: 1-6
--------------------------------------
- Name: **KEY_SHORTCUT_FERTILIZE**
- Description: Shortcut key for fertilizer tool (Position of fertilizer in your inventory)
- Type: Number
- Default: 5
- Options: 1-6
--------------------------------------
## Example

https://github.com/PPixMans/Pixels-Bot-AutoFarm/assets/170432730/04d61d2d-c646-42ae-8384-79f6f886544a

## Warning

Please be careful and follow the rules when using the boat. Recommended for educational use.

## Contribution

Leave a star in the repo to contribute

## License

This project is licensed under the MIT license. See the `LICENSE` file for more information.
