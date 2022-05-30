# Orccraft

Ну чтош, рады приветствовать вас на одном из наших заданий-проектов!

Здесь вам предстоит окунуться в мир орков (а если быть точнее, то создать его). Здесь нет места слабости и малодушию. Гнев, слезы, разочарования - это лишь малая часть эмоций, которые вас поджидают вас при выполнении данного проекта. Погнали)

<img align="center" width="400" height="350" src="https://www.meme-arsenal.com/memes/f0856c9e3dbd77364924ace61fd5736d.jpg">

Общее задание: Реализовать систему учёта бойцов в легионе фентезийного войска

## Этап 1 - Создание основ Orccraft
### Требования:
- репозиторий в GitHub, все задачи разделить на ветки
- консольная программа
- добавление и удаление юнитов
- работа в реальном времени (при закрытии программы данные могут удаляться)
- функционал программы:
  - показать всех бойцов (order_by - отсортировав)
  - показать бойцов с фильтром (поле + значение)
  - показать конкретного бойца по уникальному идентификатору (тут какой хочешь)
  - добавить бойца
  - изменить бойца (поиск так же по уникальному идентификатору)
  - удалить бойца
- у бойцов имеются следующие атрибуты:
  - раса (эльф, орк, человек)
  - класс бойца (можно обойтись тремя: маг, лучник и воин)
  - здоровье (hp)
  - интеллект, ловкость, сила
  - оружие (можно похимичить с оружием и вынести его в отдельный класс)
  - количество стрел (если лучник)
  - тип брони (если воин)
  - мана (mp, если маг)

### Пример:
```shell
$ unit_data_manager
>> 1. Show
>> 2. Insert
>> 3. Update
>> 4. Delete

>> Show

>> 1. All
>> 2. Order by <field>
>> 3. <id>
>> 4. Where <field> == <value>

>> All

>> Unit(race='human', class='warrior', hp=1000, strength=100500, agility=1005, intelligence=500, armor='middle')
>> Unit(race='orc', class='warrior', hp=100000, strength=100500, agility=1005, intelligence=10, armor='hard')
>> Unit(race='elf', class='mage', hp=100, mp=15010, strength=100, agility=100, intelligence=100500, armor=100)
>> Unit(race='human', class='bowman', hp=500, strength=100, agility=100500, intelligence=500, armor=10, arrows=150)

>> Continue? [Y(yes)/N(no)]: 
```

### Задания:
1.


## Этап 2
### Требования:
- так же консольная программа
- сохранение в файл (лучше всего подойдет либо json, либо csv форматы. Расширение должно быть .owdat)
- генерация случайных данных
- распределение по:
  - контуберниям (8-10 юнитов)
  - центуриям (60-100 юнитов)
  - манипулам (120-200 юнитов)
  - когортам (500-1000 юнитов)
- разделить оружие на ближнее, дальнее и магическое, сделать отдельным классом, если не сделано
- оружие должно лежать в отдельном файле с индексом солдата, к которому оно привязано

## Этап 3
### Требования:
- подключить базу данных SQLite
- несколько потоков:
  - 1 - обрабатывает консоль
  - 2 - взаимодействует с базой данных
  - 3 - обрабатывает запросы и полученные данные
  - ВНИМАНИЕ: смотри "гонка за ресурсами"
- красивые загрузки и раскрасить консоль
- система пользователей (админ, менеджер, поддержка, работник)

## Этап 4
### Требования
- развернуть базу данных docker-compose (PostgresSQL, MySQL, **MS SQL Server**)
- сделать CI/CD + тесты
- использовать ORM для взаимодействия с бойцами (*либо можно сделать самому)0)0)))))
- *написать программу для битвы двух армий (тут придётся долго думать....)

## Этап 5
### Требования
- написать сервер RESTful API (beast standalone, либо любое другое решение, одобренное преподавателем)
- написать клиентскую часть с GUI (
[**Dear ImGUI**](https://github.com/ocornut/imgui),
[Ultralight](https://ultralig.ht/),
[Sciter](https://sciter.com/),
[**NanoGUI**](https://github.com/wjakob/nanogui) и милая [статеечка](https://habr.com/ru/post/468485/))
), которая будет общаться с сервером
- GUI **необязательно** красивый
- сделать сайт с аналогичным дизайном (можно на шаблонах, Vue.js/React.js)
- бот в телеграмме для администрирования
