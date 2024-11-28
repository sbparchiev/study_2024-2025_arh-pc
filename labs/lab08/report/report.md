---
## Front matter
title: "Лабораторная работа №9"
subtitle: "Программирование цикла. Обработка аргументов командной строки."
author: "Парчиев Султан Багаудинович"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
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
biblatex: false
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

Приобретение навыков написания программ с использованием циклов и обработкой аргументов командной строки.

# Задание

1. Реализация циклов в NASM
2. Обработка аргументов командной строки
3. Выполнение заданий для самостоятельной работы
# Теоретическое введение

Стек — это структура данных, организованная по принципу LIFO («Last In — First Out» или «последним пришёл — первым ушёл»). Стек является частью архитектуры процессора и реализован на аппаратном уровне. Для работы со стеком в процессоре есть специальные регистры (ss, bp, sp) и команды. Основной функцией стека является функция сохранения адресов возврата и передачи аргументов при вызове процедур. Кроме того, в нём выделяется память для локальных переменных и могут временно храниться значения регистров. На рис. 8.1 показана схема организации стека в процессоре. Стек имеет вершину, адрес последнего добавленного элемента, который хранится в регистре esp (указатель стека). Противоположный конец стека называется дном. Значение, помещённое в стек последним, извлекается первым. При помещении значения в стек указатель стека уменьшается, а при извлечении — увеличивается. Для стека существует две основные операции: 
• добавление элемента в вершину стека (push); 
• извлечение элемента из вершины стека (pop).

# Выполнение лабораторной работы
1. Я создал каталог lab08 и файл lab8-1.asm

![Снимок экрана от 2024-11-28 10-51-45](https://github.com/user-attachments/assets/4efc10e7-f017-4279-9fc2-3e0a79eb22c1)

3. Я ввел текст первой программы в файл и создал исполняемый файл.

![Снимок экрана от 2024-11-28 11-04-15](https://github.com/user-attachments/assets/e7d1f0fd-7ac5-4745-ac74-f588db124e9e)

   Проверяю исполнение файла
   
![Снимок экрана от 2024-11-28 11-13-56](https://github.com/user-attachments/assets/0c299e5f-11bc-4626-92ed-30abe40e87dd)

4. Я изменил текст программы, в теле цикла label добавил строку sub eax,1. Цикл закольцевался и стал бесконечным.
   
![Снимок экрана от 2024-11-28 11-22-59](https://github.com/user-attachments/assets/857d0a8a-36d9-4d9c-8053-1841d03c03a7)

   Исполнение файла
   
![Снимок экрана от 2024-11-28 11-23-59](https://github.com/user-attachments/assets/95257255-9674-4627-aec3-5022fa277d00)

4.Я изменил текст программы так, чтобы цикл и счетчик работал правильно. В итоге после изменения программы, число проходки циклов стало соответствовать числу введенному с клавиатуры.

![Снимок экрана от 2024-11-28 11-28-11](https://github.com/user-attachments/assets/a717229d-c0f9-4c4c-b4b5-aa14141724d8)

Исполнение файла

![Снимок экрана от 2024-11-28 11-29-04](https://github.com/user-attachments/assets/d58c0265-4059-48d1-876d-884be723d00a)

5.Я создал файл lab8-2.asm и ввел туда программу, которая выводит все введенные аргументы. Программа выводит все 3 аргумента которые ввели, но в разной вариации.

![Снимок экрана от 2024-11-28 11-39-48](https://github.com/user-attachments/assets/bac1fa48-ff12-41dc-8e82-55aea282d3c8)

   Исполнение файла
   
![Снимок экрана от 2024-11-28 11-42-39](https://github.com/user-attachments/assets/fd9583ac-a3a2-4157-b568-730c46cc2d64)

6.Я создал фалй lab8-3.asm. Ввел текст программы и запустил ее. Программа вывела сумму чисел, которые я ввел.

![Снимок экрана от 2024-11-28 11-48-00](https://github.com/user-attachments/assets/2444da23-ab35-40e4-8144-307610b57bdf)

Исполнение файла

![Снимок экрана от 2024-11-28 12-31-32](https://github.com/user-attachments/assets/b343e50e-4910-4b37-b4cd-d1205dbe37fc)

# Самостоятельная работа

Я написал программу, которая выводит сумму всех решений примера для первого варианта.

![Снимок экрана от 2024-11-28 13-00-06](https://github.com/user-attachments/assets/6f603055-015b-4aff-9a29-35b94a3700d4)


# Выводы

При выполнении данной лабораторной работы я приобрел навыки написания программ с использованием цикла.

# Список литературы{.unnumbered}
Архитектура ЭВМ
::: {#refs}
:::
