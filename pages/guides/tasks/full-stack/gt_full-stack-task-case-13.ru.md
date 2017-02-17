---
title: Вариант 13 - «Агрегатор контактов»
keywords: Tasks
sidebar: guide-tasks_sidebar
toc: true
permalink: ru/gt_full-stack-task-case-13.html
folder: guides/tasks/
lang: ru
---

## Задание

В рамках выполнения практической части курса вами будет разработан сквозной пример: приложение «Агрегатор контактов».  
Первая часть практического задания будет посвящена освоению базовых технологий, таких как C#, базы данных, клиентские технологии и т.п., вторая часть будет включать изучение возможностей платформы Flexberry для эффективного создания приложений.

## Общее описание предметной области

Требуется создать приложение, позволяющее объединять контакты (друзей) из различных социальных сетей в единый список. Приложение предоставляет некоторые возможности, среди которых:

* Если у текущего пользователя есть контакты (друзья) из социальных сетей, которые также зарегистрированы в данном приложении, то приложение даёт возможность добавить в контакты (друзья) его профиль в альтернативной социальной сети (если он не был добавлен ранее).
* Поиск возможных знакомых людей на основе анализа графа контактов.

Технические требования:

*	Приложение реализуется в виде ASP.NET WebForms-приложения.
*	Данные хранятся в БД MSSQL Server.

## Практическое задание №1 - Серверная разработка (C#, .NET, ASP.NET)

Для реализации потребуется:

* Microsoft Visual Studio 2015
* Git for Windows

### Задание. Часть 1.

Требуется реализовать эффективный алгоритм сопоставления профилей пользователей. На вход подаётся 2 профиля пользователя, каждый из которых представляет собой массив строк, каждая строка представляет собой одно из следующих значений (в указанном порядке):

* Логин
* E-Mail
* Фамилия
* Имя
* Отчество
* Пол
* Дата рождения
* Город
* Страна
* Вебсайт

Любое из указанных полей может отсутсвовать, часть полей могут оказаться не на своём месте. Алгоритм должен выдавать на сколько % два указанных профиля соответствуют друг другу.  
Реализацию следует сделать в виде .net-библиотеки и подготовить модульные тесты для неё, продемонстрировать процент покрытия кода модульными тестами (чем больше, тем лучше).

### Задание. Часть 2.

Реализовать простое ASP.NET WebForms-приложение (на данном этапе без БД), которое содержит компоненты (ascx-контролы), реализующиие:

1.	Логику сопоставления двух пользователей с использованием библиотеки из 1-й части задания (поля для ввода значений, кнопка, блок с отображением результатов).
2.	Отображение в виде таблицы общего списка друзей (таблица, в которой количество столбцов соответствует количеству подключенных социальных сетей, а в строках указывается логин контакта в соответствующей социальной сети).

### Предоставление результатов выполнения работы на проверку

Реализованное решение (Visual Studio Solution) полностью разместить в репозитории на GitHub (решение должно компилироваться и запускаться). Ссылку на репозиторий предоставить преподавателям курса.

## Практическое задание №2 - Клиентская разработка (HTML, CSS, JS, jQuery)

Для реализации потребуется:

* Редактор кода для клиентской разработки: Visual Studio Code, Atom, Sublime Text и т.п.
* Git for Windows

### Задание

С использованием возможностей HTML, CSS, JS, jQuery сверстать форму, на которой будет отображаться список контактов в виде "плашек". Каждая плашка должна содержать всю имеющуюся информацию о контакте, но часть информации должна показываться во всплывающем по клику блоке. Контакты не должны дублироваться (один и тот же контакт из различных социальных сетей отображается на одной плашке). На форме также должен быть блок с информацией об общем количестве контактов. 

### Предоставление результатов

Реализованный проект разместить в репозитории на GitHub в виде встроенных страниц [GitHub Pages](https://pages.github.com/), позволяющих просматривать готовый результат. Ссылку на репозиторий и опубликованный таким образом проект предоставить преподавателям курса.

## Практическое задание №3 - Базы данных

Для реализации потребуется:

*	Microsoft SQL Server
*	Microsoft SQL Server Management Studio
*	Git for Windows

### Задание

Для указанной предметной области реализовать базу данных, заполнить базу скриптами (минимум по 5 записей на таблицу). Реализовать скрипты по созданию констрейнтов, индексов. Приложить скрипты создания БД и заполнения, бакап БД.  
Подготовить SQL-скрипты для получения следующей информации:

1. Вывести топ N пользователей, имеющих максимальное количество контактов.
2. Вывести самую часто встречающуюся фамилию пользователей.
3. Вывести статистику количества пользователей по каждому типу подключенной социальной сети в разрезе поло-возрастных групп.
4. Получить среднее количество контактов для пользователей в приложении.
5. Вывести процентное соотношение между полами пользователей в приложении.

### Предоставление результатов

Реализованные скрипты закоммитить в GitHub-репозиторий. Ссылку на репозиторий предоставить преподавателям курса.

## Практическое задание №4 - Проектирование ИС

Для реализации потребуется:

*	Flexberry Designer

### Задание

Нарисовать UML-диаграммы для обозначенной предметной области. Состав диаграмм определяется самим слушателем курсов, но должен обеспечивать полноценное описание предметной области.

### Предоставление результатов

Результатом работы является выгруженная в формате CRP стадия из Flexberry Designer. Стадию (файл с расширением *.CRP) следует закоммитить в репозиторий на GitHub, ссылку предоставить преподавателям курса.

## Практическое задание №5 - Объектный дизайн и генерация приложений

Для реализации потребуется:

*	Flexberry Designer
*	Microsoft Visual Studio 2015
*	Microsoft SQL Server
*	Git for Windows

### Задание

Выполнить объектный дизайн и генерацию ASP.NET-приложения для описанной предметной области. В качестве основы использовать реализованные ранее UML-модели. Генерация приложения и БД должна быть выполнена средствами Flexberry Designer приложение должно соответствовать требованиям и быть полностью работоспособным. Представления должны быть качественно настроены, подписи к классам и атрибутам на формах должны быть адекватными. Перечень форм и атрибутивный состав должны соответствовать предметной области и покрывать все требуемые бизнес-функции.

### Предоставление результатов

Сгенерированное приложение и скрипты создания БД следует выложить в репозиторий на GitHub. Предоставить преподавателям ссылку на репозиторий.

## Практическое задание №6 - Разработка бизнес-логики приложений

Для реализации потребуется:

* Flexberry Designer
* Microsoft Visual Studio 2015
* Microsoft SQL Server
* Git for Windows

### Задание

В сгенерированном при помощи Flexberry Designer приложении требуется реализовать:

* Страницу, на которой выводились бы результаты тех же 5-ти статистических запросов, реализованных при помощи SQL в задании 3, только в этот раз запросы нужно реализовать не на языке SQL, а с помощью Flexberry ORM средствами LINQ-провайдера и LoadingCustomizationStruct.
* Бизнес-логику приложения с помощью Flexberry ORM и бизнес-серверов.
  * Реализовать бизнес-сервер, который будет проверять уникальность логинов пользователей по каждому из типов подключенных социальных сетей.
  * Реализовать бизнес-сервер, который будет вызывать логику получения контактов из подключенных для текущего пользователя социальных сетей и обновления объектов в БД.
  * Реализовать бизнес-сервер, который будет использовать .net-библиотеку и связывать контакты из различных социальных сетей.
  * Реализовать бизнес-сервер, который при удалении пользователя или контакта помечает его как неактуальный и прячет из интерфейса приложения.
  * Добавить нехранимое поле в класс пользователя, которое будет показывать общее количество контактов пользователя., количество учащихся.

### Предоставление результатов

Доработанная бизнес-логика должна быть включена в разрабатываемое приложение и закоммичена в соответствующий репозиторий. Ссылка на репозиторий предоставляется для проверки преподавателям курса.

## Практическое задание №7 - Разработка UI-логики приложения

Для реализации потребуется:

*	Microsoft Visual Studio 2015
*	Microsoft SQL Server
*	Редактор кода для клиентской разработки: Visual Studio Code, Atom, Sublime Text и т.п.
*	Git for Windows

### Задание

Привязать реализованные ранее ascx-компоненты из задания №1 и №2 к данным из БД. Разместить данные компоненты на формах приложения.  
Реализовать логику регистрации пользователя через профиль социальной сети и привязку дополнительных профилей из других типов социальных сетей. Реализовать вызов API социальных сетей для получения информации о контактах пользователя.  
Требуется настроить красивый внешний вид для всех форм приложения. Улучшить визуальную тему оформления. Реализовать ярлыки на рабочем столе приложения для быстрого доступа к часто используемым функциям.  
Реализовать дополнительные формы, которые будут выводить результаты выполнения запросов из задания по БД.

### Предоставление результатов

Доработанная UI-логика должна быть включена в разрабатываемое приложение и закоммичена в соответствующий репозиторий. Ссылка на репозиторий предоставляется для проверки преподавателям курса.

## Практическое задание №8 - Функциональные подсистемы Flexberry

Для реализации потребуется:

*	Flexberry Designer
*	Microsoft Visual Studio 2015
*	Microsoft SQL Server
*	Git for Windows

### Задание

Для реализованного приложения настроить подсистему полномочий. Пользователи должны регистрироваться самостоятельно и получать назначение роли. Авторизация на основе форм. Создать иерархию ролей, добавить операции на просмотр данных о пользователях. Настроить несколько ролей и назначить эти роли пользователям.  
Настроить подсистему аудита. В разрабатываемом приложении все изменения объектов данных должно фиксироваться в подсистеме аудита. В навигационное меню следует добавить формы аудита, которые должны показываться только администраторам.

### Предоставление результатов

Доработанное приложение должно быть закоммичено в соответствующий репозиторий. Дополнительно в репозиторий должны быть добавлены SQL-скрипты, которые нужно выполнить для функционирования приложения с подсистемой полномочий и аудита. Ссылка на репозиторий предоставляется для проверки преподавателям курса.