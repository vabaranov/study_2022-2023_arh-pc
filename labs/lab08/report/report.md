---
## Front matter
title: "lab-07"
subtitle: "Арифметические операции в NASM"
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

Целью работы является освоение арифметических инструкций языка ассемблера NASM.

# Выполнение лабораторной работы

1. Создаю каталог для программ лабораторной работы 7, перехожу в
него и создаю файл lab7-1.asm (рис. [-@fig:001]).

![Создание файла.](image/01.png){ #fig:001 width=90% }

2.  Для корректной работы программы подключаемый файл in_out.asm копирую в каталог ~/work/arch-pc/lab07 (рис. [-@fig:002]).

![Копирование файла.](image/02.png){ #fig:002 width=90% }

3.  Создаю исполняемый файл и запускаю его (рис. [-@fig:003]).

![Исполнение программы.](image/03.png){ #fig:003 width=90% }

4. Изменяю текст программы из листинга 1, cоздаю исполняемый файл и запускаю его (рис. [-@fig:004]).

![Запуск измененной программы.](image/04.png){ #fig:004 width=90% }

5. Создаю файл lab7-2.asm в каталоге ~/work/arch-pc/lab07 и запускаю его (рис. [-@fig:005]).

![Исполнение программы.](image/05.png){ #fig:005 width=90% }

6. Изменяю текст программы из листинга 2, cоздаю исполняемый файл и запускаю его рис. [-@fig:006]).

![Запуск измененной программы.](image/06.png){ #fig:006 width=90% }

Разница между функциями в том, что iprint просто выводит сообщение на экран, а iprintLF добавляет к этому переход на новую строку.

7. Создаю файл lab7-3.asm в каталоге ~/work/arch-pc/lab07 и запуская его (рис. [-@fig:007]).

![Создание файла и исполнение программы.](image/07.png){ #fig:007 width=90% }

8. Изменяю текст программы для вычисления выражения 𝑓(𝑥) = (4 ∗ 6 + 2)/5, создаю исполняемый файл и запускаю его (рис. [-@fig:008]).

![Исполнение программы.](image/08.png){ #fig:008 width=90% }

9. Создаю файл variant.asm в каталоге ~/work/arch-pc/lab07 и ввожу в этот файл текст программы из листинга 7.4. Создаю исполняемый файл, запускаю его и вывожу номер варианта на экран (рис. [-@fig:009]).

![Вычисление номера варианта.](image/09.png){ #fig:009 width=90% }

Вопросы:

1)Какие строки листинга 7.4 отвечают за вывод на экран сообщения ‘Ваш вариант:’? mov eax,msg call sprintLF .
2) Для чего используется следующие инструкции? nasm mov ecx, x mov edx, 80 call sread Эти инструкции используются для ввода переменной Х с клавиатуры и сохранения введенных данных. 
3) Для чего используется инструкция “call atoi”? Эта инструкция используется для преобразования Кода переменной ASCII в число. 
4) Какие строки листинга 7.4 отвечают за вычисления варианта? mov ebx,20 div ebx inc edx .
5)В какой регистр записывается остаток от деления при выполнении инструкции “div ebx”? В регистре ebx. 
6) Для чего используется инструкция “inc edx”? Для увеличения значения edx на 1. 
7)Какие строки листинга 7.4 отвечают за вывод на экран результата вычислений? mov eax,edx call iprintLF.

Самостоятельная работа 

В результате работы программы variant.asm получаю вариант №17. Создаю файл с именем lab7-5.asm, пишу там программу для вычисления значения выражения 18(x+1)/6 (рис. [-@fig:010]).

![Программа.](image/10.png){ #fig:010 width=90% }

Далее запускаю файл. Подставляю заданные значения х, сверяю полученные результаты с вычисленными аналитически (рис. [-@fig:011]).
 
 ![Вычисление.](image/11.png){ #fig:011 width=90% }

# Выводы

В ходе данной лабараторной работы я освоил арифметические инструкции языка ассемблера NASM.
