
# Clan Army Commands (`/clan army`)

### 1. `/clan army send-force`
**Description:** Stations troops on a specific tile. Useful for defending your territory or preparing for an invasion. Can only be used on your own tiles.

**Options:**
- `tile` *(String, Required)*: The tile to station troops on.
- `rifleman-amount`, `bayonet-amount`, `suicide-bomber-amount`, `grenadier-amount`, `tank-amount`, `apc-amount`, `artillery-amount`, `landmine-amount` *(Integer, Optional)*: Number of each troop type to send.

**Permissions:** General and Lieutenant of the clan only.

---

### 2. `/clan army return-force`
**Description:** Withdraws troops from a tile. Can only be used on your own tiles.

**Options:**
- `tile` *(String, Required)*: The tile to withdraw from.
- (Same troop options as `send-force`)

**Permissions:** General and Lieutenant of the clan only.

---

### 3. `/clan army battle`
**Description:** Initiates a battle between two clans for control of a tile. The clan running the command is considered the attacking clan, therefore the troops of said clan get attacking bonuses, while the clan which controls the tile being fought for receives defending bonuses. The troops required to attack must come from only 1 tile. The battle outcome is decided by the strengths of all forces sent + bonuses.

**Options:**
- `defending-tile` *(String, Required)*: The tile being attacked.
- `attacking-tile` *(String, Required)*: The tile from which the attack originates.

**Permissions:** General and Lieutenant of the clan only.

---
### 4. `/clan army list`
**Description:** Lists all tiles that contain units belonging to the user's clan.

**Permissions:** General and Lieutenant of the clan only.

---

### 5. `/clan army return-all`
**Description:** Returns all troops from all tiles owned by the user's clan.

**Permissions:** General and Lieutenant of the clan only.

---

### 6. `/clan army border`
**Description:** Sets up a defensive border against a neighboring clan. This command evenly splits the provided troop amounts across every tile which is adjacent to the enemy clan. If the troops cannot be split evenly, each leftover troop type is randomly placed on one of the tiles.

**Options:**
- `clan-name` *(String, Required)*: Name of the clan to establish the border with.
- Various troop types (`rifleman-amount`, `bayonet-amount`, etc.) as optional integer inputs.

**Permissions:** General and Lieutenant of the clan only.

---

### 7. `/clan send-aid`
**Description:** Sends aid in the form of troops to another clan.

**Options:**
- `clan-name` *(String, Required)*: The exact name of the clan receiving aid.
- Various troop types (`rifleman-amount`, `bayonet-amount`, etc.) as optional integer inputs.

**Permissions:** General and Lieutenant of the clan only.

---
