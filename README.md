
# Clan Commands (`/clan`)

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

