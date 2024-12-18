---
## Front matter
title: "Лабораторная работа №3"
subtitle: "Язык разметки Markdown"
author: "Парчиев Султан Багаудинович"

## Generic otions
lang: ru-RU

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
fontsize: 13pt
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
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Овладеть практическими навыками легковесного языка разметки Markdown.


# Выполнение лабораторной работы

1. Я обновил локальный репозиторий скачав изменения из удаленного репозитория. 

![Снимок экрана от 2024-12-18 18-35-11](https://github.com/user-attachments/assets/0d217caa-b6fc-4530-ae9c-4b7de1755218)


1.2. Я проверил команду make, она создала два файла report.docx и report.pdf


1.3. C помощью команды make clean я отчистил созданные файлы и проверил это.


1.4. С помощью текстового редактора gedit открыл файл report.md.


1.5. Я заполнил отчет в файле report.md.


1.6. Я перенес файлы на github.


# Выполнение самостоятельной работы.

2.1. В соответствующем каталоге я сделал отчет по лабораторной работе №3. 


2.2. Я создал отчета в формате *.docx и *.pdf.


2.3. Я загрузил файлы на github.

!
# Выводы

Я овладел практическими навыками легковесного языка разметки Markdown.


:::
