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

# Теоретическое введение
4.2.1. Базовые сведения о Markdown
Чтобы создать заголовок, используйте знак #, например:
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
Чтобы задать для текста полужирное начертание, заключите его в двойные
звездочки:
This text is **bold**.
Чтобы задать для текста курсивное начертание, заключите его в одинарные
звездочки:
This text is *italic*.
57 Демидова А. В.
Архитектура ЭВМ
Чтобы задать для текста полужирное и курсивное начертание, заключите его
в тройные звездочки:
This is text is both ***bold and italic***.
Блоки цитирования создаются с помощью символа >:
> The drought had lasted now for ten million years, and the reign of
the terrible lizards had long since ended. Here on the Equator,
in the continent which would one day be known as Africa, the
battle for existence had reached a new climax of ferocity, and
the victor was not yet in sight. In this barren and desiccated
land, only the small or the swift or the fierce could flourish,
or even hope to survive.
↪
↪
↪
↪
↪
↪
Упорядоченный список можно отформатировать с помощью соответствую-
щих цифр:
1. First instruction
1. Sub-instruction
1. Sub-instruction
1. Second instruction
Чтобы вложить один список в другой, добавьте отступ для элементов дочер-
него списка:
1. First instruction
1. Second instruction
1. Third instruction
Неупорядоченный (маркированный) список можно отформатировать с помо-
щью звездочек или тире:
* List item 1
* List item 2
* List item 3
58 Демидова А. В.
Архитектура ЭВМ
Чтобы вложить один список в другой, добавьте отступ для элементов дочер-
него списка:
- List item 1
- List item A
- List item B
- List item 2
Синтаксис Markdown для встроенной ссылки состоит из части [link text],
представляющей текст гиперссылки, и части (file-name.md) – URL-адреса или
имени файла, на который дается ссылка:
[link text](file-name.md)
или
[link text](http://example.com/ "Необязательная подсказка")
Markdown поддерживает как встраивание фрагментов кода в предложение,
так и их размещение между предложениями в виде отдельных огражденных
блоков. Огражденные блоки кода — это простой способ выделить синтаксис для
фрагментов кода. Общий формат огражденных блоков кода:
``` language
your code goes in here
```
4.2.2. Оформление формул в Markdown
Внутритекстовые формулы делаются аналогично формулам LaTeX. Например,
формула sin2(𝑥) + cos2(𝑥) = 1 запишется как
$\sin^2 (x) + \cos^2 (x) = 1$
Демидова А. В. 59
Архитектура ЭВМ
Выключение формулы:
sin2(𝑥) + cos2(𝑥) = 1 (4.1)
со ссылкой в тексте «Смотри формулу ({-eq. 4.1}).» записывается как
$$
\sin^2 (x) + \cos^2 (x) = 1
$$ {#eq:eq1}
Смотри формулу (`[-@eq:eq1]`).
4.2.3. Оформление изображений в Markdown
В Markdown вставить изображение в документ можно с помощью непосред-
ственного указания адреса изображения. Синтаксис данной команды выглядит
следующим образом:
![Подпись к рисунку](/путь/к/изображению.jpg "Необязательная
подсказка"){ #fig:fig1 width=70% }↪
Здесь:
• в квадратных скобках указывается подпись к изображению;
• в круглых скобках указывается URL-адрес или относительный путь изоб-
ражения, а также (необязательно) всплывающую подсказку, заключённую
в двойные или одиночные кавычки.
• в фигурных скобках указывается идентификатор изображения (#fig:fig1)
для ссылки на него по тексту и размер изображения относительно ширины
страницы (width=90%)
Ссылка на изображение (рис. 4.1) может быть оформлена следующим образом
(рис. [-@fig:fig1])
60 Демидова А. В.
Архитектура ЭВМ
Рис. 4.1. Подпись к рисунку
4.2.4. Обработка файлов в формате Markdown
Преобразовать файл README.md можно следующим образом:
pandoc README.md -o README.pdf
или так
pandoc README.md -o README.docx
Для компиляции отчетов по лабораторным работам предлагается использо-
вать следующий Makefile
FILES = $(patsubst %.md, %.docx, $(wildcard *.md))
FILES += $(patsubst %.md, %.pdf, $(wildcard *.md))
Демидова А. В. 61
Архитектура ЭВМ
LATEX_FORMAT =
FILTER = --filter pandoc-crossref
%.docx: %.md
-pandoc "$<" $(FILTER) -o "$@"
%.pdf: %.md
-pandoc "$<" $(LATEX_FORMAT) $(FILTER) -o "$@"
all: $(FILES)
@echo $(FILES)
clean:
-rm $(FILES) *~

# Выполнение лабораторной работы
1. Открываю терминал.
2. Перехожу в каталог курса сформированный при выполнении лаборатор-
ной работы No3.
Обновляю локальный репозиторий, скачав изменения из удаленного репози-
тория с помощью команды git pull (рис.1).
![(рис.1)]image/Снимок экрана от 2022-10-27 11-11-11.png){ #fig:001 width=70% }
3. Перехожу в каталог с шаблоном отчета по лабораторной работе No 4.
4. Провожу компиляцию шаблона с использованием Makefile. Для этого
ввожу команду make.Открываю и проверяю корректность полученных файлов (рис.2).
[(рис.2)](image/Снимок экрана от 2022-10-27 10-51-23.png){ #fig:001 width=70% }
5. Удаляю полученный файлы с использованием Makefile. Для этого введите
команду make clean (рис.3).
[(рис.3)](image/Снимок экрана от 2022-10-27 11-11-26.png){ #fig:001 width=70% }
Проверяю, что после этой команды файлы report.pdf и report.docx были
удалены (рис.4).
[(рис.4)](image/Снимок экрана от 2022-10-27 11-51-57.png){ #fig:001 width=70% }

6. Открываю файл report.md c помощью текстового редактора gedit (рис.5).
[(рис.5)](image/Снимок экрана от 2022-10-27 11-58-37.png){ #fig:001 width=70% }
Внимательно изучите структуру этого файла.
7. Заполняю отчет и скомпилирую отчет с использованием Makefile. Про-
веряю корректность полученных файлов. 
8. Загружаю файлы на Github (рис.6).
[(рис.6)](image/Снимок экрана от 2022-10-27 13-19-45.png){ #fig:001 width=70% }

# Выводы
В ходе данной лабараторной работы я освоил процедуры оформления отчетов с помощью
легковесного языка разметки Markdown.
