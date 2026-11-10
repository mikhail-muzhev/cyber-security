[🏠 Главная](README.md) › 📚 Источники

# 📚 Источники

Все источники, на которые ссылаются материалы проекта, сгруппированы по типу. В колонке «Разделы» указаны номера разделов [«Угроз»](threats/README.md), где используется источник.

> [!NOTE]
> **Как проверять.** Предпочтение отдаётся первоисточникам: стандартам, официальным отчётам, сообщениям госорганов и самих пострадавших компаний. СМИ и вторичные источники используются, только если первоисточник недоступен или не содержит нужных данных. Доступность всех ссылок проверялась в ноябре 2026 года.
>
> Некоторые сайты (FBI, FCC, GAO, SEC, Senate.gov, NSA, NY DFS, Medium, Cloudflare, Coinbase, Uber, Computer Weekly) блокируют автоматические запросы, но открываются в обычном браузере. Сайты ФСТЭК могут быть недоступны из-за рубежа.

**Навигация:** [Российские нормативные документы и организации](#российские-нормативные-документы-и-организации) · [MITRE: ATT&CK, ATLAS, CWE](#mitre-attck-atlas-cwe) · [NIST](#nist) · [OWASP](#owasp) · [Отчёты об угрозах](#отчёты-об-угрозах) · [Госорганы и правоохранители](#госорганы-и-правоохранители) · [Компании (официальные разборы и документация)](#компании-официальные-разборы-и-документация) · [Исследования и независимые источники](#исследования-и-независимые-источники) · [СМИ](#сми)

---

## Российские нормативные документы и организации

| Источник | Разделы |
|---|:-:|
| [Банк данных угроз ФСТЭК России](https://bdu.fstec.ru/threat) | [обзор](threats/README.md) |
| [Банк России: Информационная безопасность и противодействие мошенничеству](https://www.cbr.ru/information_security/) | [2](threats/02-social-engineering.md) |
| [ГОСТ Р 50922-2006. Защита информации. Основные термины и определения](https://docs.cntd.ru/document/1200058320) | [обзор](threats/README.md), [0](threats/00-basics.md) |
| [ГОСТ Р 51275-2006. Факторы, воздействующие на информацию](https://docs.cntd.ru/document/1200057516) | [обзор](threats/README.md), [12](threats/12-physical.md) |
| [Методика оценки угроз безопасности информации, ФСТЭК России, 05.02.2021](https://www.consultant.ru/document/cons_doc_LAW_378330/) | [обзор](threats/README.md), [0](threats/00-basics.md) |

## MITRE: ATT&CK, ATLAS, CWE

| Источник | Разделы |
|---|:-:|
| [Credential Access (TA0006)](https://attack.mitre.org/tactics/TA0006/) | [3](threats/03-credentials.md), [8](threats/08-apt.md) |
| [G0007](https://attack.mitre.org/groups/G0007/) | [8](threats/08-apt.md) |
| [MITRE ATLAS](https://atlas.mitre.org/) | [11](threats/11-ai.md) |
| [MITRE ATT&CK](https://attack.mitre.org/) | [8](threats/08-apt.md) |
| [MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/) | [8](threats/08-apt.md) |
| [MITRE ATT&CK. Enterprise Tactics](https://attack.mitre.org/tactics/enterprise/) | [обзор](threats/README.md), [8](threats/08-apt.md) |
| [MITRE ATT&CK: Cloud Matrix](https://attack.mitre.org/matrices/enterprise/cloud/) | [9](threats/09-cloud.md) |
| [MITRE ATT&CK: Groups](https://attack.mitre.org/groups/) | [8](threats/08-apt.md) |
| [MITRE ATT&CK: Initial Access (TA0001)](https://attack.mitre.org/tactics/TA0001/) | [1](threats/01-malware.md), [8](threats/08-apt.md) |
| [MITRE ATT&CK: Mobile Matrix](https://attack.mitre.org/matrices/mobile/) | [10](threats/10-mobile-iot.md) |
| [MITRE ATT&CK: T1040 Network Sniffing](https://attack.mitre.org/techniques/T1040/) | [4](threats/04-network.md) |
| [MITRE ATT&CK: T1059 Command and Scripting Interpreter](https://attack.mitre.org/techniques/T1059/) | [1](threats/01-malware.md) |
| [MITRE ATT&CK: T1078 Valid Accounts](https://attack.mitre.org/techniques/T1078/) | [3](threats/03-credentials.md) |
| [MITRE ATT&CK: T1091 Replication Through Removable Media](https://attack.mitre.org/techniques/T1091/) | [12](threats/12-physical.md) |
| [MITRE ATT&CK: T1110 Brute Force](https://attack.mitre.org/techniques/T1110/) | [3](threats/03-credentials.md) |
| [MITRE ATT&CK: T1189 Drive-by Compromise](https://attack.mitre.org/techniques/T1189/) | [2](threats/02-social-engineering.md) |
| [MITRE ATT&CK: T1190 Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/) | [4](threats/04-network.md), [5](threats/05-web.md), [6](threats/06-supply-chain.md) |
| [MITRE ATT&CK: T1195 Supply Chain Compromise](https://attack.mitre.org/techniques/T1195/) | [6](threats/06-supply-chain.md) |
| [MITRE ATT&CK: T1199 Trusted Relationship](https://attack.mitre.org/techniques/T1199/) | [6](threats/06-supply-chain.md) |
| [MITRE ATT&CK: T1200 Hardware Additions](https://attack.mitre.org/techniques/T1200/) | [12](threats/12-physical.md) |
| [MITRE ATT&CK: T1486 Data Encrypted for Impact](https://attack.mitre.org/techniques/T1486/) | [1](threats/01-malware.md) |
| [MITRE ATT&CK: T1498 Network Denial of Service](https://attack.mitre.org/techniques/T1498/) | [4](threats/04-network.md) |
| [MITRE ATT&CK: T1530 Data from Cloud Storage](https://attack.mitre.org/techniques/T1530/) | [9](threats/09-cloud.md) |
| [MITRE ATT&CK: T1539 Steal Web Session Cookie](https://attack.mitre.org/techniques/T1539/) | [3](threats/03-credentials.md) |
| [MITRE ATT&CK: T1552 Unsecured Credentials](https://attack.mitre.org/techniques/T1552/) | [9](threats/09-cloud.md) |
| [MITRE ATT&CK: T1557 Adversary-in-the-Middle](https://attack.mitre.org/techniques/T1557/) | [3](threats/03-credentials.md), [4](threats/04-network.md) |
| [MITRE ATT&CK: T1566 Phishing](https://attack.mitre.org/techniques/T1566/) | [2](threats/02-social-engineering.md) |
| [MITRE ATT&CK: T1598 Phishing for Information](https://attack.mitre.org/techniques/T1598/) | [2](threats/02-social-engineering.md) |
| [MITRE ATT&CK: T1621 Multi-Factor Authentication Request Generation](https://attack.mitre.org/techniques/T1621/) | [3](threats/03-credentials.md) |
| [MITRE CWE: CWE-352 CSRF](https://cwe.mitre.org/data/definitions/352.html) | [5](threats/05-web.md) |
| [MITRE CWE: CWE-79 XSS](https://cwe.mitre.org/data/definitions/79.html) | [5](threats/05-web.md) |
| [MITRE CWE: CWE-89 SQL Injection](https://cwe.mitre.org/data/definitions/89.html) | [5](threats/05-web.md) |
| [MITRE CWE: CWE-918 SSRF](https://cwe.mitre.org/data/definitions/918.html) | [5](threats/05-web.md) |
| [T1078.001](https://attack.mitre.org/techniques/T1078/001/) | [3](threats/03-credentials.md) |
| [T1078.004](https://attack.mitre.org/techniques/T1078/004/) | [9](threats/09-cloud.md) |
| [T1110.001](https://attack.mitre.org/techniques/T1110/001/) | [3](threats/03-credentials.md) |
| [T1110.002](https://attack.mitre.org/techniques/T1110/002/) | [3](threats/03-credentials.md) |
| [T1110.003](https://attack.mitre.org/techniques/T1110/003/) | [3](threats/03-credentials.md) |
| [T1110.004](https://attack.mitre.org/techniques/T1110/004/) | [3](threats/03-credentials.md) |
| [T1111](https://attack.mitre.org/techniques/T1111/) | [3](threats/03-credentials.md) |
| [T1195.001](https://attack.mitre.org/techniques/T1195/001/) | [6](threats/06-supply-chain.md) |
| [T1195.002](https://attack.mitre.org/techniques/T1195/002/) | [6](threats/06-supply-chain.md) |
| [T1195.003](https://attack.mitre.org/techniques/T1195/003/) | [6](threats/06-supply-chain.md) |
| [T1451 (Mobile)](https://attack.mitre.org/techniques/T1451/) | [3](threats/03-credentials.md) |
| [T1485 Data Destruction](https://attack.mitre.org/techniques/T1485/) | [1](threats/01-malware.md) |
| [T1490 Inhibit System Recovery](https://attack.mitre.org/techniques/T1490/) | [1](threats/01-malware.md) |
| [T1496](https://attack.mitre.org/techniques/T1496/) | [9](threats/09-cloud.md) |
| [T1499 Endpoint Denial of Service](https://attack.mitre.org/techniques/T1499/) | [4](threats/04-network.md) |
| [T1552.001](https://attack.mitre.org/techniques/T1552/001/) | [9](threats/09-cloud.md) |
| [T1552.005](https://attack.mitre.org/techniques/T1552/005/) | [9](threats/09-cloud.md) |
| [T1595 Active Scanning](https://attack.mitre.org/techniques/T1595/) | [4](threats/04-network.md) |
| [TA0002](https://attack.mitre.org/tactics/TA0002/) | [8](threats/08-apt.md) |
| [TA0003](https://attack.mitre.org/tactics/TA0003/) | [8](threats/08-apt.md) |
| [TA0004](https://attack.mitre.org/tactics/TA0004/) | [8](threats/08-apt.md) |
| [TA0005](https://attack.mitre.org/tactics/TA0005/) | [8](threats/08-apt.md) |
| [TA0007](https://attack.mitre.org/tactics/TA0007/) | [8](threats/08-apt.md) |
| [TA0008](https://attack.mitre.org/tactics/TA0008/) | [8](threats/08-apt.md) |
| [TA0009](https://attack.mitre.org/tactics/TA0009/) | [8](threats/08-apt.md) |
| [TA0010](https://attack.mitre.org/tactics/TA0010/) | [8](threats/08-apt.md) |
| [TA0011](https://attack.mitre.org/tactics/TA0011/) | [8](threats/08-apt.md) |
| [TA0040](https://attack.mitre.org/tactics/TA0040/) | [8](threats/08-apt.md) |
| [TA0042](https://attack.mitre.org/tactics/TA0042/) | [8](threats/08-apt.md) |
| [TA0043](https://attack.mitre.org/tactics/TA0043/) | [8](threats/08-apt.md) |

## NIST

| Источник | Разделы |
|---|:-:|
| [NIST AI 100-2 E2025. Adversarial Machine Learning: A Taxonomy and Terminology](https://csrc.nist.gov/pubs/ai/100/2/e2025/final) | [11](threats/11-ai.md) |
| [NIST Glossary](https://csrc.nist.gov/glossary) | [0](threats/00-basics.md) |
| [NIST Glossary: Advanced Persistent Threat](https://csrc.nist.gov/glossary/term/advanced_persistent_threat) | [8](threats/08-apt.md) |
| [NIST SP 800-12 Rev. 1. An Introduction to Information Security](https://csrc.nist.gov/pubs/sp/800/12/r1/final) | [обзор](threats/README.md), [0](threats/00-basics.md) |
| [NIST SP 800-161 Rev. 1](https://csrc.nist.gov/pubs/sp/800/161/r1/upd1/final) | [6](threats/06-supply-chain.md) |
| [NIST SP 800-30 Rev. 1. Guide for Conducting Risk Assessments](https://csrc.nist.gov/pubs/sp/800/30/r1/final) | [0](threats/00-basics.md) |
| [NIST SP 800-34 Rev. 1. Contingency Planning Guide for Federal Information Systems](https://csrc.nist.gov/pubs/sp/800/34/r1/upd1/final) | [13](threats/13-non-malicious.md) |
| [NIST SP 800-63B-4. Authentication and Authenticator Management](https://pages.nist.gov/800-63-4/sp800-63b.html) | [3](threats/03-credentials.md) |
| [NVD: CVE-2017-5638](https://nvd.nist.gov/vuln/detail/CVE-2017-5638) | [5](threats/05-web.md) |
| [NVD: CVE-2021-44228 (Log4Shell)](https://nvd.nist.gov/vuln/detail/CVE-2021-44228) | [6](threats/06-supply-chain.md) |
| [NVD: CVE-2024-3094 (xz)](https://nvd.nist.gov/vuln/detail/CVE-2024-3094) | [6](threats/06-supply-chain.md) |

## OWASP

| Источник | Разделы |
|---|:-:|
| [Authentication Failures](https://owasp.org/Top10/2025/A07_2025-Authentication_Failures/) | [5](threats/05-web.md) |
| [Broken Access Control](https://owasp.org/Top10/2025/A01_2025-Broken_Access_Control/) | [5](threats/05-web.md) |
| [Cryptographic Failures](https://owasp.org/Top10/2025/A04_2025-Cryptographic_Failures/) | [5](threats/05-web.md) |
| [Injection](https://owasp.org/Top10/2025/A05_2025-Injection/) | [5](threats/05-web.md) |
| [Insecure Design](https://owasp.org/Top10/2025/A06_2025-Insecure_Design/) | [5](threats/05-web.md) |
| [Mishandling of Exceptional Conditions](https://owasp.org/Top10/2025/A10_2025-Mishandling_of_Exceptional_Conditions/) | [5](threats/05-web.md) |
| [OWASP Application Security Verification Standard (ASVS)](https://owasp.org/www-project-application-security-verification-standard/) | [5](threats/05-web.md) |
| [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/) | [5](threats/05-web.md) |
| [OWASP Internet of Things Project](https://owasp.org/www-project-internet-of-things/) | [10](threats/10-mobile-iot.md) |
| [OWASP LLM01:2025 Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/) | [11](threats/11-ai.md) |
| [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/) | [10](threats/10-mobile-iot.md) |
| [OWASP Top 10 for LLM Applications 2025](https://genai.owasp.org/llm-top-10/) | [11](threats/11-ai.md) |
| [OWASP Top 10:2025](https://owasp.org/Top10/2025/) | [5](threats/05-web.md) |
| [Security Logging and Alerting Failures](https://owasp.org/Top10/2025/A09_2025-Security_Logging_and_Alerting_Failures/) | [5](threats/05-web.md) |
| [Security Misconfiguration](https://owasp.org/Top10/2025/A02_2025-Security_Misconfiguration/) | [5](threats/05-web.md) |
| [Software or Data Integrity Failures](https://owasp.org/Top10/2025/A08_2025-Software_or_Data_Integrity_Failures/) | [5](threats/05-web.md) |
| [Software Supply Chain Failures](https://owasp.org/Top10/2025/A03_2025-Software_Supply_Chain_Failures/) | [5](threats/05-web.md) |

## Отчёты об угрозах

| Источник | Разделы |
|---|:-:|
| [Cloud Security Alliance: Top Threats to Cloud Computing 2024](https://cloudsecurityalliance.org/artifacts/top-threats-to-cloud-computing-2024) | [9](threats/09-cloud.md) |
| [ENISA Threat Landscape 2025](https://www.enisa.europa.eu/publications/enisa-threat-landscape-2025) | [обзор](threats/README.md), [1](threats/01-malware.md), [2](threats/02-social-engineering.md) |
| [Help Net Security: Verizon DBIR 2026](https://www.helpnetsecurity.com/2026/05/25/lessons-from-verizon-dbir-2026-findings/) | [11](threats/11-ai.md) |
| [Verizon Data Breach Investigations Report](https://www.verizon.com/business/resources/reports/dbir/) | [обзор](threats/README.md), [13](threats/13-non-malicious.md) |

## Госорганы и правоохранители

| Источник | Разделы |
|---|:-:|
| [CISA #StopRansomware Guide](https://www.cisa.gov/stopransomware/ransomware-guide) | [1](threats/01-malware.md) |
| [CISA AA20-352A: SolarWinds](https://www.cisa.gov/news-events/cybersecurity-advisories/aa20-352a) | [6](threats/06-supply-chain.md) |
| [CISA AA24-038A: Volt Typhoon](https://www.cisa.gov/news-events/cybersecurity-advisories/aa24-038a) | [8](threats/08-apt.md) |
| [CISA ICS Alert: Cyber-Attack Against Ukrainian Critical Infrastructure](https://www.cisa.gov/news-events/ics-alerts/ir-alert-h-16-056-01) | [8](threats/08-apt.md) |
| [CISA, NIST: Defending Against Software Supply Chain Attacks](https://www.cisa.gov/resources-tools/resources/defending-against-software-supply-chain-attacks) | [6](threats/06-supply-chain.md) |
| [CISA, NSA, FBI, MS-ISAC: Phishing Guidance: Stopping the Attack Cycle at Phase One](https://www.cisa.gov/resources-tools/resources/phishing-guidance-stopping-attack-cycle-phase-one) | [2](threats/02-social-engineering.md) |
| [CISA: Apache Log4j Vulnerability Guidance](https://www.cisa.gov/news-events/news/apache-log4j-vulnerability-guidance) | [6](threats/06-supply-chain.md) |
| [CISA: Avoiding Social Engineering and Phishing Attacks](https://www.cisa.gov/news-events/news/avoiding-social-engineering-and-phishing-attacks) | [2](threats/02-social-engineering.md) |
| [CISA: Defining Insider Threats](https://www.cisa.gov/topics/physical-security/insider-threat-mitigation/defining-insider-threats) | [7](threats/07-insiders.md) |
| [CISA: Heightened DDoS Threat Posed by Mirai and Other Botnets](https://www.cisa.gov/news-events/alerts/2016/10/14/heightened-ddos-threat-posed-mirai-and-other-botnets) | [4](threats/04-network.md) |
| [CISA: Implementing Phishing-Resistant MFA](https://www.cisa.gov/sites/default/files/publications/fact-sheet-implementing-phishing-resistant-mfa-508c.pdf) | [3](threats/03-credentials.md) |
| [CISA: Indicators Associated With WannaCry Ransomware](https://www.cisa.gov/news-events/alerts/2017/05/12/indicators-associated-wannacry-ransomware) | [1](threats/01-malware.md) |
| [CISA: Insider Threat Mitigation Guide](https://www.cisa.gov/resources-tools/resources/insider-threat-mitigation-guide) | [7](threats/07-insiders.md) |
| [CISA: Kaseya VSA Supply-Chain Ransomware Attack](https://www.cisa.gov/news-events/news/kaseya-ransomware-attack-guidance-affected-msps-and-their-customers) | [6](threats/06-supply-chain.md) |
| [CISA: Petya Ransomware (TA17-181A)](https://www.cisa.gov/news-events/alerts/2017/07/01/petya-ransomware) | [1](threats/01-malware.md) |
| [CISA: Physical Security](https://www.cisa.gov/topics/physical-security) | [12](threats/12-physical.md) |
| [CISA: Remediating Networks Affected by the SolarWinds and Active Directory/M365 Compromise](https://www.cisa.gov/news-events/news/remediating-networks-affected-solarwinds-and-active-directorym365-compromise) | [6](threats/06-supply-chain.md) |
| [CISA: The Attack on Colonial Pipeline](https://www.cisa.gov/news-events/news/attack-colonial-pipeline-what-weve-learned-what-weve-done-over-past-two-years) | [1](threats/01-malware.md) |
| [CISA: Understanding and Responding to DDoS Attacks](https://www.cisa.gov/resources-tools/resources/understanding-and-responding-distributed-denial-service-attacks) | [4](threats/04-network.md) |
| [CISA: xz Utils](https://www.cisa.gov/news-events/alerts/2024/03/29/reported-supply-chain-compromise-affecting-xz-utils-data-compression-library-cve-2024-3094) | [6](threats/06-supply-chain.md) |
| [ETSI: Consumer IoT Security (EN 303 645)](https://www.etsi.org/technologies/consumer-iot-security) | [10](threats/10-mobile-iot.md) |
| [Europol: World's most dangerous malware EMOTET disrupted](https://www.europol.europa.eu/media-press/newsroom/news/world%E2%80%99s-most-dangerous-malware-emotet-disrupted-through-global-action) | [1](threats/01-malware.md) |
| [FBI IC3 PSA (май 2025)](https://www.ic3.gov/PSA/2025/PSA250515) | [11](threats/11-ai.md) |
| [FBI IC3 PSA250123: North Korean IT Workers](https://www.ic3.gov/PSA/2025/PSA250123) | [7](threats/07-insiders.md) |
| [FBI: Business Email Compromise](https://www.fbi.gov/how-we-can-help-you/scams-and-safety/common-frauds-and-scams/business-email-compromise) | [2](threats/02-social-engineering.md) |
| [FCC: Juice Jacking](https://www.fcc.gov/juice-jacking-tips-to-avoid-it) | [10](threats/10-mobile-iot.md) |
| [NSA: Mobile Device Best Practices](https://media.defense.gov/2020/Jul/28/2002465535/-1/-1/0/MOBILE_DEVICE_BEST_PRACTICES_FINAL_V3%20-%20COPY.PDF) | [10](threats/10-mobile-iot.md) |
| [NY DFS: Twitter Investigation Report](https://www.dfs.ny.gov/Twitter_Report) | [2](threats/02-social-engineering.md) |
| [SolarWinds Form 8-K (SEC, 14.12.2020)](https://www.sec.gov/Archives/edgar/data/1739942/000162828020017451/swi-20201214.htm) | [6](threats/06-supply-chain.md) |
| [US DOJ: Former Seattle tech worker convicted](https://www.justice.gov/usao-wdwa/pr/former-seattle-tech-worker-convicted-wire-fraud-and-computer-intrusions) | [5](threats/05-web.md) |
| [US DOJ: Two Former Twitter Employees and a Saudi National Charged](https://www.justice.gov/opa/pr/two-former-twitter-employees-and-saudi-national-charged-acting-illegal-agents-saudi-arabia) | [7](threats/07-insiders.md) |
| [US GAO: Actions Taken by Equifax (GAO-18-559)](https://www.gao.gov/products/gao-18-559) | [5](threats/05-web.md) |
| [Сенат США: показания CEO Colonial Pipeline об отсутствии MFA](https://www.hsgac.senate.gov/media/reps/portman-presses-president-and-ceo-of-colonial-pipeline-on-gaps-in-cybersecurity-practices/) | [1](threats/01-malware.md) |

## Компании (официальные разборы и документация)

| Источник | Разделы |
|---|:-:|
| [23andMe: Addressing Data Security Concerns](https://blog.23andme.com/articles/addressing-data-security-concerns) | [3](threats/03-credentials.md) |
| [Apple: About Lockdown Mode](https://support.apple.com/en-us/105120) | [10](threats/10-mobile-iot.md) |
| [AWS: Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/) | [9](threats/09-cloud.md) |
| [Cloudflare Learning Center (на русском)](https://www.cloudflare.com/ru-ru/learning/) | [4](threats/04-network.md) |
| [Cloudflare: Что такое DDoS-атака?](https://www.cloudflare.com/ru-ru/learning/ddos/what-is-a-ddos-attack/) | [4](threats/04-network.md) |
| [Cloudflare: Что такое атака «человек посередине»?](https://www.cloudflare.com/ru-ru/learning/security/threats/man-in-the-middle-attack/) | [4](threats/04-network.md) |
| [Cloudflare: Что такое отравление кеша DNS?](https://www.cloudflare.com/ru-ru/learning/dns/dns-cache-poisoning/) | [4](threats/04-network.md) |
| [Coinbase: Protecting Our Customers — Standing Up to Extortionists](https://www.coinbase.com/blog/protecting-our-customers-standing-up-to-extortionists) | [7](threats/07-insiders.md) |
| [CrowdStrike: Falcon Update for Windows Hosts — Technical Details](https://www.crowdstrike.com/en-us/blog/falcon-update-for-windows-hosts-technical-details/) | [13](threats/13-non-malicious.md) |
| [GitHub Blog: February 28th DDoS Incident Report](https://github.blog/news-insights/company-news/ddos-incident-report/) | [4](threats/04-network.md) |
| [GitLab: Postmortem of database outage of January 31](https://about.gitlab.com/blog/2017/02/10/postmortem-of-database-outage-of-january-31/) | [13](threats/13-non-malicious.md) |
| [Google Cloud / Mandiant: UNC5537 Targets Snowflake Customer Instances](https://cloud.google.com/blog/topics/threat-intelligence/unc5537-snowflake-data-theft-extortion) | [3](threats/03-credentials.md), [9](threats/09-cloud.md) |
| [Lockheed Martin: Cyber Kill Chain](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html) | [8](threats/08-apt.md) |
| [Microsoft Security Bulletin MS17-010](https://learn.microsoft.com/en-us/security-updates/securitybulletins/2017/ms17-010) | [1](threats/01-malware.md) |
| [Microsoft. Threat Modeling Tool: STRIDE](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool-threats) | [обзор](threats/README.md) |
| [Microsoft: AiTM phishing campaign](https://www.microsoft.com/en-us/security/blog/2022/07/12/from-cookie-theft-to-bec-attackers-use-aitm-phishing-sites-as-entry-point-to-further-financial-fraud/) | [3](threats/03-credentials.md) |
| [Microsoft: Helping our customers through the CrowdStrike outage](https://blogs.microsoft.com/blog/2024/07/20/helping-our-customers-through-the-crowdstrike-outage/) | [13](threats/13-non-malicious.md) |
| [Microsoft: Shared responsibility in the cloud](https://learn.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility) | [9](threats/09-cloud.md) |
| [MSRC: Microsoft mitigated exposure of internal information](https://msrc.microsoft.com/blog/2023/09/microsoft-mitigated-exposure-of-internal-information-in-a-storage-account-due-to-overly-permissive-sas-token/) | [9](threats/09-cloud.md) |
| [Securelist: Operation Triangulation (рус.)](https://securelist.ru/operation-triangulation/107001/) | [8](threats/08-apt.md) |
| [Securelist: The last (?) secret of Operation Triangulation](https://securelist.com/operation-triangulation-the-last-hardware-mystery/111669/) | [8](threats/08-apt.md) |
| [SLSA: Supply-chain Levels for Software Artifacts](https://slsa.dev/) | [6](threats/06-supply-chain.md) |
| [Uber Newsroom: Security update](https://www.uber.com/newsroom/security-update/) | [3](threats/03-credentials.md) |
| [Wiz: 38TB of data accidentally exposed](https://www.wiz.io/blog/38-terabytes-of-private-data-accidentally-exposed-by-microsoft-ai-researchers) | [9](threats/09-cloud.md) |

## Исследования и независимые источники

| Источник | Разделы |
|---|:-:|
| [Alex Birsan: Dependency Confusion](https://medium.com/@alex.birsan/dependency-confusion-4a5d60fec610) | [6](threats/06-supply-chain.md) |
| [Amnesty International: Forensic Methodology Report (Pegasus)](https://www.amnesty.org/en/latest/research/2021/07/forensic-methodology-report-how-to-catch-nso-groups-pegasus/) | [10](threats/10-mobile-iot.md) |
| [CERT/SEI Carnegie Mellon: Common Sense Guide to Mitigating Insider Threats, 7th ed.](https://insights.sei.cmu.edu/library/common-sense-guide-to-mitigating-insider-threats-seventh-edition/) | [7](threats/07-insiders.md) |
| [Citizen Lab: FORCEDENTRY](https://citizenlab.ca/2021/09/forcedentry-nso-group-imessage-zero-click-exploit-captured-in-the-wild/) | [10](threats/10-mobile-iot.md) |
| [David Bianco: The Pyramid of Pain](https://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html) | [8](threats/08-apt.md) |
| [Have I Been Pwned](https://haveibeenpwned.com/) | [3](threats/03-credentials.md) |
| [RIPE NCC: YouTube Hijacking — A RIPE NCC RIS case study](https://www.ripe.net/about-us/news/youtube-hijacking-a-ripe-ncc-ris-case-study/) | [4](threats/04-network.md) |
| [Security Affairs: оценка Kaseya](https://securityaffairs.com/119759/cyber-crime/kaseya-attack-impacted-1500-businesses.html) | [6](threats/06-supply-chain.md) |
| [Simon Willison: Prompt injection attacks against GPT-3 (2022)](https://simonwillison.net/2022/Sep/12/prompt-injection/) | [11](threats/11-ai.md) |
| [Tischer et al. Users Really Do Plug in USB Drives They Find (IEEE S&P 2016)](https://zakird.com/papers/usb.pdf) | [12](threats/12-physical.md) |
| [Сообщение Андреса Фройнда в рассылке oss-security](https://www.openwall.com/lists/oss-security/2024/03/29/4) | [6](threats/06-supply-chain.md) |

## СМИ

| Источник | Разделы |
|---|:-:|
| [CNN, май 2024: компания подтвердила, что это Arup](https://edition.cnn.com/2024/05/16/tech/arup-deepfake-scam-loss-hong-kong-intl-hnk) | [2](threats/02-social-engineering.md), [11](threats/11-ai.md) |
| [CNN, февраль 2024](https://edition.cnn.com/2024/02/04/asia/deepfake-cfo-scam-hong-kong-intl-hnk/index.html) | [2](threats/02-social-engineering.md) |
| [Computer Weekly: OVHCloud fire](https://www.computerweekly.com/news/252497578/OVHCloud-confirms-no-casualties-following-fire-at-Strasbourg-datacentre-campus) | [13](threats/13-non-malicious.md) |
| [The Register (март 2022): отчёт пожарной службы](https://www.theregister.com/2022/03/22/ovhcloud_fire_datacenter_report/) | [13](threats/13-non-malicious.md) |

---

<div align="center">

[🏠 Главная](README.md) · [⚠️ Угрозы](threats/README.md) · [📖 Глоссарий](glossary.md)

</div>
