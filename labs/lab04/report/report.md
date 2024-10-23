---
## Front matter
title: "Лабораторная работа №4"
subtitle: "Создание и процесс обработки программ на языке ассемблера NASM"
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

Освоение процедуры компиляции и сборки программ, написанных на ассемблере NASM

# Выполнение лабораторной работы

Создадим нужную директорию с помощью команды mkdir (Рис. 2.1):

![Создание каталога lab4](image/1.jpg)

Теперь переместимся в созданный нами каталог (Рис. 2.2):

![Перемещение в созданный каталог](image/2.jpg)

Создадим файл hello с расширением .asm, в котором мы будем писать код на ассемблере (Рис. 2.3):

![Создание .asm файлы](image/3.jpg)

Для того, чтобы редактировать созданный файл, воспользуемся текстовым редактором gedit (Рис. 2.4):

![Открытие созданного файла с помощью gedit](image/4.png)

Вставим в открытый файл следующий код (Рис. 2.5):

![Редактирование файла](image/5.jpg)

Теперь нам необходимо превратить наш файл в объектный. Этим занимается транслятор NASM. Введём следующую команду (Рис. 2.6):

![Компиляция файла с помощью nasm](image/6.png)

Далее проверим, создался ли объектный файл с помощью команды ls (Рис. 2.7):

![Проверка на успешное создание файла](image/7.jpg)

Теперь попробуем использовать полный вариант команды NASM (Рис. 2.8):

![Использование команды nasm с большим количеством аргументов](image/8.jpg)

Проверим, создался ли файл с помощью команды ls (Рис. 2.9):

![Проверка на успешное создание файлов](image/9.jpg)

Для создания исполняемого файла необходимо использовать компоновщик ld, который соберёт объектный файл. Напишем следующую команду (Рис. 2.10):

![Сборка исполняемого файла с помощью ld](image/10.jpg)

Проверим, создался ли файл с помощью команды ls (Рис. 2.11):

![Проверка на успешное создание исполняемого файла](image/11.jpg)

Теперь соберём файл obj.o в файл main (Рис. 2.12):

![Сборка исполняемого файла main из файла obj.o](image/12.jpg)

Проверим, создался ли файл. Снова пропишем команду ls (Рис. 2.13):

![Проверка на успешное создание исполняемого файла](image/13.jpg)

Теперь запустим файл hello, для этого мы должны написать ./ и название файла (Рис. 2.14):

![Запуск исполняемого файла](image/14.jpg)

# Выполнение задания для самостоятельной работы

Скопируем файл hello.asm в каталог ~/work/arch-pc/lab04 под названием lab4.asm (Рис. 3.1):

![Копирование файла](image/15.png)

Внесём изменения в скопированный файл. Для этого откроем его в gedit (Рис. 3.2):

![Открытие файла для редактирования](image/16.jpg)

Теперь изменим третью строчку, заменив фразу Hello world! на фамилию и имя (Рис. 3.3):

![Процесс редактирования файла](image/17.jpg)

Теперь скомпилируем полученный файл в объектный. Для этого воспользуемся командой nasm и укажем формат elf и нужный файл для компиляции (Рис. 3.4):

![Компиляция файла в объектный](image/18.jpg)

Теперь соберём полученный объектный файл. Укажем формат elf_i386 и объектный файл для сборки (lab4.o). Укажем, что выходной файл должен быть назван lab4 (Рис. 3.5):

![Сборка объектного файла в исполняемый](image/19.jpg)

Убедимся в том, что сделали всё правильно. Для этого запустим собранный файл (Рис. 3.6):

![Запуск собранного файла](image/20.jpg)

Теперь скопируем файл hello.asm в каталог 4 лабораторной работы (Рис. 3.7):

![Копирование файла hello.asm в каталог 4 лабораторной работы](image/21.jpg)

Эту же операцию проведём для файла lab4.asm (Рис. 3.8):

![Копирование файла lab4.asm в каталог 4 лабораторной работы](image/22.jpg)

Теперь загрузим результат проделанной лабораторной работы на GitHub (Рис. 3.9):

![Загрузка проделанной работы на GitHub](image/23.jpg)

# Выводы

В результате выполнения лабораторной работы появилось понимание того, как работает алгоритм создания исполняемого файла из кода на ассемблере, а также появились навыки работы с языком nasm, компиляции кода в объектный файл и сборкой исполняемых программ.

