# appsec-forge

Practical AppSec / DevSecOps lab with **realistic, reproducible security cases**.

Learn how vulnerabilities actually happen in production systems — and how to **exploit, fix, and prevent them end-to-end**.

---

# Table of Contents

* [About](#about)
* [Target Audience](#target-audience)
* [Navigation](#navigation)
* [How to Use](#how-to-use)
* [appsec-forge VS appsec-forge-pro](#appsec-forge-vs-appsec-forge-pro)
* [License](#license)

---

# About

**appsec-forge** is a hands-on laboratory for analyzing and preventing vulnerabilities across applications, infrastructure, and supply chain.

Each case reflects real engineering workflows:

**feature → vulnerability → exploit → fix → prevention → detection**

No toy examples. Only realistic scenarios based on how systems are actually built and broken.

---

# Target Audience

For engineers who build or secure real systems:

- Developers → learn secure coding through real attack paths  
- DevOps / DevSecOps → secure pipelines, configs, and supply chain  
- Security / AppSec → structure, exploit, and mitigate vulnerabilities  

---

# Navigation

Start from the root depending on your focus:

- `languages/` — application vulnerabilities (language → context → framework → case)  
- `infrastructure/` — infra & cloud security (area → tool → context → case)  
- `supply-chain/` — CI/CD, dependencies, artifacts security  
- `devsecops/` — security tool configurations (SAST, SCA, scanning, etc.)

---

# Case Structure

Each case includes:

- `feature.md` — real product context  
- `vuln_*` — vulnerable implementation  
- `exploit/` or `exploit_payload.txt` — how it is exploited  
- `fixed_*` — baseline fix  
- `README.md` — full analysis  

---

# How to Use

1. Pick a domain (`languages`, `infrastructure`, `supply-chain`)  
2. Navigate to a specific case  
3. Reproduce the vulnerability  
4. Run the exploit  
5. Apply the fix  
6. Review prevention checklist  

Optional:

- Integrate configs from `devsecops/` into your pipeline  

---

# appsec-forge VS appsec-forge-pro

| Feature | appsec-forge (public) | appsec-forge-pro (private) |
|--------|------------|-------------|
| Vulnerability | ✔ | ✔ |
| Exploit | ✔ | ✔ |
| Fix | Basic | Production-grade |
| Depth | Limited | Full |
| Threat Model | ✖ | ✔ |
| Check-List | ✖ | ✔ |
| Hardening | ✖ | ✔ |
| Detection Rules | ✖ | ✔ |
| DevSecOps Configs | ✖ | ✔ |

**appsec-forge** → learning and preview  
**appsec-forge-pro** → production-ready security practices

---

# License

See `LICENSE` file for details.