#spring-actuator-fuzzlist

A curated list of payloads, fuzzing paths, and evasion techniques to help security researchers and bug bounty hunters discover exposed or misconfigured Spring Boot Actuator endpoints.

Spring Boot’s `/actuator` endpoints can leak sensitive system data, expose internal services, or even allow remote code execution if improperly secured. This repo helps you find them — even when they're hidden behind custom paths or protected by weak controls.

---

##What's Inside

- ✅ Common actuator endpoint names (`/health`, `/env`, `/metrics`, etc.)
- 🔀 Obfuscated & alternate base paths (`/api/actuator`, `/manage/actuator`, etc.)
- 🛡️ Bypass payloads (`/actuator%2f`, `/actuator/..;/env`, etc.)
- 🎯 Ready-to-use wordlists for FFUF, Burp Suite, or custom tools

---

##Usage

Example with **ffuf**:
```bash
ffuf -u https://target.com/FUZZ -w wordlists/actuator-paths.txt -mc all
