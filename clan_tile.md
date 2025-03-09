
# Clan Tile Commands (`/clan tile`)

### 1. `/clan tile claim`
**Description:** Claims an unoccupied tile for the clan.

**Options:**
- `tile` *(String, Required)*: Tile coordinates (e.g., `b3`).

**Permissions:** General and Lieutenant of the clan only.

---

### 2. `/clan tile scout`
**Description:** Scouts an enemy tile (Only scouts can do this). Has a 50% fail rate, at which point the clan receiveds a 12 hour cooldown before any scouts can scout again.

**Options:**
- `tile` *(String, Required)*: Tile coordinates to scout.

**Permissions:** Scout only.

---

### 3. `/clan tile upgrade`
**Description:** Opens the upgrade menu for one of the clans tiles. Allows you to purchase upgrades such as defense boosts or tax income boosts.

**Options:**
- `tile` *(String, Required)*: Tile coordinates to upgrade. (must be your clans tile)

**Permissions:** General, Lieutenant, and Mechanic only.

---

### 4. `/clan tile stats`
**Description:** Returns the stats of the provided tile.

**Options:**
- `tile` *(String, Required)*: Tile coordinates to get the stats of. 

**Permissions:** Anyone, however stats may differ between generals / non generals.

---