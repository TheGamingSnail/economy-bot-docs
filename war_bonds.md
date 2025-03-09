
# War bonds (`/clan bond`)
---
Clans have the ability to issue war bonds, which any other clan can take. This loans money to the receiving clan, while after a certain amount of time the issuing clan gets their money returned (Either by the receiving clan paying back their bonds, or by the money being forcefully removed once the term is up).

---

### 1. `/clan bond issue`
**Description:** Issues a war bond from the clan. Note: a clan may only give one bond at a time.

**Options:**
- `amount` *(Integer, Required)*: Amount of money you wish to loan in the form of a bond.
- `interest` *(Integer, Required)*: The interest on aforementioned bond in %
- `length` *(Integer, Required)*: The amount of time in days that the receiving clan has to pay you back.

**Permissions:** General of the clan only.

---

### 2. `/clan bond purchase`
**Description:** Purchase a war bond. The bond money is deposited into your clan funds.

**Options:**
- `clan-name` *(String, Required)*: The name of the clan who issued the war bond.

**Permissions:** General of the clan only.

---

### 3. `/clan bond repay`
**Description:** Repay a war bond. 

**Options:**
- `clan-name` *(String, Required)*: Name of the clan to which you wish to repay your bond.
- `amount` *(Integer, Required)*: Amount of money you wish to repay.

**Permissions:** General of the clan only.

---

### 4. `/clan bond list`
**Description:** List all outgoing war bonds your clan has.

**Permissions:** None.

### 5. `/clan bond viewall`
**Description:** View all current untaken war bonds.

**Permissions:** None.

---