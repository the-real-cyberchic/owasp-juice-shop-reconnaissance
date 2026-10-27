# OWASP Juice Shop: Attack Surface Mapping & Reconnaissance

A comprehensive reconnaissance and attack surface mapping assessment conducted on **OWASP Juice Shop (v17.1.1)** as part of security training and internship project deliverables[cite: 1].

---

## Repository Structure

- `reports/` - Detailed technical report (`.pdf`) covering environment setup, reconnaissance methodology, inventory, and prioritized testing plan[cite: 1, 6].
- `slides/` - Presentation slide deck (`.pptx` / PDF) summarizing findings across 11 structured slides[cite: 29].
- `diagrams/` - Visual architecture diagram mapping client frontend routes to backend REST APIs and the database layer[cite: 5, 37].

---

## Key Findings Summary

1. **Unauthenticated Configuration Disclosure (`/rest/admin/application-configuration`):** Leaks internal environment metadata, system configurations, and third-party parameters without requiring authentication[cite: 4, 6].
2. **Insecure Direct Object Reference (`/rest/basket/{id}`):** Utilizes sequential numeric identifiers for shopping cart operations, exposing endpoints to object tampering[cite: 4, 6].
3. **Authentication & Token Inspection (`/rest/user/login`):** Evaluated JWT issuance patterns, token validation checks (`/rest/user/whoami`), and Express backend behavior[cite: 3, 4, 6].

---

## Technology Stack Fingerprinted

- **Frontend:** Angular Single Page Application (SPA) (`main.js`, `runtime.js`)[cite: 4]
- **Backend:** Node.js running Express framework (`X-Powered-By: Express`)[cite: 4]
- **Database:** SQLite accessed via Sequelize ORM[cite: 4]
- **Authentication:** JSON Web Tokens (JWT)[cite: 4]

---

## 🚀 Author
**Mercy Itunuoluwa Olalere**  
*Cybersecurity Undergraduate & Security Operations Intern*[cite: 1]
