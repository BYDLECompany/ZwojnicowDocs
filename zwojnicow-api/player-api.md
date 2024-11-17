---
icon: person
cover: ../.gitbook/assets/Zrzut ekranu 2024-11-17 140434.png
coverY: 0
---

# Player API

### Player Class

The `Player` class represents a player entity with attributes and methods to interact with items.

#### Properties

* `name`: A string representing the player's name.

### DunHeroItem Enum

`DunHeroItem` enumerates a comprehensive list of possible items that a player can receive. Items include:

* **Rings:** Dash Ring, Death Necklace, Dexterity Necklace, etc.
* **Armor:** Dragon Armor, Golden Armor, Leather Armor, etc.
* **Potions:** Healing Potion, Strength Potion, Dexterity Potion, etc.
* **Weapons:** Barbarian Axe, Hero Sword, Iron Dagger, etc.
* **Bows and Ranged Weapons:** Arcane Tracker Bow, Bone Bow, Fire Boomerang, etc.

Each category includes unique items that enhance or affect player abilities.

### Methods

#### `player.GiveItem(item)`

* **Parameters:**
  * `item`: An instance of `DunHeroItem` representing the item to be given to the player.
* **Source:** Defined in `definitions/Player.lua`

This function is used to grant a specified item to the player, enriching gameplay by augmenting player skills or capabilities.

### LocalPlayer Instance

* `localPlayer` An instance of the `Player` class utilized for in-game actions and management.
