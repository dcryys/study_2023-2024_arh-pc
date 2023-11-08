---
## Front matter
title: "Отчёт по лабораторной работе №4"
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

Освоить процедуры компиляции и сборки программ, которые написаны на ассемблере NASM.


# Теоретическое введение

Основные функциональные элементы любой ЭВМ - ценральный процессор (ЦП), память, периферийные устройства. В состав ЦП входят арифметико-логическое устройство (АЛУ),устройство управления (УУ) и регистры. Периферийные устройства можно разделить на устройства внешней памяти и устройства ввода-вывода.

Язык ассемблера - это машинно-ориентированный язык низкого уровня. Считается, что он наиболее приближен к архитектуре ЭВМ.Ассемблер - это специальная программа транслятор.

Процесс создания и обработки программы на языке ассемблера: 
1. Текст программы набирается в текстовом редакторе (файл с расширением .asm). 
2. При помощи NASM (транслятор) текст превращается в объектный код.
3. При помощи компоновщика ld код обрабатывается, создается исполняемый файл.
4. Производится запуск программы

# Выполнение лабораторной работы

При помощи команды mkdir созаю каталог для работы с программами на языке ассемблера NASM. Перехожу в него через команду cd (рис. @fig:001). 

![Создание каталога](image/n1.png){#fig:001 width=70%}

Создаю файл hello.asm командой touch и открываю его в текстовом редакторе (рис. @fig:002).

![Создание файла](image/n2.png){#fig:002 width=70%}

В текстовом редакторе ввожу будущий код программы, соблюдая синтаксис языка (рис. @fig:003).

![Код программы](image/n3.png){#fig:003 width=70%}

При помощи транслятора NASM превращаю текст в объектный код, вводя следующую команду (рис. @fig:004).

![Трансляция](image/n4.png){#fig:004 width=70%}

Проверяю, что файл расширения .o с кодом создан (рис. @fig:005).

![Проверка](image/n5.png){#fig:005 width=70%}

Выполняю следующую последовательность команд, чтобы узнать расширенный синтаксис командной строки. Она компилирует файл hell.asm в obj.o, так чтобы формат выходного файла будет elf, в него будут включены символы для отладки и создан файл листинга. При помощи команды ls проверяю, все ли файлы были созданы (рис. @fig:006).

![Расширенный синтаксис](image/n6.png){#fig:006 width=70%}

С помощью компоновщика LD обрабатываю объектный файл и получаю исполняемый файл (рис. @fig:007).

![Линковка](image/n7.png){#fig:007 width=70%}

Ввожу аналогичную последовательность команд с другими исходными данными (рис. @fig:008). При этом исполняемый файл будет называться main. Объектный файл, из которого он собран, называется obj.o.

![Линковка другого файла](image/n8.png){#fig:008 width=70%}

Запускаю получившуюся программу. Она выводит текст "Hello World!" (рис. @fig:009).

![Запуск программы](image/n9.png){#fig:009 width=70%}

# Выполнение заданий для самостоятельной работы

В каталоге создаю копию файла hello.asm с названием lab4.asm при помощи команды cp (рис. @fig:010).

![Копирование](image/n10.png){#fig:010 width=70%}

Открываю получившийся файл в текстовом редакторе и изменяю код так, чтобы при запуске программа выводила моё имя и фамилию (рис. @fig:011).

![Изменение кода](image/n11.png){#fig:011 width=70%}

Произвожу трансляцию текста в объектный файл, затем его линковку (компоновку). Получаю исполняемый файл. Запускаю программу (рис. @fig:012).

![Трансляция, линковка, запуск](image/n12.png){#fig:012 width=70%}

Все получившиеся файлы копирую в локальный репозиторий и загружаю на GitHub.

# Выводы

По итогам выполнения лабораторной работы №4 я научилась работать с машинно-ориентированным языком низкого уровня ассемблера NASM и создала первые две прораммы.


