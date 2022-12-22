---
## Front matter
title: "lab-11"
subtitle: "Работа с файлами средствами Nasm"
author: "Владимир Андреевич Баранов"

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

Целью данной лабораторной работы являетсе приобретение навыков написания программ для работы с файлами.


# Выполнение лабораторной работы

1. Cоздаём каталог lab11, в нём создаём файл lab11-1.asm и файл
readme.txt (рис. [-@fig:001]).

![Создание каталога lab11 и файла lab11-1.asm, файла readme.txt.](image/1.png){ #fig:001 width=90% }

2. Переносим в файл программу из листинга No11.1 (рис. [-@fig:002]).

![Текст программы No1.](image/2.png){ #fig:002 width=90% }

3. Создаём исполняемый файл, проверяем работу (рис. [-@fig:003]).

![Создание исполняемого файла, проверка его работы.](image/3.png){ #fig:003 width=90% }

4. Изменяем права доступа к исполняемому файлу lab11-1, запрещаем его
выполнение с помощью команды chmod. Пытаемся запустить файл и видим
отказ в доступе. Всё правильно, мы же тольок что запретили всем доступ к
этому файлу (рис. [-@fig:004]).

![Изменение прав доступа к файлу.](image/4.png){ #fig:004 width=90% }

5. Теперь добавляем права на исполнение файла lab11-1.asm. Снова пытаемся
запустить исполняемый файл и опять видим отказ в доступе. Всё верно,
так ка мы изменили права достуа не к исполняемому файлу, а к исходному (рис. [-@fig:005]).

![Добавление прав на исполнение файла lab11-1.asm.](image/5.png){ #fig:005 width=90% }

6. Если мы оттранслируем файл lab11-1.asm в исполняемый и попробуем
запустить, то никаких запретов не будет. Ведь теперь на исполняемом файле
не стоит право запрета на исполнение (рис. [-@fig:006]).

![Создание исполняемого файла, проверка запуска.](image/6.png){ #fig:006 width=90% }

7. Теперь предоставим права доступа к файлу readme.txt, предложенные 6
варианту (w- r-x -w-). Я сделал это не одной, а тремя командами chmod (рис. [-@fig:007]).

![Предоставление прав доступа к файлу readme.txt.](image/7.png){ #fig:007 width=90% }

8. Проверяем правильность заданных прав с помощью команды ls -l. Все работает. (рис. [-@fig:008]).

![Проверка правильности заданных прав.](image/8.png){ #fig:008 width=90% }

# Самостоятельная работа

Пишем программу, которая будет запрашивать имя, принимать имя и записывать его в созданный файл (рис. [-@fig:009]).

![Код программы.](image/9.png){ #fig:009 width=90% }

Создаём исполняемый файл и проверяем его работу (рис. [-@fig:010]).

![Создание исполняемого файла, проверка его работы.](image/10.png){ #fig:010 width=90% }

# Выводы

В ходе данной лабораторной работы я научился создавать файлы, открывать
и закрывать их, записывать в них какие-либо данные, считывать какие-либо
данные. Также научился управлять правами доступа к файлам. С приобретённы-
ми за всё время знаниями я способен написать какую-нибудь функциональную
программу.

