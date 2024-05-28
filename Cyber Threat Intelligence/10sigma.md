---
layout: default
title: Beautiful SIGMA (Part I of II)
parent: Cyber Threat Intelligence
nav_order: 10
---
# Beautiful SIGMA (Part I of II)

What: #sigma\
Where: #vscode\
Who: humpalum\
When: 15/03/2022\
How: via extension
{: .fs-3 .ls-10 .text-mono .code-example }

Итак, SIGMA. Коротко [про сабж], [спецификация], [гайд] по созданию правил и значений атрибутов.

Ключевые вещи:\
❌ это не про детект вредоносной активности на потоке\
✔️ это про структурированное описание корреляционной логики\
❌ нельзя применять as is в проде, т.к. правила не учитывают особенности конкретно вашей инфраструктуры\
✔️ правила в обязательном порядке должны просматриваться аналитиком, а затем тестироваться в SIEM-решениях\
❓конвертеры есть, да. Ну и что? Во-первых, не факт, что под ваше SIEM-решение. В 2017 году была поддержка ArcSight, а с недавнего времени её просто выпилили (подозреваю, что из-за ошибок при конвертации). Во-вторых, вышеуказанную проблему с адаптацией конвертер не решит, as is использовать всё равно не получится.

А как всё таки сделать так, чтобы это всё создавалось быстро и красиво? ✈️ \
В 2018 году один из авторов SIGMA уже [писал] про один из подходов. Немного скорректирую:\
1️⃣ Скачиваем [Visual Studio Code] \
2️⃣ Устанавливаем [плагин] (находим на вкладке маркетплэйса в самой студии) \
3️⃣ Ctrl+N создаём .yaml файл и сохраняем его Ctrl+S\
4️⃣ Меняем в нижней панели справа язык на SIGMA \
5️⃣ Пишем new, плагин автоматически предложит дополнить newrule и нажимаем Enter

По итогу, у вас готовый шаблон правила, в котором плагин будет ещё подсказывать значения атрибутов tags и logsource. Подробнее о функциональных возможностях посмотрите на самой страничке в маркетплейсе.

Красивых вам правил!

Со средой

P.S.: компания Флориана разработала EDR-агент [Aurora] на SIGMA-правилах. Интересное развитие получил [chainsaw], конечно...

----
[про сабж]:https://sigmahq.io/docs/guide/about.html
[спецификация]:https://github.com/SigmaHQ/sigma-specification/blob/main/Sigma_specification.md
[гайд]:https://github.com/SigmaHQ/sigma/wiki/Rule-Creation-Guide
[Visual Studio Code]:https://code.visualstudio.com/
[плагин]:https://marketplace.visualstudio.com/items?itemName=humpalum.sigma
[писал]:https://www.nextron-systems.com/2018/02/10/write-sigma-rules/
[Aurora]:https://www.nextron-systems.com/aurora/
[chainsaw]:https://github.com/WithSecureLabs/chainsaw