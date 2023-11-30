
### Frontend

- В чём заключаются основные принципы Feature Sliced (Feature Driven) архитектуры?

### Общее

- Что вкладывается в понятие чистой архитектуры (clean architecture)?
- Из каких уровней (или слоёв) состоит проект построенный по принципам чистой архитектуры?
- Как структура команды влияет на выбор архитектурных решений?
- Что гласит закон Конвея?
* Что такое Cross-cutting concerns? Что значит coarse-grained и fine-grained ответственность?
* Архитектурные паттерны enterprise приложений
* Паттерны облачных вычислений
* Цикломатическая сложность
* Использование инструментов автоматического анализа вроде SonarQube
- Что такое "кричащая" (screaming) архитектура и о чём она кричит?
- [Tell Don't Ask](https://martinfowler.com/bliki/TellDontAsk.html)

### FSD

- В чём смысл Feature Sliced и Feature Driven архитектуры?

### UML-диаграмы

- ER диаграммы
- Data Flow диаграммы
- Диаграммы классов
- Юзкейсы
- Диаграммы последовательности

#### Coupling

* Что такое Coupling? 
* Рассказать с примерами про следующие виды coupling:
	* Content coupling
	* Common coupling
	* External coupling
	* Control coupling
	* Stamp (data-structured) coupling
	* Data coupling
* Как абстрагирование влияет на Coupling? 

#### Cohesion 

* Что такое Cohesion?  
* Рассказать с примерами про следующие виды cohesion:
	* Coincidental cohesion
	* Logical cohesion
	* Temporal cohesion
	* Procedural cohesion
	* Communicational/informational cohesion
	* Sequential cohesion
	* Functional cohesion
* Является ли величина Cohesion обратной величине Coupling?

#### Separation of concerns

* Что это такое?
* Какие преимущества даёт следование этому принципу?
* Что подразумевают под горизонтальным и вертикальным separation of concerns?
* Возможно ли вертикальное разделение без горизонтального и наоборот?
* Как связан с Cohesion?

#### Simplicity

* Как Рич Хики в своём докладе "Simple Made Easy" описывает отличие Simple от Easy? Зачем в первую очередь стоит стремится к простоте, а не к лёгкости?
* В чём заключается принцип KISS?
* Как KISS помогает в формировании ментальных моделей? В чём ценность этих моделей?
* Как участие в разработке требований от бизнеса может помочь следованию KISS?
* Когда абстрагирование противоречит KISS?
* Почему наследование может приводить к нарушению KISS?
* В чём заключается принцип YAGNI? Как он соотносится с принципом KISS?

#### DRY

* В чём основная идея принципа DRY?
* Как принцип связан с Cohesion?
* Почему этот принцип неразрывно связан с SPOT (Single point of truth)?
* Какие есть примеры дублирования кода, которые не нарушают DRY?
* Какие есть примеры копирования кода бизнес-логики, которые также не нарушают DRY?
* Как следование принципу DRY может привести к нарушению KISS?
* Как следование принципу DRY может привести к Premature Generalization?
* Почему при попытке убрать дублирование, когда повторов этого кода ещё мало (до 4-5), мы можем легко ошибиться и выбрать неверный способ рефакторинга? Какая здесь аналогия со статистикой?
* Как вы объясните фразу "Duplication is far cheaper than the wrong abstraction."?

###  Ресурсы

* [Abstraction, Encapsulation, and Information Hiding](http://www.tonymarston.co.uk/php-mysql/abstraction.txt)
* [Difference between Abstraction and Encapsulation](https://www.guru99.com/difference-between-abstraction-and-encapsulation.html#2)
* [Cohesion](https://www.chegg.com/learn/computer-science/computer-software/module-cohesion)
* [Coupling](https://www.chegg.com/learn/computer-science/computer-software/module-coupling)
* [The DRY Principle Explained: Its Benefit and Cost with Examples](https://thevaluable.dev/dry-principle-explained/) [[Перевод](https://habr.com/ru/company/mailru/blog/349978/)]
* [Why DRY? by Mark Seemann](https://blog.ploeh.dk/2014/08/07/why-dry/)
* [Repeat yourself, do more than one thing, and rewrite everything](https://programmingisterrible.com/post/176657481103/repeat-yourself-do-more-than-one-thing-and)
* [The Wrong Abstraction](https://www.sandimetz.com/blog/2016/1/20/the-wrong-abstraction)
* [A Detailed Explanation of The KISS Principle in Software](https://thevaluable.dev/kiss-principle-explained/)
* [Simple Made Easy — talk of Rich Hickey](https://www.infoq.com/presentations/Simple-Made-Easy/)
* [The Art of Separation of Concerns](http://aspiringcraftsman.com/2008/01/03/art-of-separation-of-concerns/)
* [Cross cutting concern example on SO](https://stackoverflow.com/questions/23700540/cross-cutting-concern-example)
* [Cross cutting concern on Wiki](https://en.wikipedia.org/wiki/Cross-cutting_concern)
* [Coarse-grained vs fine-grained on SO](https://stackoverflow.com/questions/3766845/coarse-grained-vs-fine-grained)

## Паттерны проектирования

- В чем разница между структурными, порождающими и поведенческими видами паттернов?
- По каждому паттерну ответить на вопросы:
	- В чем заключается суть паттерна?
	- Какие проблемы можно решить с помощью данного паттерна?
	- Какие у него есть недостатки?
	- Какие можно привести примеры использования данного паттерна?
	- К какому виду относится данный паттерн и почему?
	- С какими принципами из SOLID данный паттерн связан и каким образом?
- Singleton
- Strategy
- Template method
- Factory, Factory Method, Abstract Factory
- Observer/mediator
- Facade
- Decorator
- Command
- Component
- Какие примеры реализации этих паттернов можно привести в функциональном языке, или же в языке, где функции являются объектами первого класса, имеют замыкания и не имеют встроенных средств реализации для выражения классического ОО подхода?

### Ресурсы

- [Clojure Design Patterns](http://mishadoff.com/blog/clojure-design-patterns/)
- [Refactoring guru: design patterns](https://refactoring.guru/ru/design-patterns)

## CQRS

- Что такое паттерн CQRS (Command Query Responsibility Segregation)?