[🏠 Главная](../README.md) › [⚠️ Угрозы](README.md) › 🕸️ Атаки на веб-приложения

# 🕸️ Атаки на веб-приложения

**[Веб-приложение](../glossary.md#web-app)** — любой сайт или сервис, который работает в браузере: интернет-банк, магазин, CRM, личный кабинет. Обычно такие приложения доступны всему интернету, поэтому их атакуют постоянно.

## Содержание

- [OWASP Top 10](#owasp-top-10)
- [Самые известные атаки подробнее](#самые-известные-атаки-подробнее)
- [Реальные случаи](#реальные-случаи)
- [Как защититься](#как-защититься)
- [Источники](#источники)

---

## OWASP Top 10

**[OWASP](../glossary.md#owasp)** (Open Worldwide Application Security Project) — некоммерческое сообщество, которое составляет главный в отрасли список **10 самых критичных рисков** для веб-приложений. Актуальная версия — **OWASP Top 10:2025**. [[OWASP Top 10:2025]](https://owasp.org/Top10/2025/)

| # | Риск | 💡 Простыми словами |
|:-:|---|---|
| A01 | [Broken Access Control](https://owasp.org/Top10/2025/A01_2025-Broken_Access_Control/) — нарушение контроля доступа | Пользователь видит или делает то, что ему не положено: например, меняет в адресе `id=100` на `id=101` и видит чужой заказ |
| A02 | [Security Misconfiguration](https://owasp.org/Top10/2025/A02_2025-Security_Misconfiguration/) — ошибки настройки | Включена отладка, открыта админ-панель, стоят пароли по умолчанию |
| A03 | [Software Supply Chain Failures](https://owasp.org/Top10/2025/A03_2025-Software_Supply_Chain_Failures/) — сбои в цепочке поставок ПО | Уязвимые или заражённые библиотеки и инструменты сборки. Подробнее в разделе [📦 Цепочка поставок](06-supply-chain.md) |
| A04 | [Cryptographic Failures](https://owasp.org/Top10/2025/A04_2025-Cryptographic_Failures/) — ошибки криптографии | Данные не зашифрованы или зашифрованы устаревшим алгоритмом, пароли хранятся открытым текстом |
| A05 | [Injection](https://owasp.org/Top10/2025/A05_2025-Injection/) — инъекции | Ввод пользователя выполняется как команда: SQL-инъекции, XSS |
| A06 | [Insecure Design](https://owasp.org/Top10/2025/A06_2025-Insecure_Design/) — небезопасная архитектура | Ошибка в самой логике: например, восстановление пароля по «секретному вопросу», ответ на который легко найти |
| A07 | [Authentication Failures](https://owasp.org/Top10/2025/A07_2025-Authentication_Failures/) — ошибки аутентификации | Нет защиты от перебора, слабые пароли разрешены, сессия не завершается |
| A08 | [Software or Data Integrity Failures](https://owasp.org/Top10/2025/A08_2025-Software_or_Data_Integrity_Failures/) — нарушение целостности ПО и данных | Приложение доверяет обновлениям или данным без проверки подписи |
| A09 | [Security Logging and Alerting Failures](https://owasp.org/Top10/2025/A09_2025-Security_Logging_and_Alerting_Failures/) — недостатки журналирования и оповещения | Атака идёт, но никто не видит: нет журналов, никто не получает тревог |
| A10 | [Mishandling of Exceptional Conditions](https://owasp.org/Top10/2025/A10_2025-Mishandling_of_Exceptional_Conditions/) — неправильная обработка ошибок | При сбое приложение «открывается» вместо того, чтобы закрыться, или показывает внутренние подробности |

> [!NOTE]
> В версии 2025 появились две новые категории: **A03** (цепочка поставок) и **A10** (обработка ошибок). Атака **[SSRF](../glossary.md#ssrf)**, которая в версии 2021 была отдельным пунктом, теперь входит в A01. [[OWASP Top 10:2025]](https://owasp.org/Top10/2025/)

---

## Самые известные атаки подробнее

### 💉 SQL-инъекция

**[SQL](../glossary.md#sql)** — язык запросов к базам данных. **[SQL-инъекция](../glossary.md#sql-injection)** возникает, когда сайт вставляет то, что ввёл пользователь, прямо в запрос к базе.

⚙️ Пример. Сайт ищет пользователя так:
```sql
SELECT * FROM users WHERE login = 'ВВОД_ПОЛЬЗОВАТЕЛЯ'
```
Если в поле логина ввести `' OR '1'='1`, условие станет всегда истинным, и база вернёт всех пользователей. С помощью инъекции злоумышленник может прочитать, изменить или удалить всю базу.

🛡️ Защита: **параметризованные запросы**, в которых ввод пользователя никогда не становится частью кода запроса. [[OWASP: SQL Injection Prevention Cheat Sheet]](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html) · [[CWE-89]](https://cwe.mitre.org/data/definitions/89.html)

### 📜 XSS: межсайтовый скриптинг

**[XSS](../glossary.md#xss)** (Cross-Site Scripting). Злоумышленник внедряет на страницу сайта свой код на JavaScript. Код выполняется в браузерах других посетителей и может украсть cookie сессии, перенаправить на фишинговую страницу или действовать от имени пользователя.

⚙️ Пример: в комментарии на форуме пишут `<script>отправить_cookie_злоумышленнику()</script>`. Если сайт не обезвредил этот код, он запустится у каждого, кто откроет страницу.

🛡️ Защита: экранирование вывода, **[CSP](../glossary.md#csp)** (политика безопасности контента, которая запрещает браузеру выполнять посторонние скрипты), cookie с флагом `HttpOnly`. [[OWASP: XSS Prevention Cheat Sheet]](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html) · [[CWE-79]](https://cwe.mitre.org/data/definitions/79.html)

### 🔁 CSRF: подделка межсайтового запроса

**[CSRF](../glossary.md#csrf)** (Cross-Site Request Forgery). Вы вошли в интернет-банк и в другой вкладке открыли сайт злоумышленника. Этот сайт незаметно отправляет в банк запрос «перевести деньги», и браузер автоматически прикладывает к нему вашу cookie сессии.

🛡️ Защита: CSRF-токены (секретное значение в каждой форме), атрибут cookie `SameSite`. [[OWASP: CSRF Prevention Cheat Sheet]](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html) · [[CWE-352]](https://cwe.mitre.org/data/definitions/352.html)

### 🎯 SSRF: подделка запроса на стороне сервера

**[SSRF](../glossary.md#ssrf)** (Server-Side Request Forgery). Злоумышленник заставляет сервер сделать запрос туда, куда сам злоумышленник попасть не может: во внутреннюю сеть или к служебному адресу облака, где хранятся ключи доступа.

⚙️ Пример: сервис «загрузить картинку по ссылке» получает вместо картинки внутренний адрес `http://169.254.169.254/...`. Это служебный адрес облачного сервера, по которому он выдаёт свои секретные ключи.

🔗 [[OWASP: SSRF Prevention Cheat Sheet]](https://cheatsheetseries.owasp.org/cheatsheets/Server_Side_Request_Forgery_Prevention_Cheat_Sheet.html) · [[CWE-918]](https://cwe.mitre.org/data/definitions/918.html)

### 🔓 IDOR: прямой доступ к чужим объектам

**[IDOR](../glossary.md#idor)** (Insecure Direct Object Reference) — частный случай A01. Сайт показывает документ по номеру из адреса (`/invoice?id=1001`) и не проверяет, ваш ли это документ. Достаточно перебрать номера, чтобы скачать документы всех клиентов. [[OWASP: IDOR Prevention Cheat Sheet]](https://cheatsheetseries.owasp.org/cheatsheets/Insecure_Direct_Object_Reference_Prevention_Cheat_Sheet.html)

🏷️ **MITRE ATT&CK** для всех атак на публичные приложения: [T1190 Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)

---

## Реальные случаи

### 📰 Equifax (2017): необновлённая библиотека

Злоумышленники проникли в системы бюро кредитных историй Equifax через известную уязвимость во фреймворке Apache Struts ([CVE-2017-5638](https://nvd.nist.gov/vuln/detail/CVE-2017-5638)). Исправление вышло за два месяца до взлома, но его не установили. По данным Счётной палаты США (GAO), утекли персональные данные более 145 млн человек.
🔗 [US GAO: Actions Taken by Equifax (GAO-18-559)](https://www.gao.gov/products/gao-18-559)

### 📰 Capital One (2019): SSRF в облаке

Бывшая сотрудница облачного провайдера воспользовалась неправильно настроенным межсетевым экраном веб-приложений банка Capital One. Через SSRF она получила облачные ключи доступа и скачала данные более 100 млн клиентов.
🔗 [US DOJ: Former Seattle tech worker convicted](https://www.justice.gov/usao-wdwa/pr/former-seattle-tech-worker-convicted-wire-fraud-and-computer-intrusions)

---

## Как защититься

| 🛡️ Мера | Против чего |
|---|---|
| **Проверять права на каждом запросе на стороне сервера**, а не только скрывать кнопки в интерфейсе | A01, IDOR |
| **Параметризованные запросы, экранирование вывода, CSP** | Инъекции, XSS |
| **Обновлять фреймворки и библиотеки**, отслеживать уязвимости в зависимостях (**[SCA](../glossary.md#sca)**) | A03, случай Equifax |
| **Безопасная разработка**: моделирование угроз, код-ревью, автоматическое тестирование (**[SAST/DAST](../glossary.md#sast-dast)**) | A06 и всё остальное |
| **[WAF](../glossary.md#waf)** (межсетевой экран для веб-приложений) | Часть типовых атак. Это дополнительный уровень защиты, а не замена исправлению кода |
| **Журналирование и оповещения** о подозрительной активности | A09 |
| **Регулярный [пентест](../glossary.md#pentest)** (тестирование на проникновение) | Находит уязвимости раньше злоумышленников |

[[OWASP Cheat Sheet Series]](https://cheatsheetseries.owasp.org/) · [[OWASP ASVS]](https://owasp.org/www-project-application-security-verification-standard/)

---

## Источники

- [OWASP Top 10:2025](https://owasp.org/Top10/2025/)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
- [OWASP Application Security Verification Standard (ASVS)](https://owasp.org/www-project-application-security-verification-standard/)
- [MITRE CWE: CWE-89 SQL Injection](https://cwe.mitre.org/data/definitions/89.html)
- [MITRE CWE: CWE-79 XSS](https://cwe.mitre.org/data/definitions/79.html)
- [MITRE CWE: CWE-352 CSRF](https://cwe.mitre.org/data/definitions/352.html)
- [MITRE CWE: CWE-918 SSRF](https://cwe.mitre.org/data/definitions/918.html)
- [MITRE ATT&CK: T1190](https://attack.mitre.org/techniques/T1190/)
- [NVD: CVE-2017-5638](https://nvd.nist.gov/vuln/detail/CVE-2017-5638)
- [GAO-18-559: Equifax](https://www.gao.gov/products/gao-18-559)
- [US DOJ: Capital One case](https://www.justice.gov/usao-wdwa/pr/former-seattle-tech-worker-convicted-wire-fraud-and-computer-intrusions)

---

<div align="center">

[← 🌐 Сетевые атаки](04-network.md) · [🏠 Главная](../README.md) · [Далее: 📦 Цепочка поставок →](06-supply-chain.md)

</div>
