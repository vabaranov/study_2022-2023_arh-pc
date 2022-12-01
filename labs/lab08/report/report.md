---
## Front matter
title: "lab-08"
subtitle: "Команды безусловного и условного переходов в Nasm. Программирование ветвлений."
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
Целью работы является изучение команд условного и безусловного переходов. Приобретение навыков написания программ с использованием переходов. Знакомство с назначением и структурой файла листинга.

# Выполнение лабораторной работы

1. Создаю каталог для программам лабораторной работы No 8, перехожу в него и создаю файл lab8-1.asm (рис. [-@fig:001]).

![Создание файла.](image/01.png){ #fig:001 width=90% }

2. Ввожу в файл lab8-1.asm текст программы из листинга 8.1, проверяю программы (рис. [-@fig:002]).

![Проверка работы программы.](image/02.png){ #fig:002 width=90% }

3. Изменяю программу таким образом, чтобы она выводила сначала ‘Сообщение No 2’, потом ‘Сообщение No 1’ и завершала работу, проверяю работу программы (рис. [-@fig:003]).

![Проверка работы программы.](image/03.png){ #fig:003 width=90% }

4. Изменяю программу еще раз, проверяю ее работу (рис. [-@fig:004]).

![Проверка работы программы.](image/04.png){ #fig:004 width=90% }

5. Создаю файл lab8-2.asm в каталоге ~/work/arch-pc/lab08. Ввожу текст программы из листинга 8.3 в lab8-2.asm (рис. [-@fig:005]).

![Проверка работы программы.](image/05.png){ #fig:005 width=90% }

6. Создаю файл листинга для программы из файла lab8-2.asm Открываю файл листинга lab8-2.lst с помощью mcedit (рис. [-@fig:006]).

![Создание файла и открытие с помощью текстового редактора.](image/06.png){ #fig:006 width=90% }

Обьясняю содержимое 3-х строк:

1. 000000F2,000000F7,000000FC-этоадресстроки.
2. B9[0A000000],BA0A000000,E842FFFFFF-этомашинныйкод.
3. ‘mov ecx,B’, ‘call atoi’, mov [B], eax - это исходный текст программы.

7. Открываю файл с программой lab8-2.asm и в любой инструкции с двумя операндами удаляю один операнд. Выполняю трансляцию с получением файла листинга. 
В этом случае выдается ошибка (рис. [-@fig:007]).

![Ошибка при удалении операнда.](image/07.png){ #fig:007 width=90% }

# Самостоятельная работа:

1. Пишу программу нахождения наименьшей из 3 целочисленных переменных a,b,c. Создаю исполняемый файл и проверяю его работу (рис. [-@fig:008]) (рис. [-@fig:009]).

![Программа.](image/08.png){ #fig:008 width=90% }

![Работа программы.](image/09.png){ #fig:009 width=90% }

2. Пишу программу, которая для введенных с клавиатуры значений x и a вычисляет значение заданной функции f(x) и выводит результат вычислений. Создаю исполняемый файл и проверяю его работу (рис. [-@fig:010]) (рис. [-@fig:011]) (рис. [-@fig:012]).

![Программа.](image/10.png){ #fig:010 width=90% }

![Программа.](image/11.png){ #fig:011 width=90% }

![Работа программы.](image/12.png){ #fig:012 width=90% }

# Выводы

В ходе данной лабараторной работы я изучил команды условного и безусловного переходов, приобрел навыки написания программ с использованием переходов, ознакомился с назначением и структурой файла листинга.

