---
## Front matter
title: "Лабораторная работа №3"
subtitle: "Язык разметки Markdown"
author: "Яковлева Дарья Сергеевна"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Целью работы является освоение процедуры оформления отчетов с помощью легковесного
языка разметки Markdown.

# Выполнение лабораторной работы

откроем терминал и переместимся в рабочий каталог (Рис. 1):

![Рисунок 1. Перемещение в рабочий каталог](image/1.jpg)

Обновим локальный репозиторий с помощью команды git pull. Так мы синхронизируем файлы на компьютере с файлами на Github (Рис. 2):

![Рисунок 2. Использование git pull](image/2.jpg)

Перейдём в каталог лабораторной работы номер 3 (Рис. 3):

![Рисунок 3. Перемещение в каталог 3 лабораторной работы](image/3.jpg)

Проведём компиляцию шаблона отчёта с помощью команды make (Рис. 4):

![Рисунок 4. Использование команды make](image/4.jpg)

Проверим, создались ли файлы .docx и .pdf (Рис. 5 - 7):

![Рисунок 5. Проверка создания файлов](image/5.jpg)

![Рисунок 6. Проверка docx файла](image/6.jpg)

![Рисунок 7. Проверка pdf файла](image/7.jpg)

Удалим файлы .docx и .pdf командой make clean (Рис. 8):

![Рисунок 8. Использование команды make clean](image/8.jpg)

А теперь проверим, удалились ли файлы отчёта (Рис. 9):

![Рисунок 9. Проверка удалённых файлов](image/9.jpg)

Теперь откроем файл отчёта report.md с помощью редактора gedit (Рис. 10):

![Рисунок 10. Открытие файла отчёта с помощью gedit](image/10.jpg)

Начнём заполнять файл report.md (Рис. 11):

![Рисунок 11. Структура файла отчёта](image/11.jpg)

После заполнения отчёта прописываем команду make, чтобы скомпилировать готовый отчёт (Рис. 12):

# Выполнение задания для самостоятельной работы

# Выводы

В результате выполнения лабораторной работы были получены навыки работы с языком разметки Markdown, а также были заполнены отчёты для двух лабораторных работ.

