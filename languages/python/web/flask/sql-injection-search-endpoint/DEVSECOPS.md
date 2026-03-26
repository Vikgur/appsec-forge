This case demonstrates one of many possible approaches — a combination of several tools — and is not the only viable solution. 

**DevSecOps-tools configs:**

* [Semgrep SAST rule for Flask SQLi](/devsecops/sast/semgrep/languages/python/web/flask/sql-injection-search-endpoint.yaml)
* [Bandit SAST rule for Flask SQLi](/devsecops/sast/bandit/languages/python/web/flask/sql-injection-search-endpoint.yaml)
* [OWASP ZAP DAST config for Flask SQLi](/devsecops/dast/owasp-zap/languages/python/web/flask/sql-injection-search-endpoint.yaml)
* [Falco runtime rule for Flask SQLi](/devsecops/runtime-security/falco/languages/python/web/flask/sql-injection-search-endpoint.yaml)

**Custom script:** [Flask SQLi test script](/devsecops/scripts/languages/python/web/flask/sql-injection-search-endpoint.sh) — сhecks a Flask endpoint for SQL injection using `' OR '1'='1` in the `email` parameter, flagging vulnerability if `admin@example.com` appears in the response.
