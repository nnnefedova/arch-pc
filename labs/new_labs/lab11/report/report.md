---
## Front matter
title: "Отчёт по лабораторной работе №11"
author: "Нефёдова Наталия Николаевна"

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

Приобретение навыков написания программ для работы с файлами.

# Выполнение лабораторной работы

## Порядок выполнения лабораторной работы

1. Создайте каталог для программам лабораторной работы № 11, перейдите в него и создайте файл lab11-1.asm и readme.txt

2. Введите в файл lab11-1.asm текст программы из листинга 11.1 (Программа записи в файл сообщения). Создайте исполняемый файл и проверьте его работу. 

3. С помощью команды chmod измените права доступа к исполняемому файлу lab11-1, запретив его выполнение. Попытайтесь выполнить файл. Объясните результат. 

4. С помощью команды chmod измените права доступа к файлу lab11-1.asm с исходным текстом программы,добавив права на исполнение. Попытайтесь выполнить его и объясните результат. 

5. Предоставить права доступа к файлу readme.txt в соответствии с вариантом в таблице 11.4. Проверить правильность выполнения с помощью команды ls -l.

## 1

Создадим каталог для программам лабораторной работы № 11, перейдем в него и создайте файл lab11-1.asm и readme.txt (рис. [-@fig:001])

![1](image/1.jpg){ #fig:001 width=70% }

## 2

Введем в файл lab11-1.asm текст программы из листинга 11.1 (Программа записи в файл сообщения). Создадим исполняемый файл и проверим его работу. (рис. [-@fig:002]), (рис. [-@fig:003])

![2](image/2.jpg){ #fig:002 width=70% }

![3](image/3.jpg){ #fig:003 width=70% }

## 3

С помощью команды chmod изменим права доступа к исполняемому файлу lab11-1, запретив его выполнение. Попытаемся выполнить файл. В команде используется значение “666” - набор прав, расшифровывается как “110 110 110” в двоичной форме записи и “rw- rw- rw-” - в символьной. Таким образом, мы запрещаем исполнение файла, что и сказано при попытке выполнить файл (“отказано в доступе”) (рис. [-@fig:004])

![4](image/4.jpg){ #fig:004 width=70% }

## 4

С помощью команды chmod изменим права доступа к файлу lab11-1.asm с исходным текстом программы, добавив права на исполнение и попытаемся выполнить его. В команде используется значение “777” - набор прав, расшифровывается как “111 111 111” в двоичной форме записи и “rwx rwx rwx” - в символьной. Таким образом, мы добавляем права доступа к исполнению файла, и на попытку выполнить файл нам не выдается ошибка. (рис. [-@fig:005])

![5](image/5.jpg){ #fig:005 width=70% }

## 5

Предоставим права доступа к файлу readme.txt в соответствии с вариантом 15 в таблице 11.4 и проверим правильность выполнения с помощью команды ls -l. В первом случае нам дана символьная запись “-wx –x rwx”, которую переводим в двоичную форму “011 001 111” = “317” в восьмеричной форме. Во втором случае дана запись “010 101 010” в двоичной форме = “252” в восьмеричной. (рис. [-@fig:006])

![6](image/6.jpg){ #fig:006 width=70% }

## Задание для самостоятельной работы

Напишем программу работающую по следующему алгоритму:
- Вывод приглашения “Как Вас зовут?” 
- ввести с клавиатуры свои фамилию и имя 
- создать файл с именем name.txt 
- записать в файл сообщение “Меня зовут”
- дописать в файл строку введенную с клавиатуры 
- закрыть файл 

Создадим исполняемый файл и проверить его работу. Проверим наличие файла и его содержимое с помощью команд ls и cat. Создадим файл lab11-2.asm для выполнения работы. Напишем программу работающую по следующему алгоритму 
- Вывод приглашения “Как Вас зовут?” 
- Ввод с клавиатуры свои фамилию и имя 
- Создание файла с именем name.txt 
- Запись в файл сообщения “Меня зовут” 
- Добавление в файл строки, введенной с клавиатуры 
- Закрытие файла

(рис. [-@fig:007])(рис. [-@fig:008])(рис. [-@fig:009])

![7](image/7.jpg){ #fig:007 width=70% }

![8](image/8.jpg){ #fig:008 width=70% }

![9](image/9.jpg){ #fig:009 width=70% }

# Выводы

В ходе лабораторной работы были приобретены навыки написания программ для работы с файлами.
