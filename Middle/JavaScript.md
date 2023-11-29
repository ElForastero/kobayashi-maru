
## Итераторы и генераторы

* Что такое итерируемые объекты и итераторы? Рассказать про протоколы итерирования:
	* Iterable
	* Iterator
	* Async Iterable
	* Async Iterator
* Зачем нужны итерируемые объекты, если уже есть массивы? 
* В чём разница между перебором массива и итерируемого объекта через конструкции: ```for```, ```for of```, ```for in```?
* Что такое генераторы? Где они могут пригодиться?
* Рассказать про методы объекта-генератора:
	* next
	* throw
	* return
* Что такое композиция генераторов?
* Как вы думаете, почему в качестве ключевого слова используется именно `yield`?
* Как происходит работа с async generators?

#### Ресурсы

* [Итераторы](https://learn.javascript.ru/iterable)
* [Генераторы](https://learn.javascript.ru/generators)
* [Async iterators and generators](https://javascript.info/async-iterators-generators)
* [You Don't Know JS: Async & Performance. Chapter 4: Generators](https://github.com/getify/You-Dont-Know-JS/blob/1st-ed/async%20%26%20performance/ch4.md)
* [Iteration Protocols](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols)

## Set, Map

* Set
	* Что такое?
	* Как создать инстанс?
	* Какие методы существуют у инстанса?
	* Как можно перебрать?
	* Может ли содержать одинаковые элементы?
	* Где может быть полезен?
* Map
	* Что такое?
	* Как создать инстанс?
	* Какие методы существуют у инстанса?
	* Как можно перебрать?
	* В чем отличие от обычного объекта?
	* Где может быть полезен?
* WeakSet/WeakMap
	* Что такое?
	* В чем отличия от Set/Map?
	* Где могут быть полезны?

#### Ресурсы

* [Map и Set](https://learn.javascript.ru/map-set)
* [Map (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
* [WeakMap и WeakSet (learn.javascript.ru)](https://learn.javascript.ru/weakmap-weakset)

## Proxy

* Что такое Proxy? Для чего он нужен? Когда он может быть полезен?
* Как создать Proxy?
* Какие действия может перехватывать Proxy?
* Что такое инварианты в Proxy?
* Что такое Reflect и для чего он нужен?

#### Ресурсы

* [Proxy (learn.javascript.ru)](https://learn.javascript.ru/proxy)

## Объекты

+ Что такое геттеры и сеттеры? Как ими пользоваться в JS нативным способом?
+ Дескрипторы свойств объектов: что такое и что позволяют делать?
+ Приведение объектов к примитивам: когда происходит и как работает?
	+ Как сделать так, чтобы было возможно сложение двух объектов?
    ```javascript
    const a = { x: 3 };
    const b = { x: 5 };
    ...
    console.log(a + b); // 8
    ```
	+ Как сделать так, чтобы следующее выражение вернуло `true`?
    ```javascript
    (c==1 && c==2 && c==3)
    ```

#### Ресурсы

+ [Object to primitive conversion](https://javascript.info/object-toprimitive)
+ [ToPrimitive алгоритм в спецификации](https://www.ecma-international.org/ecma-262/9.0/index.html#sec-toprimitive)

## Массивы

+ Можно ли прервать обход элементов в методе `forEach`?
+ Можно ли с помощью метода `indexOf` определить позицию подмассива `[3, 4]` в массиве `[1, 2, [3, 4], 5]`?
+ Как строку преобразовать в массив? Можно ли для строк применить методы массивов?
+ Что делают, как и когда использовать следующие методы массивов:
	* `copyWithin`
	* `flat`
	* `flatMap`
	* `with`

## Функции

+ Что такое "всплытие" объявления переменных, и в каком случае у функций тут появляются особенности?
+ Влияет ли директива `use strict` на "всплытие"? Как избежать "всплытия" переменных?
+ Что такое IIFE (immediately invoked function expression)? Какие есть способы написать IIFE и почему это так работает?
+ Как сделать так, чтобы при вызове immediately invoked function expression сохранялся родительский контекст?
+ Как использовать стандартные методы массива для ненастоящих массивов (например, вызвать `map` для `arguments`) и почему это работает?

#### Ресурсы

+ [Immediately-Invoked Function Expression (IIFE)](http://benalman.com/news/2010/11/immediately-invoked-function-expression/)
+ [How does Array.prototype.slice.call() work?](https://stackoverflow.com/questions/7056925/how-does-array-prototype-slice-call-work)

## Promises

* Что такое Promise? Для чего он нужен?
* Как создать Promise?
	* Когда выполняется коллбэк, передаваемый аргументом в конструктор промиса?
* Методы `then`, `catch`, `finally`
	* Для чего используются?
	* Что такое цепочка промисов?
	* Что могут возвращать их коллбеки?
	* Как возвращаемое значение влияет на состояние промиса, возвращаемого данным методом?
* В чем отличие между `then(resolveHandler).catch(rejectHandler)` и `then(resolveHandler, rejectHandler)`?
* Можно ли отменить выполнение промиса?
* Для чего нужны и как использовать следующие методы:
	* `Promise.resolve`
	* `Promise.reject`
	* `Promise.all`
	* `Promise.allSettled`
	* `Promise.race`
	* `Promise.any`
* В чем преимущества и недостатки коллбэков и промисов?
* Какое состояние и результат будут у следующего промиса и почему:
  ```javascript
    const promise = new Promise((resolve, reject) => {
      resolve(0);
      reject(1);
      resolve(2);
    });
  ```
* Что такое async/await?
	* Где можно применять ключевое слово `await`?
	* Как обрабатывать ошибки для async/await?
  
#### Ресурсы

* [JavaScript — from callbacks to async/await](https://medium.freecodecamp.org/javascript-from-callbacks-to-async-await-1cc090ddad99)
* [Promise (learn.javascript.ru)](https://learn.javascript.ru/promise)
* [We have a problem with promises](https://pouchdb.com/2015/05/18/we-have-a-problem-with-promises.html)
* [You're Missing the Point of Promises](https://blog.domenic.me/youre-missing-the-point-of-promises/#toc_1)
* [You Don't Know JS: Async & Performance](https://github.com/leonardomso/You-Dont-Know-JS/tree/master/async%20%26%20performance) [(рус.)](https://github.com/devSchacht/You-Dont-Know-JS/tree/master/async%20%26%20performance) - можно прочесть первые три главы