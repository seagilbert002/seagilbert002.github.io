# Capstone ePortfolio

Welcome to my ePortfolio. This site hosts my profession portfolio, code reviews, and artifact enhancements demostrating full-stack engineering, embedded systems development, and data security.

---

## Professional Self-Introduction
I am a Computer Science student with a focus on full-stack web development, embedded systems engineering, and relational database architectures. Throughout my studies, I have developed skills in low-level hardware communication, algorithmic analysis, and secure software design.

---

## Artifact Enhancements Summary

### Category One: Software Engineering & Design
* **Original Artifact:** Raspberry Pi Thermostat Application (*CS 350*)
* **Enhancement Overview:** Re-architected a monolithic script into a decoupled **IoT Bookshelf Environmental Telemetry Daemon**.
* **Key Features:**
  * **Hardware Abstraction Layer (HAL):** Toggles seamlessly between physical GPIO sensors and simulated mock drivers for isolated testing.
  * **Fault-Tolerant Networking:** Implements an exponential backoff retry algorithm to handle network interruptions gracefully while logging shelf conditions over HTTP REST endpoints.

---

### Category Two: Algorithms & Data Structures
* **Original Artifact:** Little Library Web Application
* **Enhancement Overview:** Implemented custom password security algorithms for user authentication, focusing on key-stretching iterations and side-channel timing attack defenses.
* **Key Algorithms:**
  * **Key-Stretching Iteration Engine:** An $O(2^k)$ time-complexity algorithm that repeatedly hashes passphrases with a random 128-bit salt to prevent GPU-accelerated brute-force attacks.
  * **Constant-Time Verification:** An $O(n)$ full-scan string comparison algorithm that prevents timing side-channel exploits by ensuring execution time remains uniform regardless of input correctness.
  * **Rolling Humidity Filter:** A rolling-average algorithm used to filter sensor noise before evaluating mold-risk thresholds for collector book editions.

---

### Category Three: Databases
* **Original Artifact:** Little Library Web Application
* **Enhancement Overview:** Migrated the data layer to **Next.js with Raw PostgreSQL** (`pg` pool) using pure parameterized SQL queries instead of an ORM abstraction.
* **Key Database Architecture:**
  * **Detailed Collector Schema:** Maintains detailed inventory fields including `location`, `sprayed_edges`, `special_ed`, `signed`, `ean_isbn`, and `upc_isbn`.
  * **Friend Request Workflow:** Multi-table state machine (`PENDING`, `APPROVED`, `DECLINED`, `CHECKED_OUT`, `RETURNED`) enabling friends to request book loans.
  * **Transactional Integrity & Security:** Enforces ACID transaction blocks (`BEGIN`, `COMMIT`) during checkouts and parameterized query placeholders (`$1, $2`) to eliminate SQL injection vulnerabilities.

---

## Code Reviews & Artifact Repositories
* **GitHub Repository:** [Little Library (Next.js Conversion)](https://github.com/seagilbert002/LittleLibrary)
