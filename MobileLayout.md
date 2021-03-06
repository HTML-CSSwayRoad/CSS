# MobileLayout   

https://docs.google.com/presentation/d/1WSq6UpSpGbhnZHx7qZ-USmsZfj46aK27s1vRrdaFVo8/edit#slide=id.g631b0001c8_0_59  
https://dinarys.com/ru/blog/difference-between-responsive-and-adaptive-web-design  
https://html5book.ru/otzyvchivyj-dizayn-saita/  
https://likeit.pro/blog/aktualnye-tipy-vyerstki/  
https://flagstudio.ru/blog/4-stepeni-adaptivnosti-html-verstki#:~:text=%D0%A0%D0%B5%D1%81%D0%BF%D0%BE%D0%BD%D1%81%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20(%D0%BE%D1%82%D0%B7%D1%8B%D0%B2%D1%87%D0%B8%D0%B2%D0%B0%D1%8F)%20%D0%B2%D0%B5%D1%80%D1%81%D1%82%D0%BA%D0%B0,%D0%B0%D0%B4%D0%B0%D0%BF%D1%82%D0%B0%D1%86%D0%B8%D0%B8%20%D1%81%D0%B0%D0%B9%D1%82%D0%B0%20%D0%BF%D0%BE%D0%B4%20%D1%88%D0%B8%D1%80%D0%B8%D0%BD%D1%83%20%D1%83%D1%81%D1%82%D1%80%D0%BE%D0%B9%D1%81%D1%82%D0%B2%D0%B0.

https://gb.ru/posts/how_to_work_frontend

**Медиа-запросы (media queries) – это правила CSS, которые позволяют управлять стилями элементов в зависимости от значений технических параметров устройств.**

https://dev.to/theodorusclarence/back-to-basic-should-we-use-rem-em-or-pixel-1hd0

**em** - относительная величина, единица которой будет равна высоте шрифта блока родителя. Те, если у блока родителя   
font-size: 16px, то задав дочернему блоку width: 6.25em мы получим 100px. 

**rem** - очень похож на em, за исключением того, что единица будет равна не высоте шрифта родителя,  
а высоте шрифта элемента <html>, которая по-умолчанию всегда 16px.
  
**vw и vh** - отношение к ширине и высоте видимой части браузера, используется как %, но без привязки к родительским элементам.
  
**@media** - это обычный объект, внутри которого находится перечень элементов и их свойств.  
Описанные там свойства применяются к странице только тогда, когда наше устройство и его характеристики отвечают условиям этого @media.

Все свойства внутри блока @media не имеют повышенных приоритетов. Поэтому медиа-запросы желательно описывать внизу *.css файла
  
Кроме того, эти условия можно расширять, более конкретизируя необходимый девайс. Для этого существуют логические операторы:
  
and - связывает условия между собой: @media (min-width: 360px) and (max-width: 640px) { ... } Все устройства, с шириной экрана от 360px до 640px.  
  
оператор запятая - перечисление, (эквивалент оператору или) свойства применяются, если хотя бы одно из условий выполняется:  
@media (orientation: portrait), (max-width: 640px) { ... } Все устройства портретной ориентации с шириной экрана ниже 640px.
  
  
not - отрицание: @media not screen and (max-width: 640px) { ... }  
  Все устройства, кроме настольных пк, и с шириной экрана менее 640px.
  
 
only - заблокировать медиа-запрос от старых браузеров, которые не поддерживают CSS3:
 @media only screen { ... }
Сработает для всех пк, браузер которых знает CSS3.
```
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
```
  
У каждого типа девайса есть разбежка разрешений. Так называемые чекпоинты.   
  
Принято выделять следующие:

Мобильный телефон от 320px до 768px;  
Планшет от 768px до 1024px;  
Ноутбук от 1024px до 1366px;  
Настольный компьютер от 1366px.  
Обычно для респонсив верстки в работе используются ограничения по ширине (min-width) или (max-width), остальные гораздо реже.
