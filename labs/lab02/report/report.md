---
## Front matter
title: "Лабораторная работа № 2"
subtitle: "Отчёт"
author: "Виноградова Мария Андреевна"

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
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучить идеологию и применение средств контроля
версий. Приобрести практические навыки по работе с системой git.


# Выполнение лабораторной работы 

1. Настройка github

1) Создаем учетную запись на сайте https://github.com/ и заполняем основные данные. (рис. @fig:001).

![Создаем учетную запись](/home/mavinogradova/Изображения/photo_2024-10-12_21-26-15.jpg){#fig:001 width=70%}

2. Базовая настройка git

1) Сначала сделаем предварительную конфигурацию git. Открываем терминал и вводим следующие команды, указав имя и email владельца репозитория. (рис. @fig:002 @fig:003).

![Задаем имя и email репозитория](/home/mavinogradova/Изображения/Снимок экрана 2024-10-12 212827.jpg){#fig:002 width=70%}

![Задаем имя и email репозитория](/home/mavinogradova/Изображения/Снимок экрана 2024-10-12 212835.jpg){#fig:003 width=70%}

2) Настроим utf-8 в выводе сообщений git, зададим имя начальной ветки (будем называть её master), параметр autocrlf, параметр safecrlf.(рис. @fig:004 @fig:005 @fig:006 @fig:007).

![Настраиваем utf-8](/home/mavinogradova/Изображения/photo_2024-10-12_21-09-09.jpg){#fig:004 width=70%}

![Задаем имя начальной ветки, как master](/home/mavinogradova/Изображения/Снимок экрана 2024-10-12 210438.jpg){#fig:005 width=70%}

![Устанавливаем настройку autocrlf](/home/mavinogradova/Изображения/Снимок экрана 2024-10-12 210446.jpg){#fig:006 width=70%}

![Устанавливаем параметр safecrlf](/home/mavinogradova/Изображения/photo_2024-10-12_21-09-16.jpg){#fig:007 width=70%}

3. Создание SSH ключа

1) Для последующей идентификации пользователя на сервере репозиториев необходимо сгенерировать пару ключей (приватный и открытый). Ключи сохранятся в каталоге ~/.ssh/. (рис. @fig:008).

![Генерация ключей](/home/mavinogradova/Изображения/photo_2024-10-12_21-09-30.jpg){#fig:008 width=70%}

2) Копируем ключ из локальной консоли в буфер обмена. (рис. @fig:009).

![Копируем ключ](/home/mavinogradova/Изображения/Снимок экрана 2024-10-12 213937.jpg){#fig:009 width=70%}

3) Далее необходимо загрузить сгенерированный открытый ключ. Для этого заходим на сайт http://github.org/ под своей учётной записью и переходим в меню Setting . После этого выбираем в боковом меню SSH and GPG keys и нажимаем кнопку New SSH key . Вставляем ключ в появившееся на сайте поле и указываем для ключа имя (Title).

4) Проверяем, что ключ появился в профиле на github. (рис. @fig:010).

![Проверка ключа](/home/mavinogradova/Изображения/photo_2024-10-12_21-11-06.jpg){#fig:010 width=70%}

4. Создание рабочего пространства и репозитория курса на основе шаблона

1) Открываем терминал и создаем каталог для предмета «Архитектура
компьютера». (рис. @fig:011).

![Создаем каталог](/home/mavinogradova/Изображения/Снимок экрана 2024-10-12 214309.jpg){#fig:011 width=70%}

5. Создание репозитория курса на основе шаблона

1) Переходим на страницу репозитория с шаблоном курса
https://github.com/yamadharma/course-directory-student-template.

2) Выбираем Use this template. (рис. @fig:012).

![Выбираем Use this template](/home/mavinogradova/Изображения/photo_2024-10-12_21-10-50.jpg){#fig:012 width=70%}

3) Создаем имя репозитория “study_2024-2025_arhpc”. (рис. @fig:013).

![Создаем имя репозитория](/home/mavinogradova/Изображения/photo_2024-10-12_21-45-54.jpg){#fig:013 width=70%}

4) Открывем терминал и переходим в каталог курса, клонируем созданный репозиторий. (рис. @fig:014).

![Клонируем созданный репозиторий](/home/mavinogradova/Изображения/photo_2024-10-12_21-13-03.jpg){#fig:014 width=70%}

6. Настройка каталога курса

1) Переходим в каталог курса, удаляем лишние файлы. (рис. @fig:015).

![Переходим в нужный каталог](/home/mavinogradova/Изображения/Снимок экрана 2024-10-12 210623.jpg){#fig:015 width=70%}

2) Создаем необходимые каталоги (рис. @fig:016).

![Создаем необходимые каталоги](/home/mavinogradova/Изображения/Снимок экрана 2024-10-12 210631.jpg){#fig:016 width=70%}

3) Отправляем файлы на сервер (рис. @fig:017).

![Отправляем файлы](/home/mavinogradova/Изображения/photo_2024-10-12_21-13-12.jpg){#fig:017 width=70%}

4) Проверяем правильность создания иерархии рабочего пространства в
локальном репозитории и на странице github. (рис. @fig:018).

![Проверяем правильность создания иерархии](/home/mavinogradova/Изображения/Снимок экрана 2024-10-12 210653.jpg){#fig:018 width=70%}

7. Выполнение самостоятельной работы
Скопируем отчет по выполненной лабораторной работе №1 в соответствующие каталоги созданного рабочего пространства(labs->lab01- >report). Зайдя в свой аккаунт в github, затем перейдя в репозиторий по предмету “Архитектура компьютера”, в указанные каталоги мы видим, что все успешно загрузилось. Дальше так же загрузим и отчет по проделанной лабораторной работе №2. (рис. @fig:019 @fig:020 @fig:021).

![Копируем отчет](/home/mavinogradova/Изображения/photo_2024-10-12_21-10-50.jpg){#fig:019 width=70%}

![Копируем отчет](/home/mavinogradova/Изображения/photo_2024-10-12_21-52-17.jpg){#fig:020 width=70%}

![Проверяем github](/home/mavinogradova/Изображения/photo_2024-10-12_21-52-21.jpg){#fig:021 width=70%}


# Выводы

В процессе выполнения лабораторной работы №2 я изучила идеологию и применения средств контроля версий, ее функции и разнообразие.Я приобрела практические навыки по работе с одной из популярных систем контроля версии, с системой git. Познакомилась с основными командами git и с web-сервисом github, который требуется для работы с git. Создала рабочее пространство и репозиторий на основе шаблона и SSH-ключи, также научилась работать с каталогами курса, рабочего пространства. А в конце,пользуясь приобретенными знаниями, загрузила отчет по лабораторной работе №1 в соответствующий каталог, созданного мной репозитория.

