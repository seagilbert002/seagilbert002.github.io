# Capstone ePortfolio

Welcome to my ePortfolio. This site hosts my profession portfolio, code reviews, and artifact enhancements demostrating full-stack engineering, embedded systems development, and data security.

---

## Professional Self-Introduction
I am a Computer Science student with a focus on full-stack web development, embedded systems engineering, and relational database architectures. Throughout my studies, I have developed skills in low-level hardware communication, algorithmic analysis, and secure software design.

## Profession Self-Assessment

### Summary
Completing my Bachelor of Science in Computer Science has provided a solid foundation for me to consolidate my hands-on technical background into a comprehensive, production ready skill set. Building this ePortfolio has allowed me to critically evaluate my growth across software architecture, data structures, full-stack development, and database engineering. Through rigorous coursework and practical implementations, I have cultivated a professional philosophy centered on system reliability, defensive engineering, and digital autonomy. My goal is to leverage this technical foundation to engineer robust, maintainable software solutions while contributing to complex, mission-critical infrastructure.

### Technical Competencies & Values

#### Collaborative Team Enviroments
Throughout my degree program and personal projects, I have prioritized clean version control discipline, modular architecture, and collaborative workflows. Working in team environments reinforced the value of structured Git branching, clear commit histories, and expressive pull request documentation. Engaging in peer code reviews sharpened my ability to deliver and integrate constructive feedback, ensuring codebases maintain consistent styling, type safety, and architectural patterns. I view sustainable software development as a team effort that relies on shared technical standards and open communication just as much as individual code execution.

#### Stakeholder Communication
Translating technical complexity into clear business logic has been a cornerstone of my professional development. This skill is best exemplified by my ongoing collaboration with my wife on the Little Library project, a custom catalog and request management system designed for her to organize and share her extensive personal book collection with friends and family. Working directly with her as the primary stakeholder required gathering non-technical user requirements, analyzing borrowing workflows, and explaining architectural trade-offs (such as approval queues versus open access). Whether writing clear system documentation or mapping raw database schemas directly to her real-world book lending rules, I prioritize clarity and transparency to ensure software directly serves human needs.

#### Data Structures and Algorithmic Design
Mastering core algorithms and data structures enabled me to shift from simply writing functional code to evaluating computational complexity (Big “O” notation) for real-world efficiency. Beyond standard linear data structures, my coursework and self-directed projects explored custom algorithm implementations, key-stretching cryptographic hashing (PBKDF2 with SHA-256), and constant-time byte buffer comparisons (O(n) evaluation) to mitigate timing analysis side-channel attacks. Understanding how algorithmic choices impact memory allocations and CPU cycles ensures the software I build performs efficiently under load.

#### Systems Engineering, Homelab & Database Management
My engineering philosophy is rooted in digital autonomy and hands-on systems administration. Beyond traditional coursework, I manage a custom self-hosted homelab infrastructure featuring Proxmox VE running LXC containers, Docker services, custom Linux terminal workflows, and Tailscale mesh networking. This environment serves as a sandbox for managing database instances, network routing, reverse proxies, and system metrics.
Pairing this systems experience with full-stack web engineering, I designed Next.js App Router applications backended by raw PostgreSQL. This included managing connection pools (pg.Pool), implementing server-side Data Access Layers (DAL) with request deduplication via React cache(), and structuring B-tree indexes to optimize query execution plans away from full-table sequential scans.

#### Security & Defensive Engineering
Security is not an add-on feature it is a baseline requirement built into every layer of my software stack. Throughout my capstone and personal systems projects, I consistently emphasize defensive design principles:
- SQL Injection Mitigation: Enforcing positional parameterized queries ($1, $2) to completely isolate user input from executable SQL logic.
- ACID Transaction Integrity: Implementing atomic transaction blocks (BEGIN, COMMIT, ROLLBACK) paired with pessimistic row locks (SELECT ... FOR UPDATE) to prevent race conditions and double allocations in concurrent workflows.
- Session & Token Hygiene: Building database-backed session tracking coupled with HTTP-only, SameSite=Lax cookies to eliminate client-side XSS token extraction

#### Reflection
Developing my ePortfolio allowed me to trace my progression from writing individual scripts to engineering production-ready, full-stack applications and managing real-world containerized infrastructure. The process of auditing, refactoring, and documenting my capstone artifacts highlighted my ability to analyze existing codebases, isolate performance bottlenecks, and execute targeted security enhancements.
This program and my practical systems work have solidified my core values: digital autonomy, structural maintainability, and security first engineering. Armed with a computer science degree, homelab systems experience, and a portfolio demonstrating mastery across algorithms, database engineering, and full-stack architecture, I am prepared to deliver immediate value as a versatile computer science professional.

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

### Code Review:

[Code Review](https://youtu.be/ushpgKFn3BE)

### Original Artifact
* **GitHub Repository:** [Little Library Orignal](https://github.com/seagilbert002/LittleLibrary)

### Enhanced Artifact

* **GitHub Repository:** [Little Library Next.JS](https://github.com/seagilbert002/LittleLibrary-Next)
* **GitHub Repository:** [Sensor Daemon](https://github.com/seagilbert002/temp_humidity_sensor)


