# Сделано на основе Shower

<img src="pictures/logo.png" width="250" alt="Shower logo">

[See it in action](http://shwr.me/). Includes [Ribbon](https://github.com/shower/ribbon/) and [Material](https://github.com/shower/material/) themes, and [core](https://github.com/shower/core/) with plugins.

Follow [@shower_me](https://twitter.com/shower_me) for support and updates, [file an issue](https://github.com/shower/shower/issues/new) if you have any.

## Quick Start
1. [Fork](https://github.com/shower/shower/fork) this repository
2. Open `index.html` and start creating your presentation

#Описание.
4) Кастомные свойства. Аналог препроцессорных переменных.  Они помогают уменьшить повторяемость кода.
	Б) На больших сайтах бывает нужно сменить какой-то постоянно повторяющийся цвет, и автозаменой это делать не безопасно. Или нужно сменить цветовую схему
	Похожая ситуация с фреймворками. Чтобы их можно было удобно настраивать нужны переменные.
	
	В) Препроцессорные переменные имеют очень серьёзный недостаток: они статичны и не могут меняться на лету. Нативные Переменные позволяют менять темы на лету.
	Переменные позовляют добавить денамику в дикларативный цсс.
	
	Г) Использование переменных дает нам симантическую информацию.  Смысл --main-text-color  более понять чем #00ff00.


5) Доступны в новых браузерах, к сожалению не имеют возможности иметь обратную совестимость.
На мой взгляд, можно эксперементировать во внутренних инструментах или в личных проектах)

6) Синтаксис кастомных переменных.
	Для объявление кастомных свойств используется синтаксис с 2-мя минусами.
	Для использования приминяется функция var(). В которую в качестве аргумента передается переменная.
	Вторым аргументом можно передать дефолтное значение

7) JavaScript. Чтобы получить значение кастомного свойства, используйте метод getPropertyValue() объекта CSSStyleDeclaration.
Аналогично, чтобы динамически менять значение кастомного свойства, используйте метод setProperty() объекта CSSStyleDeclaration.

8) Первые впечатления. Эдди Османи в деакбре прошлого года обуликовал в твитере, что хром реализовал, кастостомные переменные.
И что он получил в ответ. Было много неодобрительных коммпентариев. Суть которых?

9) Синтакис такой, а не $foo
  А) Чтобы не было проблем с препроцессорами
  Б) Более подробно об этом можно прочесть в статье одного из авторов спецификации, Таба Аткинса (Tab Atkins).

10) Препроцессорные переменные не наследуются. Препроцессорные переменные сложно совмещать с другим код. 
Например если подтягиваешь еще другую либу по CDN

11) Примеры. И фишки использования
	А) Демо 1
	Б) https://googlechrome.github.io/samples/css-custom-properties/index.html
	Взгляните на пример, чтобы получить представление о разных интересных техниках, которые станут доступным благодаря кастомным свойствам

12) @​apply
@apply Аналог миксинов.
Реализовано в хроме. Таб Анткинсон.
- Позовляет вставлять набор свойств.
- Для использования применяется функция apply();

13) Выводы
- Css стримится вопладить фишки препроцессоров, и в будущем мы будем снова писать на чистом цсс
- Для вечно зеленых браузеров для решения нетревиальных задач есть интересный инструмент.
