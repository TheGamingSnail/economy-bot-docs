
# KOT4 (Kidneys of Titanium Quatro) Bot - Command Documentation

This document provides an in-depth breakdown of all commands available in the KOT4 bot. The bot features a clan system where users can create, join, and manage clans, as well as apply for jobs within their clans. Below are the available commands and their descriptions.

---

## Clan Commands (`/clan`)

### 1. `/clan create`
**Description:** Creates a new clan. Clans are required for most commands, so this is a good place to start.

**Options:**
- `clan-name` *(String, Required)*: The name of the clan.
- `ideology` *(String, Required)*: The political ideology of the clan. Choices:
  - Democracy
  - Communism
  - Authoritarian
  - Monarchy
- `starting-tile` *(String, Required)*: The map location where the clan will start (e.g., `a1`, `b2`).
- `color` *(String, Required)*: The hex code for the clan's map color.

**Permissions:** None required.

---

### 2. `/clan join`
**Description:** Allows a user to join an existing clan.

**Options:**
- `clan-name` *(String, Required)*: The name of the clan the user wishes to join.

---

### 3. `/clan leave`
**Description:** Leaves the user's current clan.

---

### 4. `/clan deposit`
**Description:** Deposits money into the clans funds. This money is taken directly from the users UnbelievaBoat balance.

**Options:**
- `amount` *(Integer, Required)*: The amount to deposit.

---

### 5. `/clan withdraw`
**Description:** Withdraws money from the clan's funds (general only).

**Options:**
- `amount` *(Integer, Required)*: The amount to withdraw.

**Permissions:** General of the clan only.

---

### 6. `/clan union`
**Description:** Combines the users clan and the given clan into one clan, keeping the original users clan name as the name for the entire clan.

**Options:**
- `clan-name` *(String, Required)*: The clan you wish to create a union with.

**Permissions:** General of the clan only.

---

### 7. `/clan stats`
**Description:** Returns the stats of the users clan (if `clan-name` is not provied) or the requested clan.

**Options:**
- `clan-name` *(String, Optional)*: The clan which you wish to see the stats of.

**Permissions:** Any user, however the stats may differ between generals / non generals.


## Clan Army Commands (`/clan army`)

### 8. `/clan army send-force`
**Description:** Stations troops on a specific tile. Useful for defending your territory or preparing for an invasion. Can only be used on your own tiles.

**Options:**
- `tile` *(String, Required)*: The tile to station troops on.
- `rifleman-amount`, `bayonet-amount`, `suicide-bomber-amount`, `grenadier-amount`, `tank-amount`, `apc-amount`, `artillery-amount`, `landmine-amount` *(Integer, Optional)*: Number of each troop type to send.

**Permissions:** General and Lieutenant of the clan only.

---

### 9. `/clan army return-force`
**Description:** Withdraws troops from a tile. Can only be used on your own tiles.

**Options:**
- `tile` *(String, Required)*: The tile to withdraw from.
- (Same troop options as `send-force`)

**Permissions:** General and Lieutenant of the clan only.

---

### 10. `/clan army battle`
**Description:** Initiates a battle between two clans for control of a tile. The clan running the command is considered the attacking clan, therefore the troops of said clan get attacking bonuses, while the clan which controls the tile being fought for receives defending bonuses. The troops required to attack must come from only 1 tile. The battle outcome is decided by the strengths of all forces sent + bonuses.

**Options:**
- `defending-tile` *(String, Required)*: The tile being attacked.
- `attacking-tile` *(String, Required)*: The tile from which the attack originates.

**Permissions:** General and Lieutenant of the clan only.

---
### 11. `/clan army list`
**Description:** Lists all tiles that contain units belonging to the user's clan.

**Permissions:** General and Lieutenant of the clan only.

---

### 12. `/clan army return-all`
**Description:** Returns all troops from all tiles owned by the user's clan.

**Permissions:** General and Lieutenant of the clan only.

---

### 13. `/clan army border`
**Description:** Sets up a defensive border against a neighboring clan. This command evenly splits the provided troop amounts across every tile which is adjacent to the enemy clan. If the troops cannot be split evenly, each leftover troop type is randomly placed on one of the tiles.

**Options:**
- `clan-name` *(String, Required)*: Name of the clan to establish the border with.
- Various troop types (`rifleman-amount`, `bayonet-amount`, etc.) as optional integer inputs.

**Permissions:** General and Lieutenant of the clan only.

---

### 14. `/clan send-aid`
**Description:** Sends aid in the form of troops to another clan.

**Options:**
- `clan-name` *(String, Required)*: The exact name of the clan receiving aid.
- Various troop types (`rifleman-amount`, `bayonet-amount`, etc.) as optional integer inputs.

**Permissions:** General and Lieutenant of the clan only.

---

## Clan Tile Commands (`/clan tile`)

### 15. `/clan tile claim`
**Description:** Claims an unoccupied tile for the clan.

**Options:**
- `tile` *(String, Required)*: Tile coordinates (e.g., `b3`).

**Permissions:** General and Lieutenant of the clan only.

---

### 16. `/clan tile scout`
**Description:** Scouts an enemy tile (Only scouts can do this). Has a 50% fail rate, at which point the clan receiveds a 12 hour cooldown before any scouts can scout again.

**Options:**
- `tile` *(String, Required)*: Tile coordinates to scout.

**Permissions:** Scout only.

---

### 17. `/clan tile upgrade`
**Description:** Opens the upgrade menu for one of the clans tiles. Allows you to purchase upgrades such as defense boosts or tax income boosts.

**Options:**
- `tile` *(String, Required)*: Tile coordinates to upgrade. (must be your clans tile)

**Permissions:** General, Lieutenant, and Mechanic only.

---

### 18. `/clan tile stats`
**Description:** Returns the stats of the provided tile.

**Options:**
- `tile` *(String, Required)*: Tile coordinates to get the stats of. 

**Permissions:** Anyone, however stats may differ between generals / non generals.

---
## Clan Mechanic Commands (`/clan army`)

### 19. `/clan mechanic upgrade`
**Description:** Allows a **mechanic** job role to upgrade a troop type, increasing its strength.

**Permissions:** Mechanic only.

---

## Clan Talent Point Commands (`/clan talent_points`)

### 20. `/clan talent_points claim`
**Description:** Claim talent points for your clan. Your contribution will be included in the calculation that gives out talent points at 12:00PM GMT.

---

### 21. `/clan talent_points use`
**Description:** Opens the menu for using talent points to upgrade your clan. Talent points can be spent on attack bonuses, defense bonuses, and tax bonuses.

**Options:**
- `tile` *(String, Required)*: Tile coordinates to upgrade. (must be your clans tile)

**Permissions:** General and Lieutenant only.

---

## Miscellaneous Commands

### 22. `/clan misceallaneous stats_menu`
**Description:** Displays game statistics, including unit strength, prices, and terrain bonuses.

--- 

### 23. `/clan settings color`
**Description:** Changes the clans color on the map to a new color.

**Options:**
- `new-color` *(String, Required)*: The new hex color you want to be displayed on the map.

**Permissions:** General of the clan only.

---

## Job Commands (`/job`)

### 1. `/job apply`
**Description:** Applies for a job within the user's clan. Jobs have different perks/abilities.

**Options:**
- `job_type` *(String, Required)*: The job to apply for. Choices:
  - `farmer`
  - `lieutenant`
  - `propagandist`
  - `delegate`
  - `scout`
  - `mechanic`

---

### 2. `/job quit`
**Description:** Resigns from the user's current job.

---

### 3. `/job application accept`
**Description:** Accepts a job application (general only).

**Options:**
- `applicant` *(User, Required)*: The user to accept.

**Permissions:** General of the clan only.

---

### 4. `/job application deny`
**Description:** Denies a job application (general only).

**Options:**
- `applicant` *(User, Required)*: The user to deny.

**Permissions:** General of the clan only.

---


## Automated Features

### Daily Talent Points Distribution
- Talent points are distributed daily at 12:00 PM GMT based on member participation. Member participation is counted based on how many clan members ran `/clan talent_points claim`, which is then used as a percentage of the total clan members to figure out how many talent points to give out. The max amount of talent points a clan can receive at once is 5.

### Elections
- Elections automatically recur every 7 days if a general is removed.

### Battle System
- Includes troop strength calculations, tile bonuses, and random casualties.

---

## Notes
- Most commands require the user to be in a clan.
- Only the general can manage job applications and withdraw clan funds.
- Tile ownership and battle mechanics follow predefined rules.

This documentation provides a complete overview of the KOT4 bot's functionality.

