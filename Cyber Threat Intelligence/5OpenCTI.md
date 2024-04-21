---
layout: default
title: OpenCTI ( Part I of V )
parent: Cyber Threat Intelligence
nav_order: 5
---
# OpenCTI ( Part I of V )

What: #platform\
Where: #github\
Who: Filigran\
When: 28/06/2019\
How: via docker
{: .fs-3 .ls-10 .text-mono .code-example }

Открываю цикл постов про OpenCTI. Расскажу базовые вещи, потом поиграемся с платным коннектором от Feedly, загрузим ленту новостей и завершим наполнением платформы разведданными по акторам.

Итак, вы зачем-то решили внедрить решение класса TIP в свою инфраструктуру 🏦
Для того, чтобы скорректировать ожидания сразу на входе и перед заключением договора о проведении пилотного проекта, поищите как позиционируют TI-платформу общемировые известные бренды. Поговорим коротко о брендах Чтобы по итогам пилота всё таки получилось использовать полученные данные и не возникло вопроса: "Ну, а что нам это дало и как, собсно, применять?" 📘

Приведу примеры позиционирования с ссылками-пруфами (как обычно 🙂):\
 — «A key benefit to using a threat intelligence platform is that it makes it easier to share external threat information across the organization to both technical and non-technical stakeholders.» [CrowdStrike]\
 — «A threat intelligence platform analyzes trillions of signals from the internet and maps them to tell you which threats are a serious risk to your business.» [Microsoft]\
 — «Integration into other cybersecurity systems so that it can work with other data points and analysis tools.» [Proofpoint]\
 — «TIPs process the data that they have collected to transform it into useful intelligence and reports for the organization.» [CheckPoint]\
 — «A Threat Intelligence Platform also aids analysts by automating the research and collection processes, significantly reducing response time.» [Anomali]

OpenCTI из себя представляет open-source [TI-платформу], над которой трудится большая команда разработчиков и энтузиастов. Версии регулярно [обновляются], баги фиксятся, а CEO [формирует] roadmap продукта. С развёртыванием, кстати, проблем не возникло, ставил согласно инструкции с помощью [докера] ("ест" 14Гб оперативки). 

Следует понимать, что "из коробки" платформа абсолютно пустая и не поставляется ни с фидами, ни с профилями акторов, ни с чем либо ещё. Это действительно пустая коробка, в которую надо ещё положить TI данные, чтобы увидеть все возможности решения.

Во-первых, это красиво (про UI), а во-вторых, подкупает полная свобода действий в части кастомизации решения под себя. Создание отчётов, линковка сущностей и заполнение их атрибутов, построение связей, указание различных меток, импорт/экспорт всего и вся. Кажется, что это очень большой плюс, но одновременно и минус. Надо же это всё кому-то делать... 🥲

Запомните этот [твит]! 

----
[CrowdStrike]:https://www.crowdstrike.com/cybersecurity-101/threat-intelligence/threat-intelligence-platforms/
[Microsoft]:https://www.microsoft.com/en-us/security/business/security-101/what-is-cyber-threat-intelligence
[Proofpoint]:https://www.proofpoint.com/au/threat-reference/threat-intelligence
[CheckPoint]:https://www.checkpoint.com/cyber-hub/cyber-security/what-is-a-threat-intelligence-platform-tip/
[Anomali]:https://www.anomali.com/resources/what-is-a-tip
[TI-платформу]:https://github.com/OpenCTI-Platform/opencti
[обновляются]:https://github.com/OpenCTI-Platform/opencti/releases
[формирует]:https://github.com/OpenCTI-Platform/opencti/issues/2864
[докера]:https://docs.opencti.io/latest/deployment/installation/#using-docker
[твит]:https://twitter.com/WeaselSec/status/1722623620277833896