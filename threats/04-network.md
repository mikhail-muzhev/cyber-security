[🏠 Главная](../README.md) › [⚠️ Угрозы](README.md) › 🌐 Сетевые атаки

# 🌐 Сетевые атаки

Атаки на то, *как* данные передаются: перегрузка каналов, перехват и подмена трафика, подмена «адресных книг» интернета.

## Содержание

- [DoS и DDoS](#dos-и-ddos)
- [Перехват трафика (MITM)](#перехват-трафика-mitm)
- [Подмена DNS](#подмена-dns)
- [Перехват маршрутов BGP](#перехват-маршрутов-bgp)
- [Сканирование и атаки на открытые сервисы](#сканирование-и-атаки-на-открытые-сервисы)
- [Как защититься](#как-защититься)
- [Источники](#источники)

---

## DoS и DDoS

**[DoS](../glossary.md#dos)** (Denial of Service, отказ в обслуживании) — атака, после которой сервис перестаёт работать для обычных пользователей. **[DDoS](../glossary.md#ddos)** (Distributed DoS, распределённый DoS) — то же самое, но атака идёт одновременно с тысяч или миллионов устройств, обычно из **[ботнета](../glossary.md#botnet)**.

💡 Аналогия: толпа людей, которые ничего не покупают, забивает вход в магазин, и настоящие покупатели не могут войти.

| Тип | ⚙️ Что перегружают | Пример |
|---|---|---|
| **Объёмные** (volumetric) | Интернет-канал: «забить трубу» | Поток мусорных пакетов на сотни гигабит в секунду |
| **Протокольные** (protocol) | Сетевое оборудование и ОС: таблицы соединений, межсетевые экраны | SYN flood: тысячи «полуоткрытых» соединений |
| **Прикладного уровня** (application layer, L7) | Само приложение: веб-сервер, базу данных | Миллионы «настоящих» запросов к тяжёлой странице поиска |

**[Амплификация](../glossary.md#amplification)** (усиление). Атакующий отправляет маленький запрос на открытый сервер (DNS, NTP, memcached) и подставляет в него адрес жертвы как обратный. Сервер отвечает жертве ответом, который в десятки или тысячи раз больше запроса.

🏷️ **MITRE ATT&CK:** [T1498 Network Denial of Service](https://attack.mitre.org/techniques/T1498/) · [T1499 Endpoint Denial of Service](https://attack.mitre.org/techniques/T1499/)
🔗 [Cloudflare: Что такое DDoS-атака?](https://www.cloudflare.com/ru-ru/learning/ddos/what-is-a-ddos-attack/)

### 📰 Mirai и Dyn (октябрь 2016)

Ботнет Mirai состоял из заражённых IoT-устройств: камер, видеорегистраторов, роутеров с заводскими паролями. Он атаковал DNS-провайдера Dyn, и на несколько часов у многих пользователей в США и Европе стали недоступны Twitter, Netflix, GitHub и другие сервисы.
🔗 [CISA: Heightened DDoS Threat Posed by Mirai and Other Botnets](https://www.cisa.gov/news-events/alerts/2016/10/14/heightened-ddos-threat-posed-mirai-and-other-botnets)

### 📰 GitHub (февраль 2018): амплификация через memcached

GitHub выдержал атаку мощностью 1,35 Тбит/с. Злоумышленники использовали открытые в интернет серверы memcached, которые многократно усиливали трафик.
🔗 [GitHub Blog: February 28th DDoS Incident Report](https://github.blog/news-insights/company-news/ddos-incident-report/)

---

## Перехват трафика (MITM)

**[MITM](../glossary.md#mitm)** (Man-in-the-Middle, «человек посередине»; в MITRE называется *Adversary-in-the-Middle*). Злоумышленник встраивается между вами и сайтом или сервером. Он может читать передаваемые данные и подменять их, а вы ничего не замечаете.

| Приём | ⚙️ Как работает |
|---|---|
| **[Сниффинг](../glossary.md#sniffing)** (sniffing, прослушивание) | Перехват всего трафика в сети. Опасен, если данные передаются без шифрования. [[MITRE T1040]](https://attack.mitre.org/techniques/T1040/) |
| **[ARP-спуфинг](../glossary.md#arp-spoofing)** (ARP spoofing) | В локальной сети злоумышленник убеждает компьютеры, что он и есть роутер, и весь трафик идёт через него. [[MITRE T1557.002]](https://attack.mitre.org/techniques/T1557/002/) |
| **[Evil Twin](../glossary.md#evil-twin)** («злой двойник») | Поддельная точка Wi-Fi с названием как у настоящей: `Airport_Free_WiFi`, `Coffee_Guest` |
| **SSL stripping** (понижение шифрования) | Злоумышленник подменяет защищённое соединение HTTPS на незащищённое HTTP и читает трафик в открытом виде |

🏷️ **MITRE ATT&CK:** [T1557 Adversary-in-the-Middle](https://attack.mitre.org/techniques/T1557/)
🔗 [Cloudflare: Что такое атака «человек посередине»?](https://www.cloudflare.com/ru-ru/learning/security/threats/man-in-the-middle-attack/)

> [!NOTE]
> **[TLS](../glossary.md#tls)** (протокол шифрования, буква «S» в HTTPS) защищает от большинства MITM-атак. Главное — не игнорировать предупреждения браузера о недоверенном сертификате.

---

## Подмена DNS

**[DNS](../glossary.md#dns)** (Domain Name System) — «телефонная книга» интернета. Она переводит понятное имя `example.com` в IP-адрес сервера. Если подменить ответ DNS, пользователь наберёт правильный адрес, но попадёт на сайт злоумышленника.

| Приём | ⚙️ Что подменяют |
|---|---|
| **Отравление кеша DNS** (DNS cache poisoning) | В кеш DNS-сервера провайдера или компании подкладывают ложную запись |
| **Перехват DNS** (DNS hijacking) | Меняют настройки DNS на роутере жертвы или захватывают учётную запись у регистратора домена |

🔗 [Cloudflare: Что такое отравление кеша DNS?](https://www.cloudflare.com/ru-ru/learning/dns/dns-cache-poisoning/)

---

## Перехват маршрутов BGP

**[BGP](../glossary.md#bgp)** (Border Gateway Protocol) — протокол, по которому крупные сети договариваются, через кого доставлять трафик. Он во многом основан на доверии. Если сеть по ошибке или умышленно объявит «адреса сервиса X у меня», трафик к X может уйти к ней.

### 📰 Pakistan Telecom и YouTube (февраль 2008)

Пакистанский оператор хотел заблокировать YouTube внутри страны, но анонсировал маршрут к YouTube на весь интернет. Около двух часов значительная часть мирового трафика YouTube уходила в Пакистан, и сервис был недоступен.
🔗 [RIPE NCC: YouTube Hijacking — A RIPE NCC RIS case study](https://www.ripe.net/about-us/news/youtube-hijacking-a-ripe-ncc-ris-case-study/)

Защита на уровне операторов: **RPKI** (криптографическая проверка того, кому принадлежат адреса). [[Cloudflare: Что такое перехват BGP?]](https://www.cloudflare.com/ru-ru/learning/security/glossary/bgp-hijacking/)

---

## Сканирование и атаки на открытые сервисы

Перед атакой злоумышленники **сканируют** интернет и ищут открытые **[порты](../glossary.md#port)** («двери» для сетевых служб) и уязвимые сервисы. Сейчас это делается автоматически по всему интернету за считаные часы.

Самые атакуемые «двери»:

- **Удалённый рабочий стол (RDP)**, открытый в интернет. [[MITRE T1133]](https://attack.mitre.org/techniques/T1133/)
- **VPN-шлюзы и межсетевые экраны** с неустановленными обновлениями. Сейчас это одна из главных точек входа: по данным Verizon DBIR 2026, эксплуатация уязвимостей стала самым частым способом проникновения. [[Help Net Security, обзор DBIR 2026]](https://www.helpnetsecurity.com/2026/05/25/lessons-from-verizon-dbir-2026-findings/)
- **Публичные приложения**: сайты, почтовые серверы. [[MITRE T1190]](https://attack.mitre.org/techniques/T1190/)

🏷️ **MITRE ATT&CK:** [T1595 Active Scanning](https://attack.mitre.org/techniques/T1595/)

---

## Как защититься

| 🛡️ Мера | Против чего |
|---|---|
| **Сервис защиты от DDoS** (у провайдера, CDN, специализированные компании) | DDoS |
| **Шифрование везде**: HTTPS, VPN в публичных Wi-Fi, отказ от устаревших протоколов без шифрования | MITM, сниффинг |
| **[HSTS](../glossary.md#hsts)**: сайт велит браузеру всегда открывать его только по HTTPS | SSL stripping |
| **Не подключаться к открытым Wi-Fi** без VPN, отключить автоподключение | Evil Twin |
| **[DNSSEC](../glossary.md#dnssec)**, защищённый DNS (DoH/DoT), MFA у регистратора домена | Подмена DNS |
| **Не выставлять RDP и админ-панели в интернет**, доступ только через VPN с MFA | Атаки на открытые сервисы |
| **Срочно обновлять устройства на границе сети**: VPN, межсетевые экраны, почтовые шлюзы | Эксплуатация уязвимостей |
| **[Сегментация сети](../glossary.md#segmentation)** и **[межсетевой экран](../glossary.md#firewall)** | Распространение атаки внутри сети |

---

## Источники

- [MITRE ATT&CK: T1498 Network Denial of Service](https://attack.mitre.org/techniques/T1498/)
- [MITRE ATT&CK: T1557 Adversary-in-the-Middle](https://attack.mitre.org/techniques/T1557/)
- [MITRE ATT&CK: T1040 Network Sniffing](https://attack.mitre.org/techniques/T1040/)
- [MITRE ATT&CK: T1190 Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)
- [Cloudflare Learning Center (на русском)](https://www.cloudflare.com/ru-ru/learning/)
- [CISA: Mirai](https://www.cisa.gov/news-events/alerts/2016/10/14/heightened-ddos-threat-posed-mirai-and-other-botnets)
- [GitHub: DDoS Incident Report (2018)](https://github.blog/news-insights/company-news/ddos-incident-report/)
- [RIPE NCC: YouTube Hijacking case study](https://www.ripe.net/about-us/news/youtube-hijacking-a-ripe-ncc-ris-case-study/)
- [CISA: Understanding and Responding to DDoS Attacks](https://www.cisa.gov/resources-tools/resources/understanding-and-responding-distributed-denial-service-attacks)

---

<div align="center">

[← 🔑 Атаки на учётные записи](03-credentials.md) · [🏠 Главная](../README.md) · [Далее: 🕸️ Атаки на веб-приложения →](05-web.md)

</div>
