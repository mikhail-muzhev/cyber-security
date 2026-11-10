[🏠 Главная](README.md) › 📖 Глоссарий

# 📖 Глоссарий

Все термины проекта с короткими объяснениями. Рядом с термином указан раздел, где о нём рассказано подробнее (➡️), и источник определения (🔗), если он есть.

> [!TIP]
> Быстрый поиск по странице: `Ctrl+F` или `Cmd+F`.

**Навигация:** [A–Z (латиница)](#латиница-az) · [А](#а) · [Б](#б) · [В](#в) · [Г](#г) · [Д](#д) · [З](#з) · [И](#и) · [К](#к) · [М](#м) · [Н](#н) · [О](#о) · [П](#п) · [Р](#р) · [С](#с) · [Т](#т) · [У](#у) · [Ф](#ф) · [Х](#х) · [Ц](#ц) · [Ч](#ч) · [Ш](#ш) · [Э](#э)

---

## Латиница (A–Z)

- <a id="aitm"></a>**AiTM** (Adversary-in-the-Middle). Фишинговый сайт-посредник, который передаёт настоящему сайту пароль и одноразовый код жертвы, а себе забирает cookie сессии. Так обходят обычную MFA. ➡️ [Учётные записи](threats/03-credentials.md#обход-многофакторной-аутентификации)
- <a id="api"></a>**API** (Application Programming Interface). Интерфейс, через который программы обмениваются данными друг с другом. Ключ API — «пароль» для программного доступа. ➡️ [Облако](threats/09-cloud.md)
- <a id="apt"></a>**APT** (Advanced Persistent Threat). Продвинутая постоянная угроза: группировка с большими ресурсами, обычно связанная с государством. Месяцами скрытно действует в сети жертвы. ➡️ [APT](threats/08-apt.md) 🔗 [NIST](https://csrc.nist.gov/glossary/term/advanced_persistent_threat)
- <a id="arp-spoofing"></a>**ARP-спуфинг** (ARP spoofing). Подмена в локальной сети: злоумышленник выдаёт свой компьютер за роутер, и трафик идёт через него. ARP — протокол, который связывает IP-адреса с физическими адресами устройств. ➡️ [Сеть](threats/04-network.md#перехват-трафика-mitm)
- <a id="bcp-drp"></a>**BCP / DRP** (Business Continuity Plan / Disaster Recovery Plan). План обеспечения непрерывности бизнеса и план восстановления после аварии: что делать, кто отвечает, в каком порядке восстанавливать системы. ➡️ [Непреднамеренные угрозы](threats/13-non-malicious.md#как-защититься) 🔗 [NIST SP 800-34](https://csrc.nist.gov/pubs/sp/800/34/r1/upd1/final)
- <a id="bec"></a>**BEC** (Business Email Compromise). Компрометация деловой переписки: мошенник выдаёт себя за руководителя или партнёра и просит перевести деньги или сменить реквизиты. ➡️ [Социальная инженерия](threats/02-social-engineering.md#-bec-компрометация-деловой-переписки)
- <a id="bgp"></a>**BGP** (Border Gateway Protocol). Протокол, по которому крупные сети интернета договариваются о маршрутах трафика. ➡️ [Сеть](threats/04-network.md#перехват-маршрутов-bgp)
- <a id="c2"></a>**C2, C&C** (Command and Control). Сервер управления, через который злоумышленник отдаёт команды заражённым устройствам и получает от них данные. ➡️ [APT](threats/08-apt.md#модель-cyber-kill-chain)
- <a id="cia"></a>**CIA, триада** (Confidentiality, Integrity, Availability). Три базовых свойства информации, которые защищает ИБ: [конфиденциальность](#confidentiality), [целостность](#integrity), [доступность](#availability). ➡️ [Базовые понятия](threats/00-basics.md#триада-cia) 🔗 [NIST SP 800-12](https://csrc.nist.gov/pubs/sp/800/12/r1/final)
- <a id="cookie"></a>**Cookie, cookie сессии**. Небольшой фрагмент данных, который сайт сохраняет в браузере. Cookie сессии — «пропуск», по которому сайт узнаёт, что вы уже вошли. Если его украсть, можно войти без пароля. ➡️ [Учётные записи](threats/03-credentials.md#кража-готовых-учётных-данных)
- <a id="credential-stuffing"></a>**Credential stuffing** («набивка» учётных данных). Автоматическая проверка пар «логин–пароль» из утечки одного сайта на других сайтах. ➡️ [Учётные записи](threats/03-credentials.md#атаки-на-пароли) 🔗 [MITRE T1110.004](https://attack.mitre.org/techniques/T1110/004/)
- <a id="csp"></a>**CSP** (Content Security Policy). Политика безопасности контента: сайт сообщает браузеру, откуда разрешено загружать и выполнять скрипты. Защищает от XSS. ➡️ [Веб](threats/05-web.md#-xss-межсайтовый-скриптинг)
- <a id="cspm"></a>**CSPM** (Cloud Security Posture Management). Инструменты, которые автоматически проверяют настройки облака и находят ошибки. ➡️ [Облако](threats/09-cloud.md#как-защититься)
- <a id="csrf"></a>**CSRF** (Cross-Site Request Forgery). Подделка межсайтового запроса: чужой сайт заставляет ваш браузер отправить запрос от вашего имени на сайт, где вы вошли. ➡️ [Веб](threats/05-web.md#-csrf-подделка-межсайтового-запроса) 🔗 [CWE-352](https://cwe.mitre.org/data/definitions/352.html)
- <a id="ddos"></a>**DDoS** (Distributed Denial of Service). Распределённая атака «отказ в обслуживании»: сервис перегружают запросами одновременно с множества устройств. ➡️ [Сеть](threats/04-network.md#dos-и-ddos) 🔗 [NIST](https://csrc.nist.gov/glossary/term/distributed_denial_of_service)
- <a id="dlp"></a>**DLP** (Data Loss Prevention). Системы защиты от утечек: отслеживают и блокируют передачу конфиденциальных данных наружу. ➡️ [Внутренние угрозы](threats/07-insiders.md#как-защититься)
- <a id="dns"></a>**DNS** (Domain Name System). Система доменных имён, «телефонная книга» интернета: переводит имена сайтов в IP-адреса. ➡️ [Сеть](threats/04-network.md#подмена-dns)
- <a id="dnssec"></a>**DNSSEC**. Расширение DNS, которое добавляет к ответам цифровую подпись, чтобы их нельзя было подменить. ➡️ [Сеть](threats/04-network.md#как-защититься)
- <a id="dos"></a>**DoS** (Denial of Service). Атака «отказ в обслуживании»: сервис перестаёт работать для обычных пользователей. ➡️ [Сеть](threats/04-network.md#dos-и-ddos) 🔗 [NIST](https://csrc.nist.gov/glossary/term/denial_of_service)
- <a id="edr"></a>**EDR** (Endpoint Detection and Response). Система защиты компьютеров и серверов следующего поколения после антивируса: следит за поведением программ, обнаруживает атаки и помогает на них реагировать. ➡️ [APT](threats/08-apt.md#как-защититься)
- <a id="email-auth"></a>**SPF, DKIM, DMARC**. Три технологии проверки подлинности почты. Они помогают понять, действительно ли письмо отправлено с заявленного домена. ➡️ [Социальная инженерия](threats/02-social-engineering.md#как-защититься) 🔗 [CISA](https://www.cisa.gov/resources-tools/resources/phishing-guidance-stopping-attack-cycle-phase-one)
- <a id="evil-twin"></a>**Evil Twin** («злой двойник»). Поддельная точка доступа Wi-Fi с тем же названием, что у настоящей. ➡️ [Сеть](threats/04-network.md#перехват-трафика-mitm)
- <a id="fido2"></a>**FIDO2, passkeys** (ключи доступа). Стандарт входа без пароля с помощью аппаратного ключа или смартфона. Ключ привязан к адресу настоящего сайта, поэтому устойчив к фишингу. ➡️ [Учётные записи](threats/03-credentials.md#обход-многофакторной-аутентификации) 🔗 [CISA](https://www.cisa.gov/sites/default/files/publications/fact-sheet-implementing-phishing-resistant-mfa-508c.pdf)
- <a id="hsts"></a>**HSTS** (HTTP Strict Transport Security). Указание сайта браузеру всегда открывать его только по HTTPS. ➡️ [Сеть](threats/04-network.md#как-защититься)
- <a id="iaas-paas-saas"></a>**IaaS, PaaS, SaaS**. Модели облачных услуг. IaaS — аренда виртуальных серверов («инфраструктура»). PaaS — готовая платформа, например база данных. SaaS — готовое приложение, например почта или CRM. ➡️ [Облако](threats/09-cloud.md#модель-разделённой-ответственности)
- <a id="idor"></a>**IDOR** (Insecure Direct Object Reference). Небезопасная прямая ссылка на объект: сайт выдаёт документ по номеру и не проверяет, принадлежит ли он пользователю. ➡️ [Веб](threats/05-web.md#-idor-прямой-доступ-к-чужим-объектам)
- <a id="ioc"></a>**IoC** (Indicator of Compromise). Индикатор компрометации, «улика» атаки: хеш вредоносного файла, IP-адрес, домен. ➡️ [APT](threats/08-apt.md#ioc-и-ttp-почему-поведение-важнее-отпечатков) 🔗 [NIST](https://csrc.nist.gov/glossary/term/indicator_of_compromise)
- <a id="iot"></a>**IoT** (Internet of Things). Интернет вещей: «умные» устройства, подключённые к сети, например камеры, роутеры, датчики, бытовая техника. ➡️ [Мобильные и IoT](threats/10-mobile-iot.md)
- <a id="llm"></a>**LLM** (Large Language Model). Большая языковая модель, нейросеть для работы с текстом: ChatGPT, Claude, GigaChat и другие. ➡️ [ИИ](threats/11-ai.md#атаки-на-ии-системы)
- <a id="lotl"></a>**LotL** (Living off the Land, «жизнь за счёт системы»). Атака с использованием встроенных инструментов ОС вместо собственных вредоносов, чтобы не вызвать подозрений. ➡️ [APT](threats/08-apt.md#-volt-typhoon-20232024-жизнь-за-счёт-системы) 🔗 [CISA AA24-038A](https://www.cisa.gov/news-events/cybersecurity-advisories/aa24-038a)
- <a id="mfa"></a>**MFA** (Multi-Factor Authentication). Многофакторная аутентификация: для входа кроме пароля нужен ещё один фактор, например код, подтверждение на телефоне или аппаратный ключ. ➡️ [Учётные записи](threats/03-credentials.md#обход-многофакторной-аутентификации) 🔗 [NIST](https://csrc.nist.gov/glossary/term/multi_factor_authentication)
- <a id="mfa-fatigue"></a>**MFA fatigue** («усталость от MFA»). Атака, при которой жертву засыпают запросами на подтверждение входа, пока она не нажмёт «Да». ➡️ [Учётные записи](threats/03-credentials.md#обход-многофакторной-аутентификации) 🔗 [MITRE T1621](https://attack.mitre.org/techniques/T1621/)
- <a id="mitm"></a>**MITM** (Man-in-the-Middle, «человек посередине»). Атака, при которой злоумышленник незаметно встраивается между двумя сторонами связи. ➡️ [Сеть](threats/04-network.md#перехват-трафика-mitm) 🔗 [MITRE T1557](https://attack.mitre.org/techniques/T1557/)
- <a id="mitre-attack"></a>**MITRE ATT&CK**. Открытая база знаний о тактиках и техниках реальных атакующих. Общий язык специалистов по защите. ➡️ [APT](threats/08-apt.md#матрица-mitre-attck) 🔗 [attack.mitre.org](https://attack.mitre.org/)
- <a id="msp"></a>**MSP** (Managed Service Provider). Компания, которая на аутсорсе обслуживает ИТ других организаций. ➡️ [Цепочка поставок](threats/06-supply-chain.md)
- <a id="ot"></a>**OT, АСУ ТП** (Operational Technology; автоматизированные системы управления технологическим процессом). Компьютерные системы, которые управляют физическим оборудованием: заводами, энергосетями, водоснабжением. ➡️ [Мобильные и IoT](threats/10-mobile-iot.md#угрозы-для-iot)
- <a id="owasp"></a>**OWASP** (Open Worldwide Application Security Project). Некоммерческое сообщество по безопасности приложений, автор списков OWASP Top 10. ➡️ [Веб](threats/05-web.md#owasp-top-10) 🔗 [owasp.org](https://owasp.org/)
- <a id="pam"></a>**PAM** (Privileged Access Management). Системы управления привилегированным доступом: контролируют и записывают действия администраторов. ➡️ [APT](threats/08-apt.md#как-защититься)
- <a id="prompt-injection"></a>**Prompt injection** (внедрение инструкций). Атака на языковую модель: в текст, который она обрабатывает, вставляют инструкции, перехватывающие управление. ➡️ [ИИ](threats/11-ai.md#-prompt-injection-внедрение-инструкций) 🔗 [OWASP LLM01](https://genai.owasp.org/llmrisk/llm01-prompt-injection/)
- <a id="raas"></a>**RaaS** (Ransomware-as-a-Service). «Шифровальщик как услуга»: разработчики сдают шифровальщик в аренду «партнёрам» и получают долю выкупа. ➡️ [Вредоносное ПО](threats/01-malware.md#шифровальщики-подробнее)
- <a id="rag"></a>**RAG** (Retrieval-Augmented Generation). Подход, при котором языковая модель перед ответом ищет нужные документы в базе знаний. ➡️ [ИИ](threats/11-ai.md#owasp-top-10-для-llm)
- <a id="rat"></a>**RAT** (Remote Access Trojan). Троян удалённого доступа, который даёт злоумышленнику полное управление компьютером. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает)
- <a id="rpo-rto"></a>**RPO / RTO** (Recovery Point Objective / Recovery Time Objective). RPO — сколько данных (за какой период) допустимо потерять. RTO — за какое время сервис должен восстановиться. ➡️ [Непреднамеренные угрозы](threats/13-non-malicious.md#как-защититься)
- <a id="sast-dast"></a>**SAST / DAST** (Static / Dynamic Application Security Testing). Автоматический поиск уязвимостей. SAST анализирует исходный код, DAST атакует работающее приложение. ➡️ [Веб](threats/05-web.md#как-защититься)
- <a id="sbom"></a>**SBOM** (Software Bill of Materials). «Состав» программы: список всех её компонентов и библиотек с версиями. ➡️ [Цепочка поставок](threats/06-supply-chain.md#как-защититься) 🔗 [CISA: SBOM](https://www.cisa.gov/sbom)
- <a id="sca"></a>**SCA** (Software Composition Analysis). Анализ состава ПО: автоматический поиск уязвимых и вредоносных сторонних библиотек. ➡️ [Цепочка поставок](threats/06-supply-chain.md#как-защититься)
- <a id="siem"></a>**SIEM** (Security Information and Event Management). Система, которая собирает журналы событий со всех систем организации и ищет в них признаки атак. ➡️ [APT](threats/08-apt.md#как-защититься)
- <a id="sql"></a>**SQL** (Structured Query Language). Язык запросов к базам данных. ➡️ [Веб](threats/05-web.md#-sql-инъекция)
- <a id="sql-injection"></a>**SQL-инъекция** (SQL injection). Атака, при которой введённые пользователем данные выполняются как часть запроса к базе данных. ➡️ [Веб](threats/05-web.md#-sql-инъекция) 🔗 [CWE-89](https://cwe.mitre.org/data/definitions/89.html)
- <a id="ssrf"></a>**SSRF** (Server-Side Request Forgery). Подделка запроса на стороне сервера: злоумышленник заставляет сервер обратиться к внутренним ресурсам. ➡️ [Веб](threats/05-web.md#-ssrf-подделка-запроса-на-стороне-сервера) 🔗 [CWE-918](https://cwe.mitre.org/data/definitions/918.html)
- <a id="tls"></a>**TLS** (Transport Layer Security). Протокол шифрования соединений. Именно он делает HTTP защищённым HTTPS. ➡️ [Сеть](threats/04-network.md#перехват-трафика-mitm)
- <a id="ttp"></a>**TTP** (Tactics, Techniques, Procedures). Тактики, техники и процедуры, то есть характерный «почерк» группировки. ➡️ [APT](threats/08-apt.md#матрица-mitre-attck) 🔗 [NIST](https://csrc.nist.gov/glossary/term/tactics_techniques_and_procedures)
- <a id="ueba"></a>**UEBA** (User and Entity Behavior Analytics). Анализ поведения пользователей и устройств: система замечает отклонения от обычного поведения. ➡️ [Внутренние угрозы](threats/07-insiders.md#как-защититься)
- <a id="waf"></a>**WAF** (Web Application Firewall). Межсетевой экран для веб-приложений: фильтрует запросы к сайту и блокирует типовые атаки. ➡️ [Веб](threats/05-web.md#как-защититься)
- <a id="xss"></a>**XSS** (Cross-Site Scripting). Межсайтовый скриптинг: внедрение вредоносного JavaScript в страницы сайта. ➡️ [Веб](threats/05-web.md#-xss-межсайтовый-скриптинг) 🔗 [CWE-79](https://cwe.mitre.org/data/definitions/79.html)
- <a id="zero-click"></a>**Zero-click** (атака без клика). Заражение устройства без каких-либо действий пользователя. ➡️ [APT](threats/08-apt.md#реальные-случаи)

---

## А

- <a id="asset"></a>**Актив** (asset). Всё, что ценно для организации и требует защиты: данные, системы, оборудование, репутация. ➡️ [Базовые понятия](threats/00-basics.md) 🔗 [NIST](https://csrc.nist.gov/glossary/term/asset)
- <a id="amplification"></a>**Амплификация** (amplification, усиление). Приём DDoS-атак: маленький запрос к открытому серверу порождает в разы больший ответ, направленный жертве. ➡️ [Сеть](threats/04-network.md#dos-и-ddos)
- <a id="attack"></a>**Атака** (attack). Попытка реализовать угрозу, то есть получить несанкционированный доступ или причинить вред. ➡️ [Базовые понятия](threats/00-basics.md) 🔗 [NIST](https://csrc.nist.gov/glossary/term/attack)
- <a id="watering-hole"></a>**Атака «водопой»** (watering hole). Заражение сайта, который часто посещают намеченные жертвы. ➡️ [Социальная инженерия](threats/02-social-engineering.md#-другие-приёмы) 🔗 [MITRE T1189](https://attack.mitre.org/techniques/T1189/)
- <a id="supply-chain-attack"></a>**Атака на цепочку поставок** (supply chain attack). Атака на жертву через того, кому она доверяет: поставщика ПО, библиотеку, подрядчика. ➡️ [Цепочка поставок](threats/06-supply-chain.md) 🔗 [MITRE T1195](https://attack.mitre.org/techniques/T1195/)

## Б

- <a id="backdoor"></a>**Бэкдор** (backdoor, «чёрный ход»). Скрытый способ войти в систему в обход обычной защиты. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает) 🔗 [NIST](https://csrc.nist.gov/glossary/term/backdoor)
- <a id="fileless"></a>**Бесфайловое вредоносное ПО** (fileless malware). Вредонос, который работает в памяти и использует встроенные средства системы, не оставляя файлов на диске. ➡️ [Вредоносное ПО](threats/01-malware.md#бесфайловые-атаки)
- <a id="botnet"></a>**Ботнет** (botnet). Сеть заражённых устройств («ботов», «зомби»), которыми удалённо управляет злоумышленник. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает) 🔗 [NIST](https://csrc.nist.gov/glossary/term/botnet)
- <a id="brute-force"></a>**Брутфорс** (brute force, перебор). Подбор пароля перебором всех возможных вариантов. ➡️ [Учётные записи](threats/03-credentials.md#атаки-на-пароли) 🔗 [MITRE T1110](https://attack.mitre.org/techniques/T1110/)

## В

- <a id="vishing"></a>**Вишинг** (vishing, voice phishing). Телефонное мошенничество: звонки от имени банка, полиции, техподдержки. ➡️ [Социальная инженерия](threats/02-social-engineering.md#-фишинг-и-его-разновидности)
- <a id="wiper"></a>**Вайпер** (wiper). Вредонос, который безвозвратно уничтожает данные. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает) 🔗 [MITRE T1485](https://attack.mitre.org/techniques/T1485/)
- <a id="web-app"></a>**Веб-приложение** (web application). Программа, которая работает через браузер: сайт, интернет-банк, личный кабинет. ➡️ [Веб](threats/05-web.md)
- <a id="attack-vector"></a>**Вектор атаки** (attack vector). Путь, которым злоумышленник проникает в систему: письмо, уязвимый сайт, флешка. ➡️ [Базовые понятия](threats/00-basics.md#вектор-и-поверхность-атаки)
- <a id="virus"></a>**Вирус** (virus). Вредонос, который внедряет свой код в другие файлы и распространяется, когда их запускают. ➡️ [Вредоносное ПО](threats/01-malware.md#по-способу-распространения) 🔗 [NIST](https://csrc.nist.gov/glossary/term/virus)
- <a id="malware"></a>**Вредоносное ПО** (malware). Любая программа, созданная для причинения вреда: кражи, шифрования, уничтожения данных, слежки. ➡️ [Вредоносное ПО](threats/01-malware.md) 🔗 [NIST](https://csrc.nist.gov/glossary/term/malware)
- <a id="insider"></a>**Внутренняя угроза, инсайдер** (insider threat). Угроза от человека с легальным доступом: сотрудника, подрядчика, бывшего работника. ➡️ [Внутренние угрозы](threats/07-insiders.md) 🔗 [CISA](https://www.cisa.gov/topics/physical-security/insider-threat-mitigation/defining-insider-threats)

## Г

- <a id="hallucination"></a>**Галлюцинация** (hallucination). Уверенный, но ложный ответ языковой модели. ➡️ [ИИ](threats/11-ai.md#owasp-top-10-для-llm)
- <a id="lateral-movement"></a>**Горизонтальное перемещение** (lateral movement). Переход атакующего с одного захваченного компьютера на другие внутри сети. ➡️ [APT](threats/08-apt.md#14-тактик-enterprise-attck) 🔗 [MITRE TA0008](https://attack.mitre.org/tactics/TA0008/)

## Д

- <a id="double-extortion"></a>**Двойное вымогательство** (double extortion). Данные сначала крадут, а потом шифруют. Выкуп требуют и за расшифровку, и за то, чтобы данные не опубликовали. ➡️ [Вредоносное ПО](threats/01-malware.md#шифровальщики-подробнее)
- <a id="jailbreak"></a>**Джейлбрейк** (jailbreak) для ИИ. Приёмы, которые заставляют языковую модель обойти встроенные ограничения. ➡️ [ИИ](threats/11-ai.md#-prompt-injection-внедрение-инструкций)
- <a id="deepfake"></a>**Дипфейк** (deepfake). Поддельные видео, фото или голос, созданные нейросетью. ➡️ [ИИ](threats/11-ai.md#ии-в-руках-злоумышленников)
- <a id="availability"></a>**Доступность** (availability). Свойство информации быть доступной тем, кому она нужна, тогда, когда она нужна. ➡️ [Базовые понятия](threats/00-basics.md#триада-cia) 🔗 [NIST](https://csrc.nist.gov/glossary/term/availability)
- <a id="drive-by"></a>**Drive-by-загрузка** (drive-by download). Заражение устройства при простом посещении взломанного или вредоносного сайта. ➡️ [Вредоносное ПО](threats/01-malware.md#как-вредонос-попадает-на-устройство) 🔗 [MITRE T1189](https://attack.mitre.org/techniques/T1189/)

## З

- <a id="loader"></a>**Загрузчик** (loader, dropper). Вредонос, задача которого — скачать и установить другие вредоносы. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает)

## И

- <a id="ai"></a>**ИИ** (искусственный интеллект, AI). Системы, которые решают задачи, традиционно требующие человеческого интеллекта: понимание текста, распознавание изображений и другие. ➡️ [ИИ](threats/11-ai.md)
- <a id="ai-agent"></a>**ИИ-агент** (AI agent). Языковая модель, которой дали инструменты и право действовать: читать почту, открывать сайты, запускать программы. ➡️ [ИИ](threats/11-ai.md#атаки-на-ии-системы)

## К

- <a id="keylogger"></a>**Кейлоггер** (keylogger). Программа или устройство, которые записывают нажатия клавиш. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает) 🔗 [MITRE T1056.001](https://attack.mitre.org/techniques/T1056/001/)
- <a id="quishing"></a>**Квишинг** (quishing, QR phishing). Фишинг через поддельный QR-код. ➡️ [Социальная инженерия](threats/02-social-engineering.md#-фишинг-и-его-разновидности)
- <a id="confidentiality"></a>**Конфиденциальность** (confidentiality). Свойство информации быть доступной только тем, у кого есть на это право. ➡️ [Базовые понятия](threats/00-basics.md#триада-cia) 🔗 [NIST](https://csrc.nist.gov/glossary/term/confidentiality)
- <a id="session-hijacking"></a>**Кража сессии** (session hijacking). Захват уже установленного сеанса пользователя, обычно через кражу cookie сессии. ➡️ [Учётные записи](threats/03-credentials.md#кража-готовых-учётных-данных) 🔗 [MITRE T1539](https://attack.mitre.org/techniques/T1539/)
- <a id="cryptojacking"></a>**Криптоджекинг, криптомайнер** (cryptojacking). Тайная добыча криптовалюты на чужом оборудовании. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает) 🔗 [MITRE T1496](https://attack.mitre.org/techniques/T1496/)

## М

- <a id="password-manager"></a>**Менеджер паролей** (password manager). Программа, которая создаёт и хранит в зашифрованном виде уникальные пароли для каждого сервиса. ➡️ [Учётные записи](threats/03-credentials.md#как-защититься)
- <a id="firewall"></a>**Межсетевой экран, файрвол** (firewall). Средство, которое фильтрует сетевой трафик по заданным правилам. ➡️ [Сеть](threats/04-network.md#как-защититься) 🔗 [NIST](https://csrc.nist.gov/glossary/term/firewall)
- <a id="threat-model"></a>**Модель угроз** (threat model). Документ с перечнем актуальных угроз для конкретной системы. В России её составляют по методике ФСТЭК. ➡️ [Обзор угроз](threats/README.md#как-классифицируют-угрозы) 🔗 [Методика ФСТЭК](https://www.consultant.ru/document/cons_doc_LAW_378330/)
- <a id="threat-modeling"></a>**Моделирование угроз** (threat modeling). Систематический поиск того, что может пойти не так в системе, обычно ещё на этапе проектирования. ➡️ [Обзор угроз](threats/README.md#как-классифицируют-угрозы)
- <a id="shared-responsibility"></a>**Модель разделённой ответственности** (shared responsibility model). Распределение обязанностей по защите между облачным провайдером и клиентом. ➡️ [Облако](threats/09-cloud.md#модель-разделённой-ответственности)

## Н

- <a id="threat-actor"></a>**Нарушитель** (threat actor). Человек или группа, которые реализуют угрозу. ➡️ [Базовые понятия](threats/00-basics.md#кто-атакует)

## О

- <a id="cloud"></a>**Облако** (cloud). Вычислительные ресурсы (серверы, хранилища, программы), которые арендуют у провайдера через интернет. ➡️ [Облако](threats/09-cloud.md)
- <a id="data-poisoning"></a>**Отравление данных** (data poisoning). Подмешивание вредоносных примеров в данные для обучения модели ИИ. ➡️ [ИИ](threats/11-ai.md#-другие-атаки-на-модели)

## П

- <a id="pentest"></a>**Пентест** (penetration test, тестирование на проникновение). Легальная имитация атаки по договору с владельцем системы, чтобы найти уязвимости раньше злоумышленников. ➡️ [Веб](threats/05-web.md#как-защититься) 🔗 [NIST](https://csrc.nist.gov/glossary/term/penetration_testing)
- <a id="dependency-confusion"></a>**Подмена зависимостей** (dependency confusion). Публикация в открытом репозитории пакета с именем внутренней библиотеки компании, чтобы система сборки скачала его вместо настоящего. ➡️ [Цепочка поставок](threats/06-supply-chain.md#виды-атак)
- <a id="shoulder-surfing"></a>**Подглядывание через плечо** (shoulder surfing). Подсматривание пароля или данных на экране и клавиатуре. ➡️ [Физические угрозы](threats/12-physical.md#кража-и-подглядывание)
- <a id="fde"></a>**Полнодисковое шифрование** (full disk encryption). Шифрование всего диска устройства. Без пароля или ключа данные прочитать нельзя. ➡️ [Физические угрозы](threats/12-physical.md#как-защититься)
- <a id="attack-surface"></a>**Поверхность атаки** (attack surface). Все точки, через которые можно атаковать систему. ➡️ [Базовые понятия](threats/00-basics.md#вектор-и-поверхность-атаки) 🔗 [NIST](https://csrc.nist.gov/glossary/term/attack_surface)
- <a id="port"></a>**Порт** (port). Номер «двери», через которую сетевая служба принимает соединения, например 443 для HTTPS. ➡️ [Сеть](threats/04-network.md#сканирование-и-атаки-на-открытые-сервисы)
- <a id="pretexting"></a>**Претекстинг** (pretexting). Обман с помощью заранее придуманной правдоподобной легенды. ➡️ [Социальная инженерия](threats/02-social-engineering.md#-другие-приёмы)
- <a id="baiting"></a>**Приманка** (baiting). Подброшенная флешка или другая «наживка», рассчитанная на любопытство. ➡️ [Физические угрозы](threats/12-physical.md#-подброшенные-флешки-baiting)
- <a id="least-privilege"></a>**Принцип минимальных привилегий** (least privilege). Каждому пользователю и программе даётся ровно столько прав, сколько нужно для работы, и не больше. ➡️ [Внутренние угрозы](threats/07-insiders.md#как-защититься) 🔗 [NIST](https://csrc.nist.gov/glossary/term/least_privilege)

## Р

- <a id="password-spraying"></a>**Распыление паролей** (password spraying). Проверка одного популярного пароля на множестве учётных записей. ➡️ [Учётные записи](threats/03-credentials.md#атаки-на-пароли) 🔗 [MITRE T1110.003](https://attack.mitre.org/techniques/T1110/003/)
- <a id="threat-intelligence"></a>**Разведданные об угрозах** (threat intelligence, TI). Собранная и проанализированная информация о том, кто атакует, кого и какими методами. ➡️ [APT](threats/08-apt.md#как-защититься) 🔗 [NIST](https://csrc.nist.gov/glossary/term/threat_intelligence)
- <a id="backup-321"></a>**Резервное копирование, правило 3-2-1**. Не меньше 3 копий данных, на 2 разных типах носителей, 1 копия вне основной площадки или офлайн. ➡️ [Вредоносное ПО](threats/01-malware.md#как-защититься) 🔗 [CISA](https://www.cisa.gov/stopransomware/ransomware-guide)
- <a id="adware"></a>**Рекламное ПО** (adware). Программа, которая навязчиво показывает рекламу. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает)
- <a id="risk"></a>**Риск** (risk). Мера того, насколько вероятен вред и насколько он может быть велик. ➡️ [Базовые понятия](threats/00-basics.md) 🔗 [NIST](https://csrc.nist.gov/glossary/term/risk)
- <a id="rootkit"></a>**Руткит** (rootkit). Вредонос, который глубоко прячется в системе и скрывает себя и другие вредоносы. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает) 🔗 [NIST](https://csrc.nist.gov/glossary/term/rootkit)

## С

- <a id="segmentation"></a>**Сегментация сети** (network segmentation). Разделение сети на изолированные части, чтобы атака в одной не распространилась на остальные. ➡️ [Сеть](threats/04-network.md#как-защититься)
- <a id="sim-swap"></a>**SIM-свопинг** (SIM swapping). Мошеннический перевыпуск SIM-карты жертвы, чтобы получать её SMS-коды. ➡️ [Учётные записи](threats/03-credentials.md#обход-многофакторной-аутентификации)
- <a id="smishing"></a>**Смишинг** (smishing, SMS phishing). Фишинг через SMS и мессенджеры. ➡️ [Социальная инженерия](threats/02-social-engineering.md#-фишинг-и-его-разновидности)
- <a id="sniffing"></a>**Сниффинг** (sniffing). Перехват и анализ сетевого трафика. ➡️ [Сеть](threats/04-network.md#перехват-трафика-mitm) 🔗 [MITRE T1040](https://attack.mitre.org/techniques/T1040/)
- <a id="social-engineering"></a>**Социальная инженерия** (social engineering). Манипуляция людьми, чтобы они сами выдали информацию или выполнили нужное злоумышленнику действие. ➡️ [Социальная инженерия](threats/02-social-engineering.md) 🔗 [NIST](https://csrc.nist.gov/glossary/term/social_engineering)
- <a id="stalkerware"></a>**Сталкерское ПО** (stalkerware). Шпионская программа, которую тайно устанавливает на телефон знакомый человек. ➡️ [Мобильные и IoT](threats/10-mobile-iot.md#угрозы-для-смартфонов)
- <a id="infostealer"></a>**Стилер** (infostealer). Вредонос, который крадёт сохранённые пароли, cookie, данные карт и криптокошельков. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает)

## Т

- <a id="typosquatting"></a>**Тайпсквоттинг** (typosquatting). Регистрация доменов или пакетов с названиями, похожими на популярные, в расчёте на опечатку. ➡️ [Цепочка поставок](threats/06-supply-chain.md#виды-атак)
- <a id="tailgating"></a>**Тейлгейтинг** (tailgating). Проход в охраняемое помещение следом за сотрудником с пропуском. ➡️ [Физические угрозы](threats/12-physical.md#проникновение-в-помещения)
- <a id="tkui"></a>**Технический канал утечки информации, ТКУИ**. Путь утечки, при котором информацию перехватывают с помощью технических средств: акустика, побочные электромагнитные излучения и наводки (ПЭМИН), оптика. ➡️ [Физические угрозы](threats/12-physical.md#технические-каналы-утечки) 🔗 [ГОСТ Р 51275-2006 (термины ПЭМИН)](https://docs.cntd.ru/document/1200057516)
- <a id="trojan"></a>**Троян** (Trojan horse). Вредонос, который маскируется под полезную программу. ➡️ [Вредоносное ПО](threats/01-malware.md#по-способу-распространения) 🔗 [NIST](https://csrc.nist.gov/glossary/term/trojan_horse)
- <a id="threat-hunting"></a>**Threat hunting** (проактивный поиск угроз). Поиск следов атакующих в сети специалистами, без ожидания срабатывания защиты. ➡️ [APT](threats/08-apt.md#как-защититься)

## У

- <a id="threat"></a>**Угроза** (threat). Совокупность условий и факторов, создающих потенциальную или реально существующую опасность нарушения безопасности информации (ГОСТ Р 50922-2006). ➡️ [Базовые понятия](threats/00-basics.md) 🔗 [ГОСТ Р 50922-2006](https://docs.cntd.ru/document/1200058320) · [NIST](https://csrc.nist.gov/glossary/term/threat)
- <a id="vulnerability"></a>**Уязвимость** (vulnerability). Слабое место системы, которое можно использовать для реализации угрозы. ➡️ [Базовые понятия](threats/00-basics.md) 🔗 [NIST](https://csrc.nist.gov/glossary/term/vulnerability)
- <a id="zero-day"></a>**Уязвимость нулевого дня** (zero-day, 0-day). Уязвимость, для которой ещё нет исправления от производителя. ➡️ [Базовые понятия](threats/00-basics.md) 🔗 [NIST](https://csrc.nist.gov/glossary/term/zero_day_attack)
- <a id="credentials"></a>**Учётные данные** (credentials). То, чем подтверждается личность при входе: логин, пароль, токен, ключ. ➡️ [Учётные записи](threats/03-credentials.md)
- <a id="whaling"></a>**Уэйлинг** (whaling). Целевой фишинг против руководителей. ➡️ [Социальная инженерия](threats/02-social-engineering.md#-фишинг-и-его-разновидности)

## Ф

- <a id="phishing"></a>**Фишинг** (phishing). Поддельные сообщения от имени доверенных организаций или людей, цель которых — выманить данные или заставить открыть вредоносный файл. ➡️ [Социальная инженерия](threats/02-social-engineering.md) 🔗 [NIST](https://csrc.nist.gov/glossary/term/phishing) · [MITRE T1566](https://attack.mitre.org/techniques/T1566/)

## Х

- <a id="hacktivism"></a>**Хактивизм** (hacktivism). Кибератаки по политическим или идеологическим мотивам. ➡️ [Базовые понятия](threats/00-basics.md#кто-атакует)
- <a id="hash"></a>**Хеш** (hash). Короткий «отпечаток» данных, полученный необратимым преобразованием. Пароли в базах хранят в виде хешей. ➡️ [Учётные записи](threats/03-credentials.md#атаки-на-пароли) 🔗 [NIST](https://csrc.nist.gov/glossary/term/hash_function)

## Ц

- <a id="integrity"></a>**Целостность** (integrity). Свойство информации оставаться неизменённой без разрешения. ➡️ [Базовые понятия](threats/00-basics.md#триада-cia) 🔗 [NIST](https://csrc.nist.gov/glossary/term/integrity)
- <a id="spear-phishing"></a>**Целевой фишинг** (spear phishing). Фишинговое сообщение, подготовленное под конкретного человека или организацию. ➡️ [Социальная инженерия](threats/02-social-engineering.md#-фишинг-и-его-разновидности) 🔗 [MITRE T1566](https://attack.mitre.org/techniques/T1566/)

## Ч

- <a id="worm"></a>**Червь** (worm). Вредонос, который сам распространяется по сети без участия человека. ➡️ [Вредоносное ПО](threats/01-malware.md#по-способу-распространения) 🔗 [NIST](https://csrc.nist.gov/glossary/term/worm)

## Ш

- <a id="ransomware"></a>**Шифровальщик** (ransomware, программа-вымогатель). Вредонос, который шифрует данные и требует выкуп за их расшифровку. ➡️ [Вредоносное ПО](threats/01-malware.md#шифровальщики-подробнее) 🔗 [CISA](https://www.cisa.gov/stopransomware)
- <a id="spyware"></a>**Шпионское ПО** (spyware). Программа, которая тайно собирает информацию о пользователе. ➡️ [Вредоносное ПО](threats/01-malware.md#по-тому-что-делает) 🔗 [NIST](https://csrc.nist.gov/glossary/term/spyware)

## Э

- <a id="exploit"></a>**Эксплойт** (exploit). Программа или приём, которые используют конкретную уязвимость. ➡️ [Базовые понятия](threats/00-basics.md)
- <a id="exfiltration"></a>**Эксфильтрация** (exfiltration). Скрытый вывод украденных данных из сети жертвы. ➡️ [APT](threats/08-apt.md#14-тактик-enterprise-attck) 🔗 [MITRE TA0010](https://attack.mitre.org/tactics/TA0010/)

---

<div align="center">

[🏠 Главная](README.md) · [⚠️ Угрозы](threats/README.md) · [📚 Источники](SOURCES.md)

</div>
