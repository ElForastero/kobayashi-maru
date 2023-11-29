* Что такое Render Prop? Где и как может использоваться такой приём?
* Custom Hooks
	* Как и для чего создавать пользовательские хуки?
	* Как правильно именовать пользовательские хуки? Почему?

### useEffect

* Нужно ли указывать функции в виде зависимостей эффектов?
* Что выведется в консоли для следующего кода, если быстро нажать 5 раз на кнопку, и почему?
    ```javascript
    function Counter() {
      const [count, setCount] = useState(0);

      useEffect(() => {
        setTimeout(() => {
          console.log(`You clicked ${count} times`);
        }, 3000);
      });

      return (
        <div>
          <p>You clicked {count} times</p>
          <button onClick={() => setCount(count + 1)}>
            Click me
          </button>
        </div>
      );
    }
    ```
* Как сделать так, что бы все 5 раз вывелось последнее значение, то есть цифра 5?
* Что выведется в консоли для следующего кода, если несколько раз быстро нажать на кнопку?
    ```javascript
    function Example() {
      const [count, setCount] = useState(0);

      useEffect(() => {
        console.log(count);
        if (count % 2 === 0) {
          return () => setTimeout(() => console.log("It was even render"), 1000);
        } else {
          return () => setTimeout(() => console.log("It was odd render"), 1000);
        }
      });

      return (
        <div>
          <p>You clicked {count} times</p>
          <button onClick={() => setCount(count + 1)}>Click me</button>
        </div>
      );
    }
    ```

### Performance

* Для чего в хук `useState` можно передавать функцию вместо `initialState`?
* Когда передача инлайн-коллбека ухудшает производительность и почему? Пример: `<LoginButton onClick={(e) => handleClick(e, user)}>`
* Как и для чего использовать хуки `useMemo` и `useCallback`? 
* Всегда ли следует оборачивать код в `useMemo`/`useCallback`?
* Что такое `React.memo`? Для чего он нужен?
	* Когда его стоит, а когда не стоит использовать?
	* Какие ограничения накладываются на пропсы при использовании `React.memo`?
	- Почему использование `React.memo` для `MemoComponent` таким образом не приносит никакой пользы (укажите на конкретные проблемные места):
```javascript
const outerComponent = ({ options, dataForClick, onComponentClick }) => {
  const makeClickHandler = (dataForClick) => {
	return () => onComponentClick(dataForClick);
  }

  const enhanceOptions = () => {
	const uppercased = {};
	Object.keys(options).forEach(key => {
	  uppercased[key] = options[key].toUpperCase();
	})
	return uppercased;
  }

  return (
	<MemoComponent
	  onClick={makeClickHandler(dataForClick)}
	  options={enhanceOptions()}
>
	  <div>This is <b>Memo Component!</b></div>
	</MemoComponent>
  );
};
```    

- Что такое windowing или virtualizing списков?
- Всегда ли происходит перерисовка DOM-элемента, если `shouldComponentUpdate` вернул `true`?

### State Management

* Какие есть способы организации состояния, когда в этом состоянии нуждаются несколько компонентов?
* Почему поднятие состояния до общего родителя может быть неудобным?
* Для чего предназначен хук `useReducer`? Как с ним работать?

### Context

* Что такое Context object? Как его создать? Из чего он состоит?
* Как использовать хук `useContext`?
* Как обновить Context из глубоко вложенной компоненты (т.е. пробрасывать коллбэк в таком случае - очень неудобное решение)?
* Можно ли вкладывать провайдеры одного и того же Context друг в друга? Из какого провайдера при этом будут браться данные?
* Почему не стоит злоупотреблять Context?

### Portals

* Что это такое? Зачем нужны? Как использовать?
* Как будет работать контекст и event bubbling в случае с порталами?

### Error Boundaries

* Что такое Error Boundaries? Зачем они нужны? Как ими пользоваться?
* Будут ли "пойманы" в `catch` блоке ошибки, возникающие при рендере `InnerComponent`? Почему?
  ```javascript
  function OuterComponent() {
    try {
      return <InnerComponent />;
    } catch (error) {
      handleError(error);
    }
  }
  ```

### Reconciliation

* Что такое? Какую функцию выполняет?
* Каким образом reconciliation алгоритм использует тип элемента (что происходит, если тип изменился, не изменился и т.д.)?

### Атрибут `key`

* Зачем нужен?
* Почему лучше не использовать индекс элемента массива в качестве значения? Когда этим правилом можно пренебречь?
* Должно ли значение атрибута `key` быть уникальными для всего отрисованного дерева (по аналогии с html-атрибутом `id`)?
* Имеется список из нескольких элементов:
```javascript
<ul>
  {list.map((text, i) => (<li key={i}>{text} <input /> </li>))}
</ul>
```

Предположим, что в каждом инпуте содержится какой-то текст. Если добавить в начало `list` еще один элемент, то какой из инпутов окажется пустым и почему?

### Synthetic Events

* Что такое и зачем нужны?
* Пусть на какое-то событие на `<input />` назначено 2 обработчика: один через атрибут `on...`, а другой через `addEventListener`.
	* В чем разница между добавлением обработчиков первым и вторым способом?
	* В каком порядке могут выполняться обработчики? От чего это зависит?
	* Может ли один из обработчиков отменить выполнение второго обработчика?
	* Какие проблемы могут возникнуть из-за использования обработчика, навешанного через `addEventListener`?
### Higher-Order Components

* Может ли HOC оборачивать несколько компонент разом?
* Зачем делать функцию, которая возвращает функцию высшего порядка, создающую HOC? Как это помогает сделать HOC композабельным?
* Какие проблемы могут возникать, если HOC не будет прокидывать входящие props дальше в потомка?
* Как обрабатывать `displayName` при создании HOC?
* Как HOC влияет на forwarded ref?
* В чем преимущество использование HOC для получения значения из контекста перед useContext и наоборот?
	* with useContext:
      ```typescript
      type Props = {
          prop1: any;
      }

      const MyComp: FC<Props> = ({ prop1 }) => {
          const { prop2,  prop3 } = useContext(context);
          ...
      } 

      // usage
      <MyComp prop1="asd" />
      ```


	* with HOC:
      ```typescript
      type Props = {
          prop1: any;
          prop2: any;
          prop3: any;
      }

      const MyComp: FC<Props> = ({ prop1, prop2, prop3 }) => {...}

      // селектор тут скорее концепция, в данном случае селектор частично удовлетворяет интерфейс компонента
      const selector1 = () => {...} // прокидывает в компоненту prop2 и prop3
      const MyCompWithStore1 = withSomething(selector1)(MyComp);
      const selector2 = () => {...} // прокидывает в компоненту prop1 и prop3
      const MyCompWithStore2 = withSomething(selector2)(MyComp);

      <MyCompWithStore1 prop1="asd" />
      <MyCompWithStore2 prop2="asd" />
      ```

### Ресурсы

* [React Documentation](https://reactjs.org/docs/getting-started.html)
* [React as a UI Runtime](https://overreacted.io/react-as-a-ui-runtime/)
* [Index as a key is an anti-pattern](https://medium.com/@robinpokorny/index-as-a-key-is-an-anti-pattern-e0349aece318)
* [React Fiber Architecture](https://github.com/acdlite/react-fiber-architecture) - здесь неплохо написано про reconciliation в целом, часть про детали реализации (fiber) опциональна.
* [React events in depth w/ Kent C. Dodds, Ben Alpert, & Dan Abramov](https://www.youtube.com/watch?v=dRo_egw7tBc)
* [Getting to know React DOM’s event handling system inside out](https://medium.com/the-guild/getting-to-know-react-doms-event-handling-system-inside-out-378c44d2a5d0)
* [Полное руководство по useEffect](https://habr.com/ru/company/ruvds/blog/445276/) - объёмная, но очень классная статья по useEffect, которая поможет раскрыть глаза на многие вещи. Возможно придётся осилить в 2 подхода.
* [Все ли вы знаете о useCallback](https://habr.com/ru/post/529950/)
* [Интересная ветка обсуждения в комментариях статьи выше](https://habr.com/ru/post/529950/comments/#comment_22380330)
* [Passing Data Deeply with Context](https://beta.reactjs.org/learn/passing-data-deeply-with-context)
- [React as a UI Runtime](https://overreacted.io/react-as-a-ui-runtime/)
- [Index as a key is an anti-pattern](https://medium.com/@robinpokorny/index-as-a-key-is-an-anti-pattern-e0349aece318)
- [React Fiber Architecture](https://github.com/acdlite/react-fiber-architecture) - здесь неплохо написано про reconciliation в целом, часть про детали реализации (fiber) опциональна.
- [React events in depth w/ Kent C. Dodds, Ben Alpert, & Dan Abramov](https://www.youtube.com/watch?v=dRo_egw7tBc)
- [Getting to know React DOM's event handling system inside out](https://medium.com/the-guild/getting-to-know-react-doms-event-handling-system-inside-out-378c44d2a5d0)
- [Новый контекст React в деталях](https://blog.csssr.ru/2018/04/06/new-react-context)