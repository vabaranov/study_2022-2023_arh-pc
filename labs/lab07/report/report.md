---
## Front matter
title: "lab-06"
subtitle: "Основы работы с
Midnight Commander (mc). Структура
программы на языке ассемблера NASM.
Системные вызовы в ОС GNU Linux."
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

Целью работы является приобретение практических навыков работы в Midnight Commander. Освоение
инструкций языка ассемблера mov и int.

# Выполнение лабораторной работы

1. Открываю Midnight Commander и с помощью  функциональной клавиши F7 создаю папку lab06 (рис. [-@fig:001]).

![Папка lab06 в mc.](image/01.png){ #fig:001 width=90% }

2. Пользуясь строкой ввода и командой touch создаю файл lab6-1.asm (рис. [-@fig:002]).

![Создание файла lab6-1.asm.](image/02.png){ #fig:002 width=90% }

3. С помощью функциональной клавиши F4 открываю файл lab6-1.asm для редактирования во встроенном редакторе nano (рис. [-@fig:003]).

![Открытие файла в редакторе.](image/03.png){ #fig:003 width=90% }


4. Ввожу текст программы из листинга, сохраняю изменения и закрываю файл. С помощью функциональной клавиши F3 открываю файл lab6-1.asm для
просмотра. Убеждаюсь, что файл содержит текст программы. (рис. [-@fig:004])

![Файл, содержащий текст программы.](image/04.png){ #fig:004 width=90% }

5. Оттранслирую текст программы lab6-1.asm в объектный файл. Выполняю компоновку объектного файла и запускаю получившийся исполняемый файл (рис. [-@fig:005]).

![Компоновка и запуск исполняемого файла.](image/05.png){ #fig:005 width=90% }

6. Скачиваю файл in_out.asm со страницы курса в ТУИС. С помощью функциональной клавиши F6 создаю копию файла lab6-1.asm с именем lab6-2.asm. Исправляю текст программы в файле lab6-2.asm с использование под- программ из внешнего файла in_out.asm. Создаю исполняемый файл и проверяю его работу  (рис. [-@fig:006]).

![Компоновка и запуск исполняемого скопированного файла.](image/06.png){ #fig:006 width=90% }

Задание для самостоятельной работы.

1. Создаю копию файла lab6-1.asm. Вношу изменения в программу (без
использования внешнего файла in_out.asm), так чтобы она работала по
следующему алгоритму:
• вывести приглашение типа “Введите строку:”;
• ввести строку с клавиатуры;
• вывести введённую строку на экран.

(рис. [-@fig:007]).

![Внесенные изменения в программу(1).](image/07.png){ #fig:007 width=90% }

2. Получаю исполняемый файл и проверяю его работу (рис. [-@fig:008]).

![Проверка работы файла(1).](image/08.png){ #fig:008 width=90% }

3. Создаю копию файла lab6-2.asm. Исправляю текст программы с исполь-
зованием подпрограмм из внешнего файла in_out.asm, так чтобы она ра-
ботала по следующему алгоритму:
• вывести приглашение типа “Введите строку:”;
• ввести строку с клавиатуры;
• вывести введённую строку на экран.

(рис. [-@fig:009]). 

![Внесенные изменения в программу(2).](image/09.png){ #fig:009 width=90% }

4. Создаю исполняемый файл и проверяю его работу (рис. [-@fig:010]).

![Проверка работы файла(2).](image/10.png){ #fig:010 width=90% }

# Выводы

В ходе данной лабараторной работы я приобрел практические навыки работы в Midnight Commander. Освоил
инструкции языка ассемблера mov и int.

