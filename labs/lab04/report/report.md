---
## Front matter

title: "lab-04"
subtitle: "Язык разметки Markdown"
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

Целью работы является освоение процедуры оформления отчетов с помощью
легковесного языка разметки Markdown.

# Выполнение лабораторной работы

1. Открываю терминал.

2. Перехожу в каталог курса сформированный при выполнении лаборатор-
ной работы No3.

Обновляю локальный репозиторий, скачав изменения из удаленного репози-
тория с помощью команды git pull (рис. [-@fig:001]).

![Результат команды 'git pull'.](image/Снимок экрана от 2022-10-27 11-11-11.png){ #fig:001 width=90% }

3. Перехожу в каталог с шаблоном отчета по лабораторной работе No 4.

4. Провожу компиляцию шаблона с использованием Makefile. Для этого
ввожу команду make.Открываю и проверяю корректность полученных файлов (рис. [-@fig:002]).

![Компиляция шаблона с использованием Makefile.](image/Снимок экрана от 2022-10-27 10-51-23.png){ #fig:002 width=90% }

5. Удаляю полученный файлы с использованием Makefile. Для этого ввожу
команду make clean (рис. [-@fig:003]).

![Удаление полученного файла.](image/Снимок экрана от 2022-10-27 11-11-26.png){ #fig:003 width=90% }

Проверяю, что после этой команды файлы report.pdf и report.docx были
удалены (рис. [-@fig:004]).

![Отсутствие файлов после команды make clean.](image/Снимок экрана от 2022-10-27 11-51-57.png){ #fig:004 width=90% }

6. Открываю файл report.md c помощью текстового редактора gedit (рис. [-@fig:005]).

![Открытие Markdown.](image/Снимок экрана от 2022-10-27 11-58-37.png){ #fig:005 width=90% }

7. Заполняю отчет и скомпилирую отчет с использованием Makefile. Про-
веряю корректность полученных файлов. 

8. Загружаю файлы на Github (рис. [-@fig:006]).

![Команды для загрузки файлов на Github.](image/Снимок экрана от 2022-10-27 13-19-45.png){ #fig:006 width=90% }

# Выводы

В ходе данной лабараторной работы я освоил процедуры оформления отчетов с помощью
легковесного языка разметки Markdown.

