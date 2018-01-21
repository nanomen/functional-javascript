# Functional JavaScript
[![Build Status](https://www.gitbook.io/button/status/book/jcouyang/functional-javascript)](https://www.gitbook.io/book/jcouyang/functional-javascript/activity)

This tiny book may only take you 2 hours to read, but it may take you to a journey of experiencing almost all the functional way of writing code in JavaScript. And It will cover some of the new feature come with ECMAScript 6 like arrow function, pattern matching etc. Further more, I will list the implementations of some fancy typeclasses from Haskell in JavaScript.

Эта малюсенькую книгу можно прочитать всего часа за два, но за это время вы пройдете весь путь по написанию функционального кода на JavaScript. В книге будут затронуты некоторые новшества из ECMAScript 6, такие как стрелочные функции (arrow function), сравнение с образцом (pattern matching) и т.п. В дальнейшем я буду добавлять JavaScript реализации классов из Haskell.

----

If you're kind of:

![](/images/i%20have%20no%20idea%20what%20im%20doing.jpg)

Plz read [Learn JavaScript](https://www.gitbook.io/book/gitbookio/javascript) first, but if you're just like:

![](/images/function%20inside%20function.jpg)

this book may help you functional stuff at some point.

Если ваши знания JavaScript можно проиллюстрировать картинкой ниже:

![](/images/i%20have%20no%20idea%20what%20im%20doing.jpg)

Пожалуйста, прочитайте вначале эту книгу [Learn JavaScript](https://www.gitbook.io/book/gitbookio/javascript), но если вы относите себя к такому персонажу:

![](/images/function%20inside%20function.jpg)

то эта книга поможет подннять ваш уровень функционального программирования

----

I chose [Eweda](https://rawgit.com/CrossEye/eweda/master/docs/eweda.html) as functional library for almost all examples.

Я выбрал функциональную библиотеку [Eweda](https://rawgit.com/CrossEye/eweda/master/docs/eweda.html) для иллюстрирования примеров этой книги.

> **Comment** Eweda is stick with more pure academic ideas but unpractical due to Javascript's poor handling of recursion. Here I just use it for example and show the functional idea, but if you want to use such api in production, please use [Ramda](https://rawgit.com/CrossEye/ramda/master/docs/ramda.html).

> Eweda придерживается чистых, академических идей функционального программирования и совершенно непрактична при применении рекурсии в JavaScript. Я использую ее только для иллюстрирования функциональных принципов и идей, но если вы хотите использовать подобное функционально API в продакшене, используйте [Ramda](https://rawgit.com/CrossEye/ramda/master/docs/ramda.html).

> **Comment** [Why not Underscore](http://fr.umio.us/why-ramda/) Short story: no auto curry. Long story: checkout chapter 2.

> [Почему не Underscore](http://fr.umio.us/why-ramda/) Коротко: нет автоматического каррирования. Подлиннее: читайте главу 2.

----

> **Note** In case I will write some code in ECMAScript 6 or (draft) standard, you better use firefox to run all those (who looks weird) examples. Simply tell what feature your browser has implement [here](http://kangax.github.io/compat-table/es6/)). Anyway, most long example will be followed by a jsbin.

> В некоторых примерах я буду писать код на ECMAScript 6 или использовать методы, не вошедшие в стандарт. Для корректного воспроизведения примеров используйте firefox (либо Chrome, на момент перевода многие методы уже поддерживаются многими браузерами). Вы можете проверить, что поддерживает ваш браузер [здесь](http://kangax.github.io/compat-table/es6/). Так же многие примеры будут вставлены через jsbin.

--------------
> Спасибо [@scott](https://github.com/scotv) за перевод на английский язык.  
> Спасибо [@nanomen](https://github.com/nanomen) за перевод на русский язык.
