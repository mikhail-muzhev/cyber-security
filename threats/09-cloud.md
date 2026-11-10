[🏠 Главная](../README.md) › [⚠️ Угрозы](README.md) › ☁️ Угрозы в облаке

# ☁️ Угрозы в облаке

**[Облако](../glossary.md#cloud)** — чужие серверы, которые вы арендуете через интернет: Yandex Cloud, VK Cloud, AWS, Azure, Google Cloud. Облака у крупных провайдеров обычно защищены очень хорошо. Большинство инцидентов происходит **не из-за взлома провайдера, а из-за ошибок клиента**.

## Содержание

- [Модель разделённой ответственности](#модель-разделённой-ответственности)
- [Главные угрозы](#главные-угрозы)
- [Реальные случаи](#реальные-случаи)
- [Как защититься](#как-защититься)
- [Источники](#источники)

---

## Модель разделённой ответственности

**[Модель разделённой ответственности](../glossary.md#shared-responsibility)** (shared responsibility model) определяет, что защищает провайдер, а что клиент. Граница зависит от типа услуги.

| Что защищать | **[IaaS](../glossary.md#iaas-paas-saas)** (виртуальные серверы) | **PaaS** (платформа, например управляемая база данных) | **SaaS** (готовое приложение, например почта) |
|---|:-:|:-:|:-:|
| Данные и доступ к ним | 👤 Клиент | 👤 Клиент | 👤 Клиент |
| Учётные записи и права | 👤 Клиент | 👤 Клиент | 👤 Клиент |
| Приложение | 👤 Клиент | 👤 Клиент | ☁️ Провайдер |
| ОС и её обновления | 👤 Клиент | ☁️ Провайдер | ☁️ Провайдер |
| Серверы, сеть, дата-центр | ☁️ Провайдер | ☁️ Провайдер | ☁️ Провайдер |

> [!IMPORTANT]
> **Данные и доступ к ним — всегда ответственность клиента.** Если вы открыли хранилище всему интернету, провайдер не виноват.

[[Microsoft: Shared responsibility in the cloud]](https://learn.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility) · [[AWS: Shared Responsibility Model]](https://aws.amazon.com/compliance/shared-responsibility-model/)

---

## Главные угрозы

| Угроза | 💡 Что происходит | 🏷️ ATT&CK |
|---|---|---|
| ⚙️ **Ошибки настройки** (misconfiguration) | Хранилище файлов открыто всему интернету, база данных доступна без пароля, отключено журналирование | [T1530](https://attack.mitre.org/techniques/T1530/) |
| 🔑 **Утечка ключей доступа** | Ключ **[API](../glossary.md#api)** (программного доступа к облаку) попал в публичный репозиторий кода, в мобильное приложение или в чат | [T1552.001](https://attack.mitre.org/techniques/T1552/001/) |
| 👑 **Избыточные права** | У сервисов и людей больше прав, чем нужно. Одна взломанная учётка открывает всё облако | [T1078.004](https://attack.mitre.org/techniques/T1078/004/) |
| 👤 **Захват учётной записи** | Вход в консоль управления облаком по украденному паролю без MFA | [T1078.004](https://attack.mitre.org/techniques/T1078/004/) |
| 🎯 **Кража ключей через сервис метаданных** | Через уязвимость [SSRF](05-web.md#-ssrf-подделка-запроса-на-стороне-сервера) у сервера запрашивают его временные ключи | [T1552.005](https://attack.mitre.org/techniques/T1552/005/) |
| ⛏️ **Скрытый майнинг** | Злоумышленник запускает на ваш счёт сотни серверов для добычи криптовалюты | [T1496](https://attack.mitre.org/techniques/T1496/) |
| 🌫️ **Нехватка видимости** | Компания не знает, какие ресурсы у неё есть в облаке («теневое ИТ»), и не замечает атаку | — |

Ошибки настройки и управления, а также слабое управление учётными записями и доступом стоят в начале списка главных облачных угроз Cloud Security Alliance. [[CSA: Top Threats to Cloud Computing 2024]](https://cloudsecurityalliance.org/artifacts/top-threats-to-cloud-computing-2024)

---

## Реальные случаи

### 📰 Microsoft AI Research (2023): слишком широкая ссылка доступа

Исследователи Microsoft выложили на GitHub ссылку для скачивания моделей ИИ. Ссылка содержала токен **SAS** (подписанный адрес доступа к хранилищу Azure), который давал доступ ко всему хранилищу, а не к отдельным файлам. В открытом доступе оказались 38 ТБ внутренних данных, включая резервные копии компьютеров сотрудников. Проблему нашли исследователи компании Wiz.
🔗 [MSRC: Microsoft mitigated exposure of internal information](https://msrc.microsoft.com/blog/2023/09/microsoft-mitigated-exposure-of-internal-information-in-a-storage-account-due-to-overly-permissive-sas-token/) · [Wiz Research](https://www.wiz.io/blog/38-terabytes-of-private-data-accidentally-exposed-by-microsoft-ai-researchers)

### 📰 Snowflake (2024): учётные записи без MFA

Около 165 клиентов облачной платформы данных пострадали из-за входа по украденным паролям без второго фактора. Подробнее в разделе [🔑 Атаки на учётные записи](03-credentials.md#-snowflake-2024-пароли-из-стилеров-и-вход-без-mfa).
🔗 [Mandiant: UNC5537](https://cloud.google.com/blog/topics/threat-intelligence/unc5537-snowflake-data-theft-extortion)

### 📰 Capital One (2019): SSRF и облачные ключи

Через неправильно настроенный межсетевой экран злоумышленница получила временные ключи облачного сервера и скачала данные более 100 млн клиентов. Подробнее в разделе [🕸️ Веб-приложения](05-web.md#-capital-one-2019-ssrf-в-облаке).

---

## Как защититься

| 🛡️ Мера | 💡 Суть |
|---|---|
| **MFA для всех учётных записей**, особенно для администраторов и root | Самая эффективная мера против захвата учётных записей |
| **Минимальные права** (IAM, Identity and Access Management — система управления доступом) | Регулярно пересматривайте права и удаляйте лишние |
| **Не хранить ключи в коде.** Используйте менеджеры секретов, временные ключи, **сканирование секретов** в репозиториях | Утечка ключей |
| **[CSPM](../glossary.md#cspm)** (Cloud Security Posture Management) | Инструмент, который автоматически находит ошибки настройки облака |
| **Запрет публичного доступа к хранилищам** на уровне всей организации | Открытые бакеты (хранилища файлов) |
| **Защищённая версия сервиса метаданных** (например, IMDSv2 в AWS) | Кража ключей через SSRF |
| **Журналирование всех действий** и оповещения | Обнаружение атаки и расследование |
| **Бюджетные оповещения** | Резкий рост счёта — признак скрытого майнинга |

[[CSA: Top Threats to Cloud Computing 2024]](https://cloudsecurityalliance.org/artifacts/top-threats-to-cloud-computing-2024) · [[MITRE ATT&CK: Cloud Matrix]](https://attack.mitre.org/matrices/enterprise/cloud/)

---

## Источники

- [Microsoft: Shared responsibility in the cloud](https://learn.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility)
- [AWS: Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
- [Cloud Security Alliance: Top Threats to Cloud Computing 2024](https://cloudsecurityalliance.org/artifacts/top-threats-to-cloud-computing-2024)
- [MITRE ATT&CK: Cloud Matrix](https://attack.mitre.org/matrices/enterprise/cloud/)
- [MITRE ATT&CK: T1530 Data from Cloud Storage](https://attack.mitre.org/techniques/T1530/)
- [MITRE ATT&CK: T1552 Unsecured Credentials](https://attack.mitre.org/techniques/T1552/)
- [MSRC: SAS token exposure (2023)](https://msrc.microsoft.com/blog/2023/09/microsoft-mitigated-exposure-of-internal-information-in-a-storage-account-due-to-overly-permissive-sas-token/)
- [Wiz: 38TB of data accidentally exposed](https://www.wiz.io/blog/38-terabytes-of-private-data-accidentally-exposed-by-microsoft-ai-researchers)
- [Mandiant: UNC5537 / Snowflake](https://cloud.google.com/blog/topics/threat-intelligence/unc5537-snowflake-data-theft-extortion)

---

<div align="center">

[← 🎯 Целевые атаки (APT)](08-apt.md) · [🏠 Главная](../README.md) · [Далее: 📱 Мобильные устройства и IoT →](10-mobile-iot.md)

</div>
