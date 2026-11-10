[🏠 Главная](../README.md) › [⚠️ Угрозы](README.md) › 🔑 Атаки на учётные записи

# 🔑 Атаки на учётные записи

**[Учётные данные](../glossary.md#credentials)** (credentials) — это то, чем вы подтверждаете, что вы — это вы: логин, пароль, одноразовый код, **[cookie сессии](../glossary.md#cookie)**. Злоумышленнику проще войти с чужим настоящим паролем, чем взламывать систему. Для системы защиты такой вход выглядит как обычная работа сотрудника.

🏷️ **MITRE ATT&CK:** [T1078 Valid Accounts](https://attack.mitre.org/techniques/T1078/) · тактика [Credential Access (TA0006)](https://attack.mitre.org/tactics/TA0006/)

## Содержание

- [Атаки на пароли](#атаки-на-пароли)
- [Кража готовых учётных данных](#кража-готовых-учётных-данных)
- [Обход многофакторной аутентификации](#обход-многофакторной-аутентификации)
- [Реальные случаи](#реальные-случаи)
- [Как защититься](#как-защититься)
- [Источники](#источники)

---

## Атаки на пароли

| Атака | 💡 Простыми словами | 🏷️ ATT&CK |
|---|---|---|
| **[Перебор (брутфорс)](../glossary.md#brute-force)** (brute force) | Пробовать все варианты подряд: `aaaa`, `aaab`, ... | [T1110](https://attack.mitre.org/techniques/T1110/) |
| **Подбор по словарю** (password guessing) | Пробовать популярные пароли: `123456`, `qwerty`, `Password1` | [T1110.001](https://attack.mitre.org/techniques/T1110/001/) |
| **[Распыление паролей](../glossary.md#password-spraying)** (password spraying) | Один популярный пароль пробуют на тысячах учётных записей. Блокировка после нескольких ошибок не срабатывает, потому что на каждую учётку приходится одна попытка | [T1110.003](https://attack.mitre.org/techniques/T1110/003/) |
| **[Credential stuffing](../glossary.md#credential-stuffing)** («набивка» учётных данных) | Пары «логин–пароль» из утечки одного сайта пробуют на других. Работает, потому что люди используют один пароль везде | [T1110.004](https://attack.mitre.org/techniques/T1110/004/) |
| **Взлом хешей** (password cracking) | Пароли в базах хранятся в виде **[хешей](../glossary.md#hash)** (необратимых «отпечатков»). Если база утекла, хеши подбирают на своих мощных компьютерах без ограничений на число попыток | [T1110.002](https://attack.mitre.org/techniques/T1110/002/) |
| **Пароли по умолчанию** (default credentials) | Заводской пароль `admin/admin` на роутере, камере, сервере, который никто не сменил | [T1078.001](https://attack.mitre.org/techniques/T1078/001/) |

---

## Кража готовых учётных данных

Пароль не обязательно подбирать, его можно украсть:

- **[Фишинг](02-social-engineering.md).** Человек сам вводит пароль на поддельном сайте.
- **[Стилеры](01-malware.md#по-тому-что-делает).** Вредонос забирает все сохранённые в браузере пароли и cookie. Собранные данные (логи стилеров) продают на теневых площадках.
- **Утечки баз данных.** Базы взломанных сайтов публикуют или продают. Проверить, была ли ваша почта в утечках, можно на [Have I Been Pwned](https://haveibeenpwned.com/).
- **[Кража сессии](../glossary.md#session-hijacking)** (session hijacking). После входа сайт выдаёт браузеру cookie сессии, своего рода «пропуск», чтобы не спрашивать пароль снова. Если украсть этот пропуск, можно войти без пароля и без второго фактора. [[MITRE T1539]](https://attack.mitre.org/techniques/T1539/)
- **Pass-the-Hash.** Во внутренней сети Windows для входа иногда достаточно хеша пароля, знать сам пароль не нужно. [[MITRE T1550.002]](https://attack.mitre.org/techniques/T1550/002/)

---

## Обход многофакторной аутентификации

**[MFA](../glossary.md#mfa)** (Multi-Factor Authentication, многофакторная аутентификация) — вход, для которого кроме пароля нужен ещё один фактор: код из SMS или приложения, подтверждение на телефоне, аппаратный ключ. MFA резко усложняет взлом, но её тоже научились обходить:

| Приём | ⚙️ Как работает | 🏷️ ATT&CK |
|---|---|---|
| **[MFA fatigue](../glossary.md#mfa-fatigue)** («усталость от MFA», MFA bombing) | Злоумышленник знает пароль и раз за разом отправляет запрос на подтверждение входа. Жертва в итоге нажимает «Да», чтобы уведомления прекратились | [T1621](https://attack.mitre.org/techniques/T1621/) |
| **[AiTM-фишинг](../glossary.md#aitm)** (Adversary-in-the-Middle) | Фишинговый сайт работает как посредник: передаёт настоящему сайту и пароль, и одноразовый код, а себе забирает cookie сессии | [T1557](https://attack.mitre.org/techniques/T1557/) |
| **[SIM-свопинг](../glossary.md#sim-swap)** (SIM swapping) | Мошенник убеждает оператора связи перевыпустить SIM-карту жертвы на себя и получает все её SMS-коды | [T1451 (Mobile)](https://attack.mitre.org/techniques/T1451/) |
| **Выманивание кода** | «Продиктуйте код из SMS, это для отмены операции» | [T1111](https://attack.mitre.org/techniques/T1111/) |

> [!TIP]
> Против всех этих приёмов защищают **ключи FIDO2 и passkeys** (ключи доступа). Они криптографически привязаны к адресу настоящего сайта и не сработают на поддельном. Код вводить не нужно, поэтому его нельзя выманить. [[CISA: Phishing-Resistant MFA]](https://www.cisa.gov/sites/default/files/publications/fact-sheet-implementing-phishing-resistant-mfa-508c.pdf)

---

## Реальные случаи

### 📰 Uber (сентябрь 2022): MFA fatigue

Злоумышленник получил пароль подрядчика и засыпал его запросами на подтверждение входа. В итоге подрядчик подтвердил вход, и атакующий получил доступ к внутренним системам компании.
🔗 [Uber Newsroom: Security update](https://www.uber.com/newsroom/security-update/)

### 📰 Snowflake (2024): пароли из стилеров и вход без MFA

Группировка UNC5537 входила в клиентские аккаунты облачной платформы данных Snowflake по учётным данным, украденным стилерами, иногда несколько лет назад. На этих аккаунтах не было MFA. Затем злоумышленники выгружали данные и вымогали деньги. Пострадали около 165 организаций. Сама платформа Snowflake взломана не была.
🔗 [Google Cloud / Mandiant: UNC5537 Targets Snowflake Customer Instances](https://cloud.google.com/blog/topics/threat-intelligence/unc5537-snowflake-data-theft-extortion)

### 📰 23andMe (2023): credential stuffing

Злоумышленники вошли в аккаунты сервиса генетических тестов, используя пароли из утечек с других сайтов. Через функцию «родственники» они получили данные о миллионах других пользователей.
🔗 [23andMe: Addressing Data Security Concerns](https://blog.23andme.com/articles/addressing-data-security-concerns)

---

## Как защититься

| 🛡️ Мера | Против чего |
|---|---|
| **Уникальный пароль для каждого сервиса** и **[менеджер паролей](../glossary.md#password-manager)** | Credential stuffing |
| **Длинные пароли или фразы** (15 символов и больше). NIST рекомендует длину, а не обязательные «спецсимволы» и регулярную смену без причины | Перебор, словари |
| **MFA везде**, особенно на почте, VPN и в облаке. Лучше всего ключи FIDO2 или passkeys | Почти все атаки из этого раздела |
| **Number matching**: при подтверждении входа ввести число с экрана, а не просто нажать «Да» | MFA fatigue |
| **Блокировка или задержка после неудачных попыток**, мониторинг входов из необычных мест | Перебор, распыление |
| **Сменить пароли по умолчанию** на всех устройствах | Вход с заводскими паролями |
| **Проверка паролей по базам утечек** при их создании | Использование уже скомпрометированных паролей |
| **Запрет на перевыпуск SIM без личного визита** (услуга у операторов) | SIM-свопинг |

[[NIST SP 800-63B-4]](https://pages.nist.gov/800-63-4/sp800-63b.html)

---

## Источники

- [MITRE ATT&CK: T1110 Brute Force](https://attack.mitre.org/techniques/T1110/)
- [MITRE ATT&CK: T1078 Valid Accounts](https://attack.mitre.org/techniques/T1078/)
- [MITRE ATT&CK: T1621 Multi-Factor Authentication Request Generation](https://attack.mitre.org/techniques/T1621/)
- [MITRE ATT&CK: T1539 Steal Web Session Cookie](https://attack.mitre.org/techniques/T1539/)
- [NIST SP 800-63B-4. Authentication and Authenticator Management](https://pages.nist.gov/800-63-4/sp800-63b.html)
- [CISA: Implementing Phishing-Resistant MFA](https://www.cisa.gov/sites/default/files/publications/fact-sheet-implementing-phishing-resistant-mfa-508c.pdf)
- [Microsoft: AiTM phishing campaign](https://www.microsoft.com/en-us/security/blog/2022/07/12/from-cookie-theft-to-bec-attackers-use-aitm-phishing-sites-as-entry-point-to-further-financial-fraud/)
- [Uber: Security update (2022)](https://www.uber.com/newsroom/security-update/)
- [Mandiant: UNC5537 / Snowflake](https://cloud.google.com/blog/topics/threat-intelligence/unc5537-snowflake-data-theft-extortion)
- [23andMe: Addressing Data Security Concerns](https://blog.23andme.com/articles/addressing-data-security-concerns)
- [Have I Been Pwned](https://haveibeenpwned.com/)

---

<div align="center">

[← 🎣 Социальная инженерия](02-social-engineering.md) · [🏠 Главная](../README.md) · [Далее: 🌐 Сетевые атаки →](04-network.md)

</div>
