
# KOT4 (Kidneys of Titanium Quatro) Bot - Command Documentation

This document provides an in-depth breakdown of all commands available in the KOT4 bot. The bot features a clan system where users can create, join, and manage clans, as well as apply for jobs within their clans. Below are the available commands and their descriptions.

---

## Clan Commands (`/clan`)

### 1. `/clan create`
**Description:** Creates a new clan.

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
- `clan-name` *(String, Required)*: The name of the clan to join.

---

### 3. `/clan leave`
**Description:** Leaves the user's current clan.

---

### 4. `/clan deposit`
**Description:** Deposits money into the clan's funds.

**Options:**
- `amount` *(Integer, Required)*: The amount to deposit.

---

### 5. `/clan withdraw`
**Description:** Withdraws money from the clan's funds (general only).

**Options:**
- `amount` *(Integer, Required)*: The amount to withdraw.

**Permissions:** General of the clan only.

---

### 6. `/clan army send-force`
**Description:** Sends troops to defend a specific tile.

**Options:**
- `tile` *(String, Required)*: The tile to defend.
- `rifleman-amount`, `bayonet-amount`, `suicide-bomber-amount`, `grenadier-amount`, `tank-amount`, `apc-amount`, `artillery-amount`, `landmine-amount` *(Integer, Optional)*: Number of each troop type to send.

---

### 7. `/clan army return-force`
**Description:** Withdraws troops from a defended tile.

**Options:**
- `tile` *(String, Required)*: The tile to withdraw from.
- (Same troop options as `send-force`)

---

### 8. `/clan battle`
**Description:** Initiates a battle between two clans for control of a tile.

**Options:**
- `defending-tile` *(String, Required)*: The tile being attacked.
- `attacking-tile` *(String, Required)*: The tile from which the attack originates.

---

### 9. `/clan send-aid`
**Description:** Sends aid in the form of troops to another clan.

**Options:**
- `clan-name` *(String, Required)*: The exact name of the clan receiving aid.
- Various troop types (`rifleman-amount`, `bayonet-amount`, etc.) as optional integer inputs.

---

### 10. `/clan list`
**Description:** Lists all tiles that contain units belonging to the user's clan.

---

### 11. `/clan return-all`
**Description:** Returns all troops from all tiles owned by the user's clan.

---

### 12. `/clan border`
**Description:** Sets up a defensive border against a neighboring clan.

**Options:**
- `clan-name` *(String, Required)*: Name of the clan to establish the border with.
- Various troop types (`rifleman-amount`, `bayonet-amount`, etc.) as optional integer inputs.

---

### 13. `/clan tile claim`
**Description:** Claims an unoccupied tile for the clan.

**Options:**
- `tile` *(String, Required)*: Tile coordinates (e.g., `b3`).

---

### 14. `/clan scout`
**Description:** Scouts an enemy tile (Only scouts can do this).

**Options:**
- `tile` *(String, Required)*: Tile coordinates to scout.

---

### 15. `/clan upgrade`
**Description:** Opens the upgrade menu for a tile.

**Options:**
- `tile` *(String, Required)*: Tile coordinates to upgrade.

---

### 16. `/clan mechanic upgrade`
**Description:** Allows a **mechanic** job role to upgrade a troop type, increasing its strength.

---

## Job Commands (`/job`)

### 1. `/job apply`
**Description:** Applies for a job within the user's clan.

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

## Miscellaneous Commands

### 1. `/clan misceallaneous stats_menu`
**Description:** Displays game statistics, including unit strength, prices, and terrain bonuses.

---

## Automated Features

### Daily Talent Points Distribution
- Talent points are distributed daily at 12:00 PM GMT based on member participation.

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

