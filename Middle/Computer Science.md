## Базовые принципы алгоритмизации

###  Парадигмы проектирования алгоритмов

* По каждой из парадигм:
	* дайте определение;
	* перечислите недостатки и преимущества;
	* приведите алгоритмы использующие эту парадигму.
* Brute-force
* Divide and Conquer
* Dynamic Programming
* YAGNI

### Анализ и оценка сложности

* Что такое Space complexity?
* Что такое Time complexity?
* Что такое RAM? (Random access machine, [определение смотреть здесь](https://www.google.com/search?q=the+algorithm+design+manual+2nd+edition+steven+skiena))
* Что значит сложность худшего случая? Лучшего? Среднего?
* Дайте опредление для каждого из обозначений:
	* О (Big Oh)
	* Ω (Big Omega)
	* θ (Big Theta)
* Какое практическое применение имеет оценка сложности алгоритмов?

##### Ресурсы
1. [Wiki: Algorithm](https://en.wikipedia.org/wiki/Algorithm) [[RUS]](https://ru.wikipedia.org/wiki/%D0%90%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC)
2. [The Algorithm Design Manual Second Edition, Skiena](https://www.google.com/search?q=the+algorithm+design+manual+2nd+edition+steven+skiena)  Chapter 2
3. [Horowitz and Sahani Fundamentals Of Computer Algorithms 2nd edition](https://www.academia.edu/39717003/Horowitz_and_sahani_fundamentals_of_computer_algorithms_2nd_edition) Chapters 1, 3, 4, 5
4. [Essential Algorithms: A Practical Approach to Computer Algorithms](https://www.google.com/search?source=hp&ei=MZCJXu-dLZeDk74P6ciQuAo&q=essential+algorithms+a+practical+approach+&oq=essential+algorithms+a+practical+approach+&gs_lcp=CgZwc3ktYWIQAzICCAAyAggAMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgYIABAWEB4yBggAEBYQHjoFCAAQgwE6BAgAEAo6CQgAEAoQRhD_AToECAAQDToFCAAQzQJKMggXEi4wZzkwZzEwN2cxMTBnMTA2ZzEwNmcxMDlnMTE3ZzExNmcxMTNnMTQ5ZzBnMTExSh0IGBIZMGcxZzFnMWcxZzFnMWcxZzFnMWczZzBnMlBHWN0hYI0saABwAHgAgAGtAYgBzAuSAQM4LjaYAQCgAQGqAQdnd3Mtd2l6&sclient=psy-ab&ved=0ahUKEwiv-uvj6NDoAhWXwcQBHWkkBKcQ4dUDCAc&uact=5)  Chapter 1
5. [Introduction to Asymptotic Analysis](http://www.cs.cornell.edu/courses/cs312/2004fa/lectures/lecture16)

## Структуры данных

* Что такое абстрактный тип данных?
* Каким типом данных, абстрактным типом данных и какой структурой данных является DOM tree?

##### Ресурсы
* [Wiki: Data type](https://en.wikipedia.org/wiki/Data_type)
* [Wiki: Data structure](https://en.wikipedia.org/wiki/Data_structure)
* [Wiki: Abstract data type](https://en.wikipedia.org/wiki/Abstract_data_type)
* [Geeksforgeeks: Abstract data types](https://www.geeksforgeeks.org/abstract-data-types/)
* [Programming with abstract data types](http://web.cs.iastate.edu/~hridesh/teaching/362/07/01/papers/p50-liskov.pdf)
* Narasimha Karumanchi, Data Structures And Algorithms Made Easy. Chapter 1

### Хэш таблица

* Что такое коэффициент заполнения?
* Что такое коллизия?
* Рассказать про политики разрешения коллизий:
  * Прямое связывание
  * Открытая адресация (линейное и квадратичное пробирования, двойное хэширование)

##### Ресурсы
* [Essential Algorithms: A Practical Approach to Computer Algorithms](https://www.google.com/search?source=hp&ei=MZCJXu-dLZeDk74P6ciQuAo&q=essential+algorithms+a+practical+approach+&oq=essential+algorithms+a+practical+approach+&gs_lcp=CgZwc3ktYWIQAzICCAAyAggAMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgYIABAWEB4yBggAEBYQHjoFCAAQgwE6BAgAEAo6CQgAEAoQRhD_AToECAAQDToFCAAQzQJKMggXEi4wZzkwZzEwN2cxMTBnMTA2ZzEwNmcxMDlnMTE3ZzExNmcxMTNnMTQ5ZzBnMTExSh0IGBIZMGcxZzFnMWcxZzFnMWcxZzFnMWczZzBnMlBHWN0hYI0saABwAHgAgAGtAYgBzAuSAQM4LjaYAQCgAQGqAQdnd3Mtd2l6&sclient=psy-ab&ved=0ahUKEwiv-uvj6NDoAhWXwcQBHWkkBKcQ4dUDCAc&uact=5)  Chapter 8
* Narasimha Karumanchi, Data Structures And Algorithms Made Easy. Chapter 4, 7

### Списки

* Что такое смежные стуктуры данных? Связанные? В чём разница?
* Что такое связанный список?
* В каких случаях используется?

##### Ресурсы
* [The Algorithm Design Manual Second Edition](https://www.google.com/search?q=The+Algorithm+Design+Manual+Second+Edition&oq=The+Algorithm+Design+Manual+Second+Edition&aqs=chrome..69i57.1669j0j1&sourceid=chrome&ie=UTF-8) Chapter 3
* [Essential Algorithms: A Practical Approach to Computer Algorithms](https://www.google.com/search?source=hp&ei=MZCJXu-dLZeDk74P6ciQuAo&q=essential+algorithms+a+practical+approach+&oq=essential+algorithms+a+practical+approach+&gs_lcp=CgZwc3ktYWIQAzICCAAyAggAMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgYIABAWEB4yBggAEBYQHjoFCAAQgwE6BAgAEAo6CQgAEAoQRhD_AToECAAQDToFCAAQzQJKMggXEi4wZzkwZzEwN2cxMTBnMTA2ZzEwNmcxMDlnMTE3ZzExNmcxMTNnMTQ5ZzBnMTExSh0IGBIZMGcxZzFnMWcxZzFnMWcxZzFnMWczZzBnMlBHWN0hYI0saABwAHgAgAGtAYgBzAuSAQM4LjaYAQCgAQGqAQdnd3Mtd2l6&sclient=psy-ab&ved=0ahUKEwiv-uvj6NDoAhWXwcQBHWkkBKcQ4dUDCAc&uact=5) Chapter 3

### Графы и деревья

#### Графы

* Что значит "ориентированный граф"? "Неориентированный граф"?
* Способы представления:
	* Что значит "матрица инцидентности"?
	* Что значит "матрица смежности"?
	* Что значит "список смежности"?
* Каково определение маршрута, пути, цикла? Чем отличаются эти понятия?
* Что такое "Эйлеров путь" и "Эйлеров цикл"?
* Что такое "Гамильтонов путь" и "Гамильтонов цикл"?

##### Ресурсы
* [Глоссарий теории графов](https://ru.m.wikipedia.org/wiki/%D0%93%D0%BB%D0%BE%D1%81%D1%81%D0%B0%D1%80%D0%B8%D0%B9_%D1%82%D0%B5%D0%BE%D1%80%D0%B8%D0%B8_%D0%B3%D1%80%D0%B0%D1%84%D0%BE%D0%B2)
* Narasimha Karumanchi, Data Structures And Algorithms Made Easy. Chapter 9
* Омельченко, Теория графов. Главы 1-3
* [Курс "Основы теории графов". Разделы 1-2](https://stepik.org/126)

#### Деревья

* Какое дерево называют "полным" (complete)?
* Что такое "бинарное дерево"?
* Что такое "бинарное дерево поиска"?
* Что такое сбалансированное дерево? Самобалансирующееся? Для чего используется?

##### Ресурсы
* [Difference between Binary Tree and Binary Search Tree](https://www.geeksforgeeks.org/difference-between-binary-tree-and-binary-search-tree/)
* [Essential Algorithms: A Practical Approach to Computer Algorithms](https://www.google.com/search?source=hp&ei=MZCJXu-dLZeDk74P6ciQuAo&q=essential+algorithms+a+practical+approach+&oq=essential+algorithms+a+practical+approach+&gs_lcp=CgZwc3ktYWIQAzICCAAyAggAMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgYIABAWEB4yBggAEBYQHjoFCAAQgwE6BAgAEAo6CQgAEAoQRhD_AToECAAQDToFCAAQzQJKMggXEi4wZzkwZzEwN2cxMTBnMTA2ZzEwNmcxMDlnMTE3ZzExNmcxMTNnMTQ5ZzBnMTExSh0IGBIZMGcxZzFnMWcxZzFnMWcxZzFnMWczZzBnMlBHWN0hYI0saABwAHgAgAGtAYgBzAuSAQM4LjaYAQCgAQGqAQdnd3Mtd2l6&sclient=psy-ab&ved=0ahUKEwiv-uvj6NDoAhWXwcQBHWkkBKcQ4dUDCAc&uact=5)  Chapter 10
* Narasimha Karumanchi, Data Structures And Algorithms Made Easy. Chapter 9

## Алгоритмы

### Алгоритмы на графах и деревьях

#### Алгоритм поиска в глубину (DFS)

* Что это?
* Описать алгоритм работы.

##### Ресурсы
* Narasimha Karumanchi, Data Structures And Algorithms Made Easy. Chapter 9

#### Алгоритм поиска в ширину (BFS)

* Что это?
* Описать алгоритм работы.
* В каких случая предпочтителен BFS, а в каких — DFS?

##### Ресурсы
* Narasimha Karumanchi, Data Structures And Algorithms Made Easy. Chapter 9

### Сортировки
* Зачем нужны сортировки?
* Что значит "устойчивая сортировка"?

#### Быстрая сортировка
* Описать алгоритм работы

##### Ресурсы
* [Essential Algorithms: A Practical Approach to Computer Algorithms](https://www.google.com/search?source=hp&ei=MZCJXu-dLZeDk74P6ciQuAo&q=essential+algorithms+a+practical+approach+&oq=essential+algorithms+a+practical+approach+&gs_lcp=CgZwc3ktYWIQAzICCAAyAggAMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgYIABAWEB4yBggAEBYQHjoFCAAQgwE6BAgAEAo6CQgAEAoQRhD_AToECAAQDToFCAAQzQJKMggXEi4wZzkwZzEwN2cxMTBnMTA2ZzEwNmcxMDlnMTE3ZzExNmcxMTNnMTQ5ZzBnMTExSh0IGBIZMGcxZzFnMWcxZzFnMWcxZzFnMWczZzBnMlBHWN0hYI0saABwAHgAgAGtAYgBzAuSAQM4LjaYAQCgAQGqAQdnd3Mtd2l6&sclient=psy-ab&ved=0ahUKEwiv-uvj6NDoAhWXwcQBHWkkBKcQ4dUDCAc&uact=5) Chapter 6
* Narasimha Karumanchi, Data Structures And Algorithms Made Easy. Chapter 10

### Поиск

#### Бинарный поиск
* Что это и для каких целей нужен?
* Описать алгоритм работы

##### Ресурсы
* [Essential Algorithms: A Practical Approach to Computer Algorithms](https://www.google.com/search?source=hp&ei=MZCJXu-dLZeDk74P6ciQuAo&q=essential+algorithms+a+practical+approach+&oq=essential+algorithms+a+practical+approach+&gs_lcp=CgZwc3ktYWIQAzICCAAyAggAMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgYIABAWEB4yBggAEBYQHjoFCAAQgwE6BAgAEAo6CQgAEAoQRhD_AToECAAQDToFCAAQzQJKMggXEi4wZzkwZzEwN2cxMTBnMTA2ZzEwNmcxMDlnMTE3ZzExNmcxMTNnMTQ5ZzBnMTExSh0IGBIZMGcxZzFnMWcxZzFnMWcxZzFnMWczZzBnMlBHWN0hYI0saABwAHgAgAGtAYgBzAuSAQM4LjaYAQCgAQGqAQdnd3Mtd2l6&sclient=psy-ab&ved=0ahUKEwiv-uvj6NDoAhWXwcQBHWkkBKcQ4dUDCAc&uact=5) Chapter 7
* Narasimha Karumanchi, Data Structures And Algorithms Made Easy. Chapter 11

### Практические задачи по алгоритмам

Перед прохождением заданий необходимо зарегистрироваться на [курсе](https://stepik.org/126). Рекомендуется посмотреть хотя бы одну лекцию на шаг до задания, чтобы было легче разобраться в нём. Также можно пройти разделы 1 и 2 курса, для общего развития, это не обязательное условие.

* [Найти количество компонент связности неориентированного графа при помощи поиска в глубину](https://stepik.org/lesson/9934/step/9?unit=10930)
* [Найти наименьшие пути от начальной вершины при помощи поиска в ширину](https://stepik.org/lesson/9934/step/16?unit=10930)
* [Найдите эйлеров цикл в графе](https://stepik.org/lesson/10765/step/12?unit=10933)