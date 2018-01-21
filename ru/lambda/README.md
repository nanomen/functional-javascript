# Lambda

Why we need to talk about lambda, aka. λ, at the very beginning?
Почему в самом начале книги мы говорим о Лямбде (символ записывается так - λ)?

![](http://images.wikia.com/half-life/en/images/archive/3/3a/20120621181904!Lambda_reactor_complex_logo.png)

Look at the definition: Lambda contains a transforming rule (substitution from a variable) and a syntax for declaring function. The generic usage of Lambda calculation is that any calculating function can be represented and calculated by lambda. Therefore, it is equivalent to the Turing machine

Посмотрим на определение: Лямбда содержит правило преобразования (подстановка (замещение) из переменной) и синтаксис для декларирования функции. Основное использование Лямбда вычислений это вычисление функции которое может быть представлено вычислением лямбдой. Следовательно это равнозначно машине Тьюринга

Lambda is a mapping relationship between `x` to `y`. It is equivalent to the anonymous function in most of Functional Programming Languages. The reason of being named as lambda expression is that these functions are always used once or few times, which do not need function name.

Лямбда отображает отношения между `x` и `y`. Это сравнимо с анонимной функцией в функциональных языках программирования. Причина того, почему так назвали лямбда выражения в том, что эти функции всегда используются один или несколько раз и не нуждаются в именовании.

![](http://m.memegen.com/eo6ojw.jpg)
![](http://m.memegen.com/1qleyk.jpg)

Anonymous function can be passed into another function as a parameter, or returned as a closure.
Анонимная функция может быть передана в другую функцию как параметр или возвращена как замыкание.

However, an anonymous function is not necessarily a lambda calculus, because an anonymous function may accept multiple parameters, while, the lambda calculus accepts only one parameter, like:
Однако анонимная функция не всегда может быть лямбда вычислением, потому что анонимная функция может принимать в себя несколько параметров, пока, лямбда вычисление принимает в себя только один параметр, например:

```
multiple(x, y) = x*y

```
Simplify to a mapping expression, removing the function name:
Простое выражение преобразования, имя функции удаляется:

```
(x,y) -> x*y
```

Is this a lambda? Negative. Lambda is not just a simple mapping relationship without function name, but also a mapping from only single parameter.
Это лямбда? Нет. Лямбда это не только обыкновенное преобразование аргументов без именования функции, но так же преобразование только с одним параметром.

Precisely speaking, let's look at into the mapping process above:
Говорю вам точно, давайте посмотрим в процессы преобразования ниже:

1. We create a lambda accepting only one parameter:
1. Мы создаем лямбда прием только с одним параметром:

    ```
    (x) -> (y -> x*y)       // лямбда A
    ```

1. lambda A gives (returns) us another lambda which also accepts one parameter:
1. Лямбда возвращает нам другую лямбду которая также принимает один параметр:

    ```
    (y -> x*y)
    // lambda B, which is returned from inside of lambda A
    // лямбда B, которая возвращена изнутри лямбды А
    ```

1. For example, we pass number 5 into lambda A:
1. Например, мы передаем число 5 в лямбду А:

    ```
    (5) -> (y -> 5*y)
    ```

1. Then we get another lambda B1, with number 5 in it:
1. Потом мы получаем другую лямбду В1 с числом 5 внутри:

    ```
    (y -> 5*y)              // лямбда B1
    ```

1. This lambda `y -> 5*y` is a mapping from `y` to `5*y`, if we pass number 4 into lambda B1, we get:
1. Эта лямбда `y -> 5*y` преобразуется из `y` в `5*y`, если мы передаем число 4 в лямбду В1, мы получаем:

    ```
    4 -> 5*4
    ```

That is, the anonymous function `(x,y)->x*y` is the combination of two lambdas, instead of one lambda as it looks like.
То есть, анонимная функция `(x,y)->x*y` это комбинация двух лямбд, вместо одной из лямбд как мы тут видели

The way that a function accepting single parameter returns another function that accepts the second single parameter is called Curring. We will talk about Curring more in Chapter 02.
Путь когда функция принимает единственный параметр возвращающий другую функцию которая принимает второй единственный параметр и это называется каррирование. Мы будем говорить о каррировании во 2 главе.

Before we go deeper in Curring, let's look at how to use lambda in JavaScript at first.
Перед тем как углубиться в каррирование давайте сначала посмотрим как используется лмбда в JavaScript.
