## Методы для работы со строками
`.length`                 вернет длину строки с учетом пробелов

`slice(start , end)`      извлекает часть строки и ВОЗВРАЩАЕТ НОВУЮ СТРОКУ. От start До end

`.toLowerCase() `         приведет строку к нижнему регистру

`.toUpperCase() `         приведет строку к верхнему регистру

`.includes('*')`          ищет указанное значение в скобках в строке, возвращает true/false

`.indexOf('*') `          вернет ИНДЕКС символа с которого он НАЧИНАЕТСЯ , если таковых несколько то вернет только ПЕРВОГО найденого

` charAt(позиция)`        Чтобы получить символ, используйте вызов charAt(позиция). Первый символ имеет позицию 0


## Методы для работы с массивами

`Array.isArray()` отвечает на вопрос "Это массив?" и ВОЗВРАЩАЕТ true или false

`Array.from()`   СОЗДАСТ новый массив из массивоподобного объекта arguments или строки, то что имеет свойство length

`.push();`               добавить елем в КОНЕЦ массива 

`.pop(); `               удалить ПОСЛЕДНИЙ елем массива и вернутть его

`.unshift();`             добавить елем в НАЧАЛО массива 

`.shift(); `              удалить ПЕРВЫЙ елем массива и вернутть его

`.splice(pos,0,new,new)`  вставляет новый елементы . position указывает начальную позицию в массиве, в которой будут вставлены новые элементы. 
- Второй аргумент равен нулю 0, он говорит методу не удалять какие-либо элементы.
- Третий, четвертый и все последующие аргументы - это новые элементы, которые вставляются в массив.                       

`.splice(pos, num)`       удаляет елементы массива. Аргумент position указывает позицию (индекс) 
- первого элемента для удаления, а аргумент num определяет количество удаляемых элемента.
- Метод splice изменяет исходный массив и ВОЗВРАЩАЕТ массив, содержащий удаленные элементы.

`.slice(1 , 4)`  метод slice(begin, end) копирует участок массива от begin до end, не  включая end. Исходный массив при этом не меняется.
 - Если не указать end – копирование будет до конца массива
 - Можно использовать отрицательные индексы, они отсчитываются с конца
 - Если вообще не указать аргументов – скопируется весь массив

`.join("разделитель")`  записывает массив в строку, можно с разделителем

`.split("разделитель")` позволяет превратить строку в массив, разбив ее по разделителю.  

`.concat(имя массива)`  склеивает массив с другим, можно несколько, указываем через запятую

`.indexOf(елемент)`     вернет ИНДЕКС ЕЛЕМЕНТА

`.includes()`    определяет, содержит ли массив некоторый элемент, возвращает true или false   

`.reverse()`  меняет порядок элементов в массиве на противоположный, при этом изменяя исходный массив.

`forEach(callback(x,y,z))`  перебирает массив подобно циклу for. Метод forEach НИЧЕГО НЕ ВОЗВРАЩАЕТ, его используют только для перебора, как более «элегантный» вариант, чем обычный цикл for. Параметры: X - елемент массива, Y - индекс массива, Z - сам массив

`.every(callback(x,y,z))`    АНАЛОГ && проверяет, удовлетворяют ли ВСЕ элементы массива условию, заданному в передаваемой функции. Перебирает елементы пока не встретит, тот, который НЕ удовлетворяет условиям. Как только найдет такой вернет FALSE, если все елементы удовлетворяют условию вернет TRUE. Параметры: X - елемент массива, Y - индекс массива, Z - сам массив 

`.some(callback(x,y,z))` АНАЛОГ || проверяет есть ли в массиве елемент, который удовлетворяет условию. Если такой есть вернет TRUE, если нет то FALSE. Отличается от .every() тем, что перебирает ВСЕ елементы и дает ответ исходя из наличия или отсутствия данного елемента. А в .every() нужно чтобы ВСЕ улементы должны удовлетворять условию.  Параметры: X - елемент массива, Y - индекс массива, Z - сам массив

`.map(callback(x,y,z))`  проходится по каждому элементу (x) в массиве и производит с ним нужные действия ВОЗВРАЩАЕТ НОВЫЙ МАССИВ, основываясь на существующем массиве. Параметры: X - елемент массива, Y - индекс массива, Z - сам массив

`.filter(callbac(x,y,z))`  используется для фильтрации массива через функцию. Проверяет каждый елемент массива, и если он удовлетворяет НАШЕМУ условию, записывает его в НОВЫЙ МАССИВ. Параметры: X - елемент массива, Y - индекс массива, Z - сам массив

`.reduce(x,y,z,f)`  используется для вычисления на основе массива какого-либо единого значения, иначе говорят «для свёртки массива».(+-*/). Получения суммы елементов массива или других математических действий.
Аргументы функции callback(previousValue, currentItem, index, arr)
- previousValue – последний результат вызова функции, он же «промежуточный результат».
- currentItem – текущий элемент массива, элементы перебираются по очереди слева-направо.
- index – номер текущего элемента.
- arr – обрабатываемый массив.
При первом вызове previousValue = [0] индексу массива, currentItem = [1] индексу массива. Производим с ними нужные нам действия (+-*/). На второй итерации previousValue будет равно ПРЕДЫДУЩЕМУ результату а currentItem будет равен следующему елементу массива. 

`.find(callback(x,y,z))`  будет искать до первого совпадения, после чего прервет свое выполнение
ВОЗВРАЩАЕТ TRUE если находит указанный елемент, или UNDEFIND усли не найдет

`sort()` на месте сортирует элементы массива и ВОЗВРАЩАЕТ ОТСОРТИРОВАННЫЙ МАССИВ. в качестве параметра можно передать функцию с кастомным порядком сортировки (https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/sort) 

## Методы и команды для объектов 

`Object.values()` имя объекта. ВОЗВРАЩАЕТ МАССИВ ЗНАЧЕНИЙ КЛЮЧЕЙ объекта

`Object.keys()`  имя объекта. ВОЗВРАЩАЕТ МАССИВ, содержащий все КЛЮЧИ объекта

`Object.entries()` имя объекта. ВОЗВРАЩАЕТ МАССИВ МАССИВОВ с ключами и значениями свойств объекта.

`"ключ" in объект` проверяет есть ли указанный ключ в объекте ВОЗВРАЩАЕТ TRUE/FALSE

`.hasOwnProperty("ключ")` проверяет есть ли указанный ключ в объекте ВОЗВРАЩАЕТ TRUE/FALSE

`Object.freeze()`  замораживает объект: это значит, что он предотвращает добавление новых свойств к объекту, удаление старых свойств из объекта и изменение существующих свойств

` delete объект.свойство ` удалит указанное свойство

## Циклы 
`for(let i of array)`    цикл FOR OF перебирает ЕЛЕМЕНТЫ МАССИВА. в переменной i будут НЕ ИНДЕСЫ массива а ЕЛЕМЕНТЫ  

`for(let key in объект)` Цикл FOR IN перебирает каждый КЛЮЧ объекта


## Математические

`Math.abs()`      аргументом передаем число . ВОЗВРАЩАЕТ абсолютное значение числа. можно использ. для преобразование отрицательного числа в положительное

`Math.random()`   генерирует число от 0 до 1 . Если нужен диапазон, то умножаем на этот диапазон

`Math.round()`    округляет то что передали в скобках с учтом бОльшей или мЕньшей доли (1.3=1 или 1.8=2)

`Math.ceil()`   округляет до целого цисла только в БОЛЬШУЮ строну (1.3=2 или 1.8=2)

`Math.floor()`  округляет до целого цисла только в МЕНЬШУЮ строну (1.3=1 или 1.8=1)

`.toFixed(n) `  округляет число до n знаков после запятой, при необходимости добивает нулями до данной длины и возвращает в виде строки

`Math.pow(2,3)`    возведет ПЕРВОЕ значение в степень ВТОРОГО значения EX: 2в3 степени 

`Number.parseInt(Math.random()*10)` - отбросить все что после запятой и вернет целое число

`Math.max(a, b, c)`	ВОЗВРАЩАЕТ НАИБОЛЬШЕЕ из чисел, перечисленных через запятую в круглых скобках (наибольший аргумент)

`Math.min(a, b, c)`	ВОЗВРАЩАЕТ НАИМЕНЬШЕЕ из чисел, перечисленных через запятую в круглых скобках (наименьший аргумент)


## Проверки

`Number.isInteger()`     проверяет аргумент,  ЦЕЛОЕ ли число. Возвращает TRUE/FALSE

`typeof`                 возвращает тип значения переменной

`isNaN()`                определяет является переменная NAN НЕчисловым значением. ВОЗВРАЩАЕТ TRUE/FALSE  
##### Перед сравнением ПРИВОДИТ подаваемое ему на вход значение через Number(value)

`Number.isNaN`  проверяет, является ли указанное значение NaN или нет ВОЗВРАЩАЕТ TRUE/FALSE 
##### Number.isNaN НЕ ПРИВОДИТ перед сравнением подаваемое ему на вход значение через Number(value)

`isFinite `  ВОЗВРАЩАЕТ TRUE/FALSE , совпадает ли указанное значение со всем кроме: Infinity, -Infinity и NaN.
##### Перед сравнением ПРИВОДИТ подаваемое ему на вход значение через Number(value)

`Number.isFinite`  ВОЗВРАЩАЕТ TRUE/FALSE , совпадает ли указанное значение со всем кроме: Infinity, -Infinity и NaN.
##### Number.isFinite во всех отношениях безопаснее, поскольку не занимается лишними приведениями. А чтобы значение приводилось к его числовому представлению, всегда есть Number.isFinite(Number(value)).

 


## Преобразования

`String()`    преобразовывает к СТРОКЕ

`Number()`               преобразовыввает к ЧИСЛУ то что в скобках, если не может преобразовать то ВОЗВРАЩАЕТ NAN

`Number.parseInt()`      парсит данные СЛЕВА НАПРАВО до ПЕРВОЙ буквы (или символа) и приводит к 
##### ЦЕЛОМУ числу

`Number.parseFloat()`    парсит данные СЛЕВА НАПРАВО до ПЕРВОЙ буквы (или символа) и приводит к 
##### ДРОБНОМУ числу


## Стрелочные функции
- объявляются и назначаются ТОЛЬКО переменным FunctionExpression
- если параметр 1, то можно передавать без скобок
- если в блоке кода одна команда, то можно писать без фигурных скобок
- если параметров нет, то обязательно должны быть пустые круглые скобки
- нет локальной переменной arguments содержащей все аргументы
- если необходимо собрать все аргументы в коллекцию используйте опертор rest.
- this в использовании внутри тела функции ВСЕГДА будет обращаться к глобальному контексту (ducument)

