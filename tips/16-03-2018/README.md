PHP 5 is very very flexible in accessing member variables and member functions. 
These access methods maybe look unusual and unnecessary at first glance; but they are very useful sometimes; s
pecially when you work with SimpleXML classes and objects. I have posted a similar comment in SimpleXML function reference section, 
but this one is more comprehensive. 

Недавно на одном из проектов было большое количество задач связанных с датами.
Про некоторые из них я напишу ниже.

И так.

Объекты в PHP передаются по ссылке, из - за этого такой код, будет менять родительскую переменную.

$currentDate = new DateTime();

$nextWeekDate = $currentDate->modify('+1 week');

Что бы такого не произошло, стоит использовать оператор clone

$currentDate = new DateTime();

$nextWeekDate = clone $currentDate;
$nextWeekDate = $nextWeekDate->modify('+1 week');

1)в часах и минутах
2) TimeZone issye

3) DateInterval интервалы неправиьные
4)DateTimeImmutable
5) добавление формата в конструктор
