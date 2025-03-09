

# Job Commands (`/job`)

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
