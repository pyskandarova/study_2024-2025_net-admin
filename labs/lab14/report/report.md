---
## Front matter
title: "Лабораторная работа 14"
subtitle: "Администрирование локальных сетей"
author: "Полина Юрьевна Скандарова"

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

Настроить взаимодействие через сеть провайдера посредством статической маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного в г. Сочи.

# Задание

1. Настроить связь между территориями (рис. [-@fig:001] , рис. [-@fig:002] , рис. [-@fig:003] , рис. [-@fig:004], рис. [-@fig:005]).
2. Настроить оборудование, расположенное в квартале 42 в Москве (рис. [-@fig:006] , рис. [-@fig:007] , рис. [-@fig:008] , рис. [-@fig:009]).
3. Настроить оборудование, расположенное в филиале в г. Сочи (рис. [-@fig:010] , рис. [-@fig:011]).
4. Настроить статическую маршрутизацию между территориями (рис. [-@fig:012] , рис. [-@fig:013] , рис. [-@fig:014]).
5. Настроить статическую маршрутизацию на территории квартала 42 в г. Москве (рис. [-@fig:015] , рис. [-@fig:016]).
6. Настроить NAT на маршрутизаторе msk-donskaya-gw-1 (рис. [-@fig:017]).

# Выполнение лабораторной работы

Настройка линка между площадками

![Настройка интерфейсов коммутатора provider-sw-1](image/1.PNG){#fig:001 width=70%}

![Настройка интерфейсов маршрутизатора msk-donskaya-gw-1](image/2.PNG){#fig:002 width=70%}

![Настройка интерфейсов маршрутизатора msk-q42-gw-1](image/3.PNG){#fig:003 width=70%}

![Настройка интерфейсов коммутатора sch-sochi-sw-1](image/4.PNG){#fig:004 width=70%}

![Настройка интерфейсов маршрутизатора sch-sochi-gw-1](image/5.PNG){#fig:005 width=70%}

Настройка площадки 42-го квартала

![Настройка интерфейсов маршрутизатора msk-q42-gw-1](image/6.PNG){#fig:006 width=70%}

![Настройка интерфейсов коммутатора msk-q42-sw-1](image/7.PNG){#fig:007 width=70%}

![Настройка интерфейсов маршрутизирующего коммутатора msk-hostel-gw-1](image/8.PNG){#fig:008 width=70%}

![Настройка интерфейсов коммутатора msk-hostel-sw-1](image/9.PNG){#fig:009 width=70%}

Настройка площадки в Сочи

![Настройка интерфейсов маршрутизатора sch-sochi-gw-1](image/10.PNG){#fig:010 width=70%}

![Настройка интерфейсов коммутатора sch-sochi-sw-1](image/11.PNG){#fig:011 width=70%}

Настройка маршрутизации между площадками

![Настройка маршрутизатора msk-donskaya-gw-1](image/12.PNG){#fig:012 width=70%}

![Настройка маршрутизатора msk-q42-gw-1](image/13.PNG){#fig:013 width=70%}

![Настройка маршрутизатора sch-sochi-gw-1](image/14.PNG){#fig:014 width=70%}

Настройка маршрутизации на 42 квартале

![Настройка маршрутизатора msk-q42-gw-1](image/15.PNG){#fig:015 width=70%}

![Настройка интерфейсов маршрутизирующего коммутатора msk-hostel-gw-1](image/16.PNG){#fig:016 width=70%}

Настройка NAT на маршрутизаторе msk-donskaya-gw-1

![Настройка NAT на маршрутизаторе msk-donskaya-gw-1](image/17.PNG){#fig:017 width=70%}

# Выводы

Настроено взаимодействие через сеть провайдера посредством статической маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного в г. Сочи.