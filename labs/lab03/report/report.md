---
## Front matter
title: "Отчёт по лабораторной работе №3"
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

Целью данной работы является освоение процедуры оформления отчётов при помощи легковесного
языка разметки Markdown.


# Теоретическое введение

: Основные сведения о Markdown: {#tbl:std-dir}

|   Действие                               | Описание                                                                                                |
|------------------------------------------|---------------------------------------------------------------------------------------------------------|
| `#`                                      | Создание заголовка. Эквивалентно h1 в языке гипертекстовой разметки HTML. ## - h2, ### - h3, #### - h4  |
| `** ** `                                 | Полужирное начертание текста                                                                            |
| `*  *`                                   | Курсивное начертание текста                                                                             |
| `*** ***`                                | Одновременно курсивное и полужирное начертание текста                                                   |
| `>`                                      | Создание блока цитирования                                                                              |
| `1.`                                     | Создание упорядоченного списка (чтобы вложить список в другой, необходимо добавить отступ)              |
| `*` или `-`                              | Создание маркированного (неупорядоченного) списка                                                       |
| `[link text](http://)`                   | Создание текстовой гиперссылки                                                                          |
|` ``` language`                           | Встраивание фрагмента кода в предложение                                                                |
|`![name](way/file.jpg "text"){parameters}`| Вставка изображения                                                                                     |


# Выполнение лабораторной работы

Открываю терминал. Скачиваю измененные данные из репозитория и обновляю его при помощи команды "git pull" (рис. @fig:001). 

![Выполнение команды git pull](image/Обновление репозитория (1).png){#fig:001 width=70%} 

Перехожу в каталог третьей лабораторной работы и произвожу компиляцию шаблона с использованием команды "Makefile" (рис. @fig:002) - (рис. @fig:004). 

![Компиляция шаблона (создание .docx)](image/Компиляция шаблона (2).png){#fig:002 width=70%} 

![Компиляция шаблона (создание .pdf)](image/Компиляция шаблона (3).png){#fig:003 width=70%} 

![Файлы созданы](image/Скомпилировалось (4).png){#fig:004 width=70%} 

Удаляю полученные файлы при помощи команды "make clean" (рис. @fig:005) - (рис. @fig:006). 

![Выполнение команды make clean](image/Удаление (5).png){#fig:005 width=70%} 

![Файлы удалены](image/Удалилось (6).png){#fig:006 width=70%} 

Открываю файл report.md при помощи текстового редактора (рис. @fig:007) - (рис. @fig:008). 

![Команда gedit](image/Открывание шаблона (7).png){#fig:007 width=70%} 

![Структура файла](image/Изучение структурыы (8).png){#fig:008 width=70%} 


# Выполнение заданий для самостоятельной работы

Создаю отчет по лабораторной работе #2 в Markdown и загружаю его в каталог. (рис. @fig:009). 

![Отчёт](image/12344.png){#fig:009 width=70%} 


# Выводы

По итогам выполнения лабораторной работы №3 я научилась работать с легковесным языком разметки Markdown и выполнять отчёты при помощи него.

::: {#refs}
:::
