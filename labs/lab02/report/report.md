---
## Front matter
title: "Отчёт по лабораторной работе №2"
subtitle: "Дисциплина: Архитектура компьютера"
author: "Будник Александра Олеговна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---


# Цель работы

Целью данной работы является изучить особенности идеологии и применения средств контроля версий GitHub, а также приобрести практические навыки по работе с системой git.


# Теоретическое введение

Системы контроля версий применяются при работе нескольких человек над одним проектом. В таких системах используется централизованная модель (единый репозиторий). Системы контроля версий поддерживают возможность отслеживания изменений и разрешения конфликтов.

Система контроля версий Git - набор программ командной строки, к которым можно получить доступ из терминала.

Описание некоторых команд git {#tbl:std-dir}

| Команда          | Описание команды                                                |
|------------------|---------------------------------------------------------------- |
| `git unit`       | Создание главного дерева репозитория                            |
| `git pull`       | Получение обновлений из центрального репозитория в локальный    |
| `git push`       | Отправка обновлений из локального репозитория в центральный     |
| `git commit -am` | Сохранение изменений (и добавление комментария)                 |
| `git add`        | Добавление конкретных изменённых/созданных файлов               |
| `git status`     | Просмотр списка всех изменённых файлов в данной директории      |
 

# Выполнение лабораторной работы

Произвожу первичную настойку git. Вхожу в аккаунт и задаю параметры работы с системой контроля версий. Называю основную ветку master (рис. @fig:001).

![Базовая настройка git](image/im1.png){#fig:001 width=100%}

Создаю SSH – ключ для последующей идентификации на сервере (рис. @fig:002). 

![Создание ключа](image/im2.png){#fig:002 width=100%}

Узнаю содержимое ключа при помощи команды «cat» и копирую его (рис. @fig:003). 

![Ключ](image/im3.png){#fig:003 width=100%}

Вставляю ключ в специальное поле на сайте github. Ключ успешно создан и позволяет соединить компьютер и сервер. (рис. @fig:004). 

![Ключ](image/im4.png){#fig:004 width=100%}

Создаю репозиторий для работы при помощи команды «mkdir» и параметра «-p». (рис. @fig:005). 

![Создание репозитория](image/im5.png){#fig:005 width=100%}

Этот репозиторий должен быть создан на основе уже существующего шаблона. Для этого клонирую готовый репозиторий с сайта (рис. @fig:006). 

![Клонирование репозитория](image/im6.png){#fig:006 width=100%}

Произвожу настройку каталога курса. С помощью команды «rm» удаляю лишние файлы (рис. @fig:007). 

![Настройка каталога курса](image/im7.png){#fig:007 width=100%}

Отправляю файлы на сервер при помощи команды «git add». С функцией «git commit» добавляю описание произведённых действий (рис. @fig:008). 

![Команды git add и git commit](image/im8.png){#fig:008 width=100%}

Использую команду «git push» для отправки всех произведённых изменений локального дерева в центральный репозиторий (рис. @fig:009). 

![Отправка изменений](image/im9.png){#fig:009 width=100%}


# Выполнение заданий для самостоятельной работы

Создаю отчет и загружаю его в нужные каталоги на сервере в GitHub. Добавляю отчёт по прошлой лабораторной работе в репозиторий (рис. @fig:010). 

![Отчёт](image/im10.png){#fig:010 width=100%}


# Выводы

По итогам выполнения лабораторной работы №2 я научилась работать с системой контроля версий GitHub, произвела её базовую настройку для работы и учёбы.




