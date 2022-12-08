---
## Front matter
title: "lab-09"
subtitle: "Программирование цикла. Обработка аргументов командной строки."
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

Целью работы является приобретение навыков написания программ с использованием циклов и
обработкой аргументов командной строки.

# Выполнение лабораторной работы

1. Создаю каталог для лабораторной работы No 9, перехожу в него и создаю файл lab9-1.asm (рис. [-@fig:001]).

![Создание файла.](image/01.png){ #fig:001 width=90% }

2. Ввожу в файл lab9-1.asm текст программы из листинга 9.1. (рис. [-@fig:002]).

![Текст программы.](image/02.png){ #fig:002 width=90% }

3. Создаю исполняемый файл и проверяю его работу (рис. [-@fig:003]).

![Проверка работы программы.](image/03.png){ #fig:003 width=90% }

4.  Изменяю текст программы, добавив изменение значение регистра ecx в цикле (рис. [-@fig:004]).

![Текст программы.](image/04.png){ #fig:004 width=90% }

5. Создаю исполняемый файл и проверяю его работу (рис. [-@fig:005]).

![Проверка работы программы.](image/05.png){ #fig:005 width=90% }

Число проходов цикла не соответствует значению N, введенному с клавиатуры.

6. Вношу изменения в текст программы, добавив команды push и pop для сохранения значения счетчика цикла loop (рис. [-@fig:006]).

![Текст программы.](image/06.png){ #fig:006 width=90% }

7. Создаю исполняемый файл и проверяю его работу (рис. [-@fig:007]).
 
 ![Проверка работы программы.](image/07.png){ #fig:007 width=90% }
 
В данном случае число проходов цикла соответствует значению N, введенному с клавиатуры.

8. Создаю файл lab9-2.asm в каталоге ~/work/arch-pc/lab09 и ввожу в него текст программы из листинга 9.2. (рис. [-@fig:008]).

![Текст программы.](image/08.png){ #fig:008 width=90% }

9. Создаю исполняемый файл и запускаю его, указав аргументы (рис. [-@fig:009]).

![Проверка работы программы.](image/09.png){ #fig:009 width=90% }

10. Создаю файл lab9-3.asm в каталоге ~/work/arch-pc/lab09 и ввожу в него текст программы из листинга 9.3. (рис. [-@fig:010]).

![Текст программы.](image/10.png){ #fig:010 width=90% }

11. Создаю исполняемый файл и запускаю его, указав аргументы (рис. [-@fig:011]).

![Проверка работы программы.](image/11.png){ #fig:011 width=90% }

12. Изменяю текст программы из листинга 9.3 для вычисления произведения аргументов командной строки (рис. [-@fig:012]).

![Текст программы.](image/12.png){ #fig:012 width=90% }

13.  Создаю исполняемый файл и запускаю его, указав аргументы (рис. [-@fig:013]).

![Проверка работы программы.](image/13.png){ #fig:013 width=90% }

#Самостоятельная работа

Пишу программу, которая находит сумму значений функции (рис. [-@fig:014]).

![Программа.](image/14.png){ #fig:014 width=90% }

Создаю исполняемый файл и проверяю его работу на нескольких наборах (рис. [-@fig:015]).

![Проверка работы программы.](image/15.png){ #fig:015 width=90% }

# Выводы

Я приобрел навыки написания программ с использованием циклов и обработкой аргументов командной строки.

