---
## Front matter
title: "Лабораторная работа №11"
subtitle: "Администрирование локальных сетей"
author: "Скандарова Полина Юрьевна"

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

Провести подготовительные мероприятия по подключению локальной сети организации к Интернету.

# Выполнение лабораторной работы

Вношу изменения в схему L1 сети, добавив в неё сеть провайдера и сеть модельного Интернета с указанием названий оборудования и портов подключения. Вношу изменения в схемы L2 и L3 сети, указав адреса и VLAN сети провайдера и модельной сети Интернета. Скорректируйте таблицы распределения IP-адресов и портов. На схеме предыдущего моего проекта размещаю необходимое оборудование для сети провайдера и сети модельного Интернета: 4 медиаконвертера (Repeater-PT), 2 коммутатора типа Cisco 2960-24TT, маршрутизатор типа Cisco 2811, 4 сервера (рис. [-@fig:001]).

![Схема сети с выходом в Интернет](image/1.PNG){#fig:001 width=70%}

Присваиваю названия размещённым в сети провайдера и в сети модельного Интернета объектам согласно модельным предположениям и схеме L1. В физической рабочей области добавляю здание провайдера и здание, имитирующее расположение серверов модельного Интернета. Присваиваю им соответствующие названия(рис. [-@fig:002]).

![Схема сети в физической рабочей области Packet Tracer](image/2.PNG){#fig:002 width=70%}

Переношу из сети «Донская» оборудование провайдера и модельной сети Интернета в соответствующие здания (рис. [-@fig:003]) (рис. [-@fig:004]).

![Оборудование в здании сети провайдера](image/3.PNG){#fig:003 width=70%}

![Оборудование в здании сети модельного Интернета](image/4.PNG){#fig:004 width=70%}

На медиаконвертерах заменяю имеющиеся модули на PT-REPEATER-NM-1FFE и PT-REPEATER-NM-1CFE для подключения витой пары по технологии Fast Ethernet и оптоволокна соответственно (рис. [-@fig:005]).

![Медиаконвертер с модулями PT-REPEATER-NM-1FFE и PT-REPEATER-NM-1CFE](image/5.PNG){#fig:005 width=70%}

Провожу соединение объектов согласно скорректированной схеме L1. Прописываю IP-адреса серверам согласно табл. 11.1 из руководства. Прописываю сведения о серверах на DNS-сервере сети «Донская» (рис. [-@fig:006]).

![Сведения о серверах на DNS-сервере сети «Донская»](image/6.PNG){#fig:006 width=70%}

# Выводы

Проведены подготовительные мероприятия по подключению локальной сети организации к Интернету.
