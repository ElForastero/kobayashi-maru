## Базовые принципы проектирования

* Что такое абстрагирование? Какие есть отличия между абстракцией, инкапсуляцией и скрытием информации?
* MVVM
- MVP
- IoC
- SOA
- EDA
- DDD

### Frontend

- Что такое Flux архитектура?
- В чём основная особенность Atomic подхода к разработке компонентов?

### SOLID

#### Общее

- Когда принципы SOLID могут быть полезны?
- В каких случаях следует избегать применения принципов SOLID?
- Как доказать или опровергнуть следующее утверждение?

> Принципы SOLID работают как единая целостная система. Каждый из принципов делает кодовую базу более сопровождаемой определенным образом, ограничивая одну из сторон кодовой базы. При совместном применении принципы направляют разработчика к проектированию продуманного в различных измерениях решения.
> 
> - SRP подсказывает, как разделить кодовую базу без потери целостности каждой части.
> - OCP подсказывает, как сделать систему расширяемой, если можно спрогнозировать будущие изменения.
> - LSP подсказывает, как не совершать популярных, но неочевидных ошибок в полиморфизме подтипов.
> - ISP подсказывает, как подключать подсистемы друг к другу. Модули, сформированные в соответствии с SRP, не всегда достаточно минимальны для своего клиента, иногда модули с одной причиной изменения могут иметь несколько клиентов с разными контрактами.
> - DIP определяет, как контролировать взаимозависимости. Следование DIP позволяет изучать каждый модуль в отдельности и быть многократно используемым. Но даже в совокупности принципы SOLID не охватывают всех аспектов хорошего проектирования.

##### Ресурсы

- [Bob Martin SOLID Principles of Object Oriented and Agile Design](https://www.youtube.com/watch?v=TMuno5RZNeE)
- [Принципы проектирования классов (S.O.L.I.D.)](https://blog.byndyu.ru/2009/10/solid.html)
- [OTA SOLID (интерактивный ресурс)](https://ota-solid.now.sh/)
- [SOLID Principles with Uncle Bob - Robert C. Martin](https://www.hanselminutes.com/145/solid-principles-with-uncle-bob-robert-c-martin)
- [The Principles of OOD](http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod) (contains links to original papers about SOLID, those papers are definitely recommended to be read)
- Adaptive Code: Agile coding with design patterns and SOLID principles. Second Edition (Gary McLean Hall, Part III, Chapters 7-11)

#### Принцип единой ответственности (SRP)

- Что такое принцип единой ответственности?
- В чем заключается цель SRP?
- Что такое ответственность в контексте SRP?
- Что означает "причина для изменения" в контексте SRP?
- Может ли одна и та же "причина для изменения" использоваться в разных модулях?
- Какие принципы проектирования дополняют SRP и помогают не переусердствовать с декомпозицией?
- Можно ли применять SRP, если у нас нет прогноза развития системы (например, мы совершенно не знакомы с проектом)?
- Как SRP связан с принципом DRY?
- Какова связь между SRP и связностью?
- В чем разница между SRP и принципом разделения ответственности?
- Может ли SRP быть полезным и для проекта, написанного в парадигме FP?

##### Ресурсы

- [The Single Responsibility Principle](https://blog.cleancoder.com/uncle-bob/2014/05/08/SingleReponsibilityPrinciple.html)
- [Think you understand the Single Responsibility Principle?](https://hackernoon.com/you-dont-understand-the-single-responsibility-principle-abfdd005b137)
- [On the Criteria To Be Used in Decomposing Systems into Modules](https://www.win.tue.nl/~wstomv/edu/2ip30/references/criteria_for_modularization.pdf) (closely related to SRP)
- [Review of "On the criteria to be used in decomposing systems into modules"](https://blog.acolyer.org/2016/09/05/on-the-criteria-to-be-used-in-decomposing-systems-into-modules/)
- [The Modular Structure of Complex Systems](https://www.researchgate.net/publication/2814490_The_Modular_Structure_of_Complex_Systems)

#### Принцип открытости-закрытости (OCP)

- О чём гласит принцип открытости-закрытости?
- Что означают понятия "открытый для расширения" и "закрытый для модификации"?
- Какова цель OCP?
- Какие преимущества дает закрытие широко используемых модулей для модификации?
- Как сделать модуль открытым для расширения?
- Все ли модули вашего проекта должны следовать OCP? Если нет, то какой из них должен?
- Как архитектура, основанная на плагинах, связана с OCP?
- Почему абстракции необходимы, если вы хотите следовать OCP?
- Как выбрать виды изменений, от которых следует закрывать дизайн модуля?
- Почему предоставление доступа на чтение/запись к состоянию через свойства публичного класса приводит к нарушению принципа OCP?
- Почему следование OCP проще, если не нарушается SRP?
- Как OCP может привести к преждевременному обобщению?
- Может ли OCP быть полезной и для проекта, написанного в стиле FP?

##### Ресурсы

- [An Open and Closed Case](http://blog.cleancoder.com/uncle-bob/2013/03/08/AnOpenAndClosedCase.html)
- [The Open Closed Principle](https://blog.cleancoder.com/uncle-bob/2014/05/12/TheOpenClosedPrinciple.html)
- [The Open-Closed Principle and what hides behind it](https://hackernoon.com/the-open-closed-principle-c3dc45419784)
- [Patterns in Practice. The Open Closed Principle](https://docs.microsoft.com/en-us/archive/msdn-magazine/2008/june/patterns-in-practice-the-open-closed-principle)

#### Принцип замещения Лискова (LSP)

- Что такое принцип замещения Лискова?
- Какова цель LSP?
- Каким образом нарушение LSP приводит к нарушению OCP?
- Когда квадрат может быть унаследован от прямоугольника, а когда нет, согласно LSP?
- Почему LSP требует рассматривать внешнее публичное поведение модуля как непротиворечивое, а не только внутреннее частное поведение?
- Может ли LSP быть полезен и для проекта, написанного в стиле FP?

##### Ресурсы

- [The Liskov Substitution Principle — and why you might want to enforce it](https://medium.com/hackernoon/the-liskov-substitution-principle-and-why-you-might-want-to-enforce-it-6f5bbb05c06d)
- [SOLID Class Design: The Liskov Substitution Principle](https://www.tomdalling.com/blog/software-design/solid-class-design-the-liskov-substitution-principle/)

#### Принцип разделения интерфейсов (ISP)

- Что такое принцип разделения интерфейсов?
- Какова цель применения ISP?
- Как ISP помогает решить проблему классов, реализующих несвязанные интерфейсы?
- Как нарушение принципа ISP может привести к нарушению LSP?
- Может ли принцип ISP быть полезен и для проекта, написанного в стиле FP?

##### Ресурсы

- [The Interface Segregation Principle — it’s confused](https://medium.com/@jim_ej/the-interface-segregation-principle-its-confused-aa856de97d36)

#### Принцип инверсии зависимостей (DIP)

- Что такое принцип инверсии зависимостей?
- В чем заключается цель DIP?
- Какие модули являются "высокоуровневыми", а какие - "низкоуровневыми" в контексте DIP?
- Всегда ли сквозные проблемы являются "низкоуровневыми"? Почему?
- Что такое "инверсия" зависимостей в контексте DIP?
- Как DIP связана с OCP?
- Где должна быть объявлена абстракция, связывающая высокоуровневые и низкоуровневые модули? Может ли она быть объявлена в низкоуровневом модуле, а затем импортирована в высокоуровневый?
- Нарушает ли DIP библиотека (например, React), если она конкретна и широко используется в вашем проекте?
- Что такое принцип стабильных зависимостей (SDP) и как он связан с DIP?
- Что такое метрика стабильности и что она измеряет?
- Почему модули с высокой стабильностью имеют тенденцию быть менее изменчивыми?
- Почему модули с наименьшей стабильностью называют безответственными и зависимыми?
- Какие проблемы возникают, если все модули в системе максимально устойчивы? Или максимально неустойчивы?
- Что такое принцип стабильных абстракций (The Stable Abstractions Principle) и как он связан с SDP?
- Почему метрики неустойчивости и абстракции должны быть сбалансированы?
- Что такое главная последовательность, в которой сумма показателей неустойчивости и абстракции равна 1?
- Может ли DIP быть полезен и для проекта, написанного в стиле FP?

##### Ресурсы

- [The Dependency Inversion Principle. C++ Report.](https://www.labri.fr/perso/clement/enseignements/ao/DIP.pdf)
- [OO Design Quality Metrics](https://linux.ime.usp.br/~joaomm/mac499/arquivos/referencias/oodmetrics.pdf)
- [Stability](https://drive.google.com/file/d/0BwhCYaYDn8EgZjI3OTU4ZTAtYmM4Mi00MWMyLTgxN2YtMzk5YTY1NTViNTBh/view)
- [Dependency Inversion Implies Interfaces Are Owned by High-level Modules](https://mikhail.io/2016/05/dependency-inversion-implies-interfaces-are-owned-by-high-level-modules/)
- [DIP in the Wild](https://martinfowler.com/articles/dipInTheWild.html)

## Инверсия управления

### Что такое IoC?

- В чем преимущества фреймворков, предоставляющих IoC, перед библиотеками?
- В чем преимущества библиотек без IoC перед фреймворками?
- Может ли модуль предоставлять интерфейс, поддерживающий оба подхода: с IoC и без IoC?

### Инъекция зависимостей

- Что такое DI?
- Каковы альтернативы DI? Каковы преимущества и недостатки каждой альтернативы?
- Можно ли реализовать DI без IoC?
- Как DI помогает достичь разделения забот?
- Как связаны между собой DI и принцип инверсии зависимостей из SOLID?

Что такое несоответствие импеданса? Каковы примеры несоответствия импеданса в различных технологиях? Каковы наиболее популярные паттерны решений?
Какие проблемы могут быть вызваны преждевременной оптимизацией? Как решить проблемы с производительностью, избегая преждевременной оптимизации?
Каковы преимущества предоставления API с различными уровнями абстракции?
Почему обратные вызовы нарушают композитность?

### Large Scale JS

- В чем заключается основная идея предлагаемого подхода?
- Какие паттерны используются в этом подходе?
- Какова роль событий в этом подходе? Можно ли реализовать подобный подход только с помощью синхронных вызовов функций?
- Как это помогает достичь отказоустойчивости?
- Как модули могут зависеть друг от друга?

### API модуля

- Каковы характеристики хорошего API модуля?
- Как сделать так, чтобы API было сложно использовать не по назначению? Каковы преимущества этой характеристики?
- Что такое свойства согласованности и концептуальной целостности API? Почему эти свойства ценны?
- Как написание сценариев использования перед написанием кода может помочь добиться чистоты API?
- В чем разница между расширяемостью авторами модулей и клиентами модулей?
- Как вы можете объяснить фразу "Асимметрия функции должна отражаться асимметрией формы"?
- Как имена, используемые в API вашего модуля, могут отражать структуру вашего модуля и повышать связность различных частей вашего контракта?
- Что такое крайние случаи в контексте проектирования API? Почему неявная обработка краевых случаев предпочтительнее явной?
- О чем говорит правило "Лучший API - это отсутствие API"? Каковы примеры нарушения этого правила?

- Как модульное программирование помогает нам достичь лучшего локального рассуждения при разработке модуля?
- Какие преимущества дает декларирование явного контракта между клиентом и тем, кто реализует модуль?
- В чем разница между абстракцией путем параметризации и абстракцией путем спецификации?

#### Ресурсы

- [How To Design Better JavaScript APIs](https://www.smashingmagazine.com/2012/10/designing-javascript-apis-usability/) (little bit opinionated post, don't consider as perfect guide)
- [Library patterns Multiple levels of abstraction](http://tomasp.net/blog/2015/library-layers/)
- [Library patterns Why frameworks are evil](http://tomasp.net/blog/2015/library-frameworks/)
- [A quick intro to Dependency Injection: what it is, and when to use it](https://www.freecodecamp.org/news/a-quick-intro-to-dependency-injection-what-it-is-and-when-to-use-it-7578c84fa88f/) [[Перевод](https://medium.com/@xufocoder/a-quick-intro-to-dependency-injection-what-it-is-and-when-to-use-it-de1367295ba8)]
- [Inversion of Control Containers and the Dependency Injection pattern](https://martinfowler.com/articles/injection.html)
- [Dependency injection (from Wikipedia)](https://en.wikipedia.org/wiki/Dependency_injection)
- [The Little Manual of API Design](https://people.mpi-inf.mpg.de/~jblanche/api-design.pdf)
- [Modular Programming: Modules and Signatures](https://www.cs.cornell.edu/courses/cs3110/2013sp/lectures/lec07-modules/lec07.html)
- [Patterns For Large-Scale JavaScript Application Architecture](https://addyosmani.com/largescalejavascript/)
- [Создание архитектуры программы или как проектировать табуретку](https://habr.com/ru/post/276593/)