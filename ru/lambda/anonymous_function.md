# Анонимные функции

Supporting anonymous function means we treate function as first class citizen. So you can pass a function as a parameter, or returned as a value. JavaScript is actually a functional programming language. It supports first class function and allow us to define an anonymous function easily.
Поддержка анонимных функций означает что функция рассматривается как функция первого класса. Это значит передача функции как параметра или возвращение ее как значение. JavaScript на самом деле функциональный язык. Он поддерживает функции первого класса и может легко объявлять их как анонимные функции.

![](http://southparkstudios.mtvnimages.com/shared/characters/kids/mysterion.jpg)

### Define Anonymous Function
### Определение анонимной функции

```js
function(x){
    return x*x;
}// => SyntaxError: function statement requires a name
```

Why we got a SyntaxError here? Because we need a function expression to create an anonymous function.
Почему мы получили синтаксическую ошибку здесь? Потому что нам нужно получить функцию выражение для создания анонимной функции

Expression should returns a value:
Выражение должно вернуть значение:

``` js
var a = new Array()  // new Array() is an expression, and the whole line is called a statement. (new Array() это выражение, и эта строка называется объявлением)
```

But why the error says: `function statement requires a name`. In JavaScript, there is another way to declare a function, that is using function statement. A statement requires a name. The code above is treated as function statement, because there is nothing to return. Therefore, we got the error.
Но почему в тексте ошибки говорится: `функция объявление требует имя`. В JavaScript, есть другой путь декларирования функции, который используется как функция объявление. Объявление требует имени для функции. Код выше рассматривался как функция объявление, потому что здесь ничего не возвращается. Поэтому мы получаем ошибку.

If we assign `function (x){return x*x}` to a variable, or pass it as a parameter, we will not get any SyntaxError, because `function (x){return x*x}` is only a expression under this circumstance. For instance:
Если мы применяем `function (x){return x*x}` к переменной или передадим его как параметр, то не получаем никакую синтаксическую ошибку, потому что `function (x){return x*x}` это всего-лишь выражение при этом обстоятельстве. К примеру:

```js
var squareA = function(x){
    return x*x;
}
```

However, a tricky thing is that `squareA` becomes a named function.
Однако, есть сложная вещь в том что `squareA` становится именованной функцией.

```
console.log(squareA)  // => function squareA()
```

Even `squareA` becomes a named function, but the definition process is different from code below:
Несмотря на то, что  `squareA` становится именованной функцией, всё же процесс определения отличный от кода ниже:

```js
function squareB(x){
    return x*x;
} // => undefined
```

`squareB` directly defines a function using function statement that obviously has no return. While, `squreA` defines an anonymous function using function expression, and assigns the function returned from function expression to a variable named `squareA`. So, a expression returns a value:
`squareB` непосредственно определяет использование функции определения которое очевидно не возвращается. Пока `squareA` определена анонимной функцией использующей функцию выражение, и назначает функцию возвращенной из функции выражения в переменную именем `squareA`. Итак выражение возвращает значение; 

```
console.log(function(x){ return x*x});
// => undefined
// => function ()
```

The `undefined` is the return value for `console.log()`, and `function()` is the return value from function expression that defines an anonymous function.
Значение `undefined` это возврат значения из вызова функции `console.log()` и `function()` возвращает значение из функции выражения которая определена как анонимная функция

Although squareA looks like a named function, but while you construct an Object from it, that will be a bit funny:
Хотя `squareA` похожа на именованную функцию, но пока она конструируется от объекта, это будет немного забавно:
```js
new squareA().constructor.name // => ""
new squareB().constructor.name // => "squareB"
```

### Использование анонимной функции

Function is first class, that means we can assign a function to a variable:
Функция является функцией первого класса тогда, когда она может быть назначена как значение переменной:

```js
var square = function(x) {return x*x}
```

We can pass the anonymous function as a parameter as well. just like we passed an anonymous function to `console.log`:
Тык же мы можем передать анонимную функцию как параметр. Так как мы сделали это, передав анонимную функцию в `console.log`:

```js
 console.log(function(x){return x*x})
```

And, we can return a function just like return a value:
И мы можем вернуть функцию так же, как и значение:

```js
function multiply(x){
    return function(y){
        return x*y;
    }
}

multiply(1)(2) // => 2
```
