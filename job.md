

# Job Commands (`/job`)

---
Members can apply for jobs, which have different perks / abilities once they have them. Members can receive their salaries once every 6 hours by running the `!collect` command.

Job Info:

- `farmer` - No abilities, salary of 900 BB.
- `lieutenant` - Control of the clan army, salary of 1800 BB.
- `propagandist` - Access to the propaganda channel, salary of 1600 BB.
- `delegate` - Access to the negotiating table, salary of 2400 BB.
- `scout` - Ability to scout enemy tiles, salary of 1200 BB.
- `mechanic` - Ability to upgrade units / tiles, salary of 1500 BB.

---
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

### 5. `/clan mechanic upgrade`
**Description:** Allows a **mechanic** job role to upgrade a troop type, increasing its strength.

**Permissions:** Mechanic only.

---
