---
layout: default
title: Beautiful SIGMA (Part II of II)
parent: Cyber Threat Intelligence
nav_order: 11
---
# Beautiful SIGMA (Part II of II)

What: #sigma\
Where: #vscode\
Who: Qwerty Bubble\
When: 01/06/2024\
How: Python
{: .fs-3 .ls-10 .text-mono .code-example }

Итак, SIGMA.

В прошлом посте вспомнили, что это такое и как писать так, чтобы было быстро и красиво. В этом посте тоже начнём с полезных материалов по теме:\
1) [Вступление] от ребят, которые делали крутую песочницу, а теперь предлагают полностью автоматизировать Tier 1 SOC;\
2) [Описание] по источникам событий от Nextrone Systems;\
3) Подробный разбор темы от коллег из PT [Часть 1], [Часть 2], [Часть 3];\
4) [Статья] от VT по преобразованию SIGMA-логики в YARA-правила;\
5) Также приложу архив c курсом по написанию SIGMA правил (пароль sigma).

Вооружившись всеми знаниями и написав целый ворох различных правил, давайте теперь отшлифуем весь массив того, что получилось

Написанный [скрипт] решает две основные задачи:

➖ проверяет синтаксис на соответствие схемы языка YAML;\
➖ валидирует наличие и содержимое необходимых атрибутов в правиле (за основу был взят код из [этого] репозитория);

Красивых вам правил! 

Всем хороших выходных и берегите себя

----
[про сабж]:https://sigmahq.io/docs/guide/about.html
[Вступление]:https://intezer.com/blog/threat-hunting/intro-to-sigma-rules/
[Описание]:https://www.nextron-systems.com/2023/03/24/demystifying-sigma-log-sources/
[Часть 1]:https://habr.com/ru/companies/pt/articles/510480/
[Часть 2]:https://habr.com/ru/companies/pt/articles/513032/
[Часть 3]:https://habr.com/ru/companies/pt/articles/515532/
[Статья]:https://blog.virustotal.com/2023/06/threat-hunting-converting-sigma-to-yara.html
[скрипт]:https://github.com/QwertyBubble/sigma-validator
[этого]:https://github.com/rjbs/Rx