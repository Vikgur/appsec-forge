# Table of Contents

* [About](#about)
* [Vulnerability Overview](#vulnerability-overview)
* [Feature Context](#feature-context)
* [Attack Surface](#attack-surface)
* [Vulnerable Flow](#vulnerable-flow)
* [Exploit](#exploit)
* [Impact](#impact)
* [Root Cause](#root-cause)
* [Fix (Base)](#fix-base)
* [Prevention](#prevention)
* [What’s Missing](#whats-missing)
* [Next Step](#next-step)
* [License](#license)

# About

SQL injection in a Flask search endpoint allows full database exposure.  
Common in internal tools, admin APIs, and quick-filter features.

# Vulnerability Overview

Class: SQL Injection (SQLi).  
User-controlled input alters SQL query structure.  
Leads to unintended data access and query manipulation.

# Feature Context

Search users by email via API.  
Used for fast lookup in admin panels and internal services.

# Attack Surface

Entry point: HTTP query parameter `email`.  
Trust boundary: user input → database query.

# Vulnerable Flow

User sends request with email parameter.  
Application builds SQL query using string formatting.  
Database executes modified query.  
Response returns unintended data.

# Exploit

See exploit_payload.txt.  
Attacker injects SQL condition to bypass filtering.  
Result: full dataset returned.

# Impact

Unauthorized data access.  
User enumeration.  
Sensitive data exposure.  
Potential pivot into other systems.

# Root Cause

Direct string interpolation in SQL queries without parameterization.  
Input treated as trusted data instead of untrusted input.

# Fix (Base)

See fixed_app.*  
Use parameterized queries to separate data from query structure.

# Prevention

Prevent issues through manual checks and **DevSecOps practices implementation**.  
This case demonstrates one of many possible approaches — a combination of several tools — and is not the only viable solution.  
Find configurations in **DEVSECOPS.md**.

# What’s Missing

bypass techniques  
edge cases  
detection  
CI/CD protection  
production hardening

# Next Step

Production coverage includes:  
checklist  
threat modeling  
hardening  
detection  

→ full production version is available in appsec-forge-pro

# License

This case is part of the repository licensed under the MIT License.  
See the root LICENSE file for details.
