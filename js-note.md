# Курс JavaScript 10 часов

JavaScript

[Курс JavaScript 10 часов](https://www.notion.so/JavaScript-10-7aa934a7d4bf433dbd6a3f710c59197a?pvs=21)

[https://www.youtube.com/watch?v=CxgOKJh4zWE](https://www.youtube.com/watch?v=CxgOKJh4zWE)

Среды выполнения JS: веб-браузер (Arc), node.js, IDE (в моем случае это PhpStorm, VS code)

## Самое важное в JavaScript

Выражения

Функции

Объекты

## Главная идея в JavaScript

Практически все сущности в JS, это объекты.

Объект — набор свойств.

Имя (оно же и ключ): Значение. 

Пример объекта:

```jsx
{
visible: true,
colorDepth: 24,
title: 'My Image',
orientation: {
	angle: 0,
	type: 'landscape'
},
pixelDepth: 24,
width: 1440
}
```

Массив, функция, *интеджер, *стринг — объекты.

*Интеджер и стринг ведут себя как объекты.

### console.log

```jsx
console.log('Hello World!')
```

console — объект, . — точечная запись, log — метод (он же функция), ( ) — вызов метода, ‘ ‘ — значение типа string.

с помощью точечной записи мы получаем доступ к методу объекта.

с помощью ( ) мы вызываем метод log.

кроме log, есть dir — отображает все свойства объекта.

так же есть метод table — отображает все свойства объекта в табличном виде.

Выражение

Возвращает

Значение

## Выражения. Примеры.

```jsx
'abc' 

10

5 + 2 

c = 10 

'Good ' + 'Evening'

a <= b || c !== d

myFunction(c, d) 
```

## Выражения. Результатом каждого выражения является значение.

```jsx
'abc' // 'abc'
10 // 10
5 + 2 // 7
'Good ' + 'Evening' // 'Good Evening'
a <= b || c !== d // true or false
myFunction(c, d) // результат функции
```

## Выражение присваивания.

```jsx
a = 20
```

## Выражения с побочными действиями. Не только возвращает значение, но и выполняет другие действия.

```jsx
a = 5

b++

myFunction(c, d)
```

## Переменные дают возможность повторного доступа к значениям.

## Имена переменных.

PascalCase — типы и классы.

DB_PASSWORD — значения известны до запуска приложения и не меняются.

camelCase — все остальные переменные, используется чаще всего.

Названия переменных должны быть понятными.

## Объявление переменных.

let

const

var (используется редко, не рекомендуется к использованию)

## В чем отличие между let и const.

```jsx
let a // объявление

const c = 10 // объявление и присваивание

a = true // присваивание
```

let

```jsx
let a = 10

a = 20

let b 

b = false
```

const

```jsx
const c = 10

c = 20
// TypeError: Assignment to constant variable.
```

## Объявление и присваивание.

```jsx
console.log(a) // ReferenceError: a is not defined

let a // объявление

console.log(a) // undefined

a = true // присваивание

console.log(a) // true
```

## Тип переменной определяется типом присвоенного значения.

```jsx
const a = 10 // 10 - (Number)

const b = 'abc' // - (String)
```

## Типы.

Примитивные типы и ссылочный тип.

Переменная имеет значение, значение имеет тип.

## Примитивные типы.

string, boolean, number, null, undefined, symbol.

## Ссылочный тип.

object

## Значения примитивных типов.

‘Hello world’

true

undefined

25

## Ссылочный тип.

Память.

0x3151 — 

{

a: 10,

b: true

}

0x7213 — [1, 2, 3]

Мы можем иметь разные ссылки (переменные), которые ссылаются на один и тот же объект в памяти.

Значение примитивных типов хранятся непосредственно в переменных. 

Если мы меняем значения в объекте, то эти же значения меняются у всех переменных, которые на него ссылаются. Значения в объекте можно менять сколько угодно раз. 

```jsx
const objectA = {
	a: 10,
	b: true
}
```

```jsx
const objectA = {
	a: 10,
	b: true
}

const copyofA = objectA
```

Тем самым мы создали две ссылки на один и тот же объект.

```jsx
const objectA = {
	a: 10,
	b: true
}

const copyofA = objectA

copyofA.a = 20

// objectA.a -> 20
```

Мы поменяли значение ‘a’ у объекта на ‘20’.

```jsx
const objectA = {
	a: 10,
	b: true
}

const copyofA = objectA

copyofA.c = 'abc'

// objectA.c -> 'abc'
```

Мы присвоили объекту новое свойство типа строки c = ‘abc’

## Динамическая типизация

Код не JS. Пример статической типизации: 

Код JS. Пример динамической типизации:

```jsx
String a = 'abc'

int b = 10

b = 'xyz' // Error
```

```jsx
a = 'abc' // String

a = 10 // Number

```

## Динамическая типизация в JS

```jsx
let a = 10

a = true

a = 'Bogdan'

a = undefined
```

Это не ошибки в JS.

```jsx
function a() {
	console.log('Hey there')
}

a() // 'Hey there'

a = 10

a() // Uncaught TypeError: a is not a function
```

Здесь уже ошибка, так как мы поменяли значение переменной ‘a’ на string, она перестала быть функцией.

Поэтому рекомендуется использовать везде, где это возможно, const. Ведь он позволяет предотвратить возможные проблемы, связанные с динамической типизацией.

## Const для объявления переменных

```jsx
const a = () => {
	console.log('Hey there')
}

a() // 'Hey there'

a = 10 // TypeError: Assignment to constant variable

a()
```

## Объекты — структура и синтаксис.

```jsx
const myCity = {
city: 'New York',
popular: true,
country: 'USA'
}

console.log(myCity.city)
// 'New York'

console.log(myCity.popular)
// true
```

Порядок свойств объектов не имеет значения.

## Удаление свойств у объекта.

```jsx
const myCity = {
city: 'New York',
country: 'USA'
}

delete myCity.country

console.log(myCity)

// {city: 'New York'}
```

```jsx
const myCity = {
	city: 'New York'
}

myCity['popular'] = true

console.log(myCity)
// {city: 'New York', popular: true}

const countryPropertyName = 'country'

myCity[countryPropertyName] = 'USA'

console.log(myCity)

// {city: New York, popular: true, country: USA}
```

## Вложение свойства.

```jsx
const myCity = {
city: 'New York',
info: {
	isPopular: true,
	country: 'USA'
	}
}

console.log(myCity.info.isPopular)
// true

delete myCity.info['isPopular']

console.log(myCity)
// {city: 'New York', info: {country: 'USA'}}
```

## Использование переменных

```jsx
const name = 'Bogdan'
const postsQty = 23

const userProfile = {
name: name,
postQty: postQty,
hasSignedAgreement: false
}
```

Сокращенный вариант

```jsx
const name = 'Bogdan'
const postsQty = 23

const userProfile = {
name,
postsQty,
hasSignedAgreement: false
}
```

Сокращенные свойства рекомендуется размещать в начале объекта.

## Глобальные объекты.

window — веб браузер

global — node.js

## Унифицированный глобальный объект.

globalThis — node.js, веб браузер.

## Методы.

Метод — свойство объекта, значение которого — функция.

Пример:

```jsx
const myCity = {
city: 'New York',
cityGreeting: function () {
	console.log ('Greetings!!')
	}
}

myCity.cityGreeting()
// 'Greetings!!'
```

Сокращенный вариант записи:

```jsx
const myCity = {
city: 'New York',
cityGreeting() {
	console.log ('Greetings!!')
	}
}

myCity.cityGreeting()
// 'Greetings!!'
```

Свойства объектов не содержат функции, а методы содержат.

Свойство:

```jsx
myCity.city
```

Метод:

```jsx
myCity.cityGreeting()
```

## JSON

JSON — JAVASCRIPT OBJECT NOTATION

```json
{
	"userId": 1,
	"id": 1,
	"title": "Test title",
	"status": {
		"completed": false
		}
{
```

## Передача данных в формате JSON

Из JSON в JS.

```json
{"userId": 1"id": 1"title": "Test title","status":{"completed": false}}
```

```jsx
JSON.parse()
```

```jsx
{
	userId: 1,
	id: 1,
	title: 'Test title',
	status: {
		completed: false
		}
{
```

Из JS в JSON.

```jsx
{
	userId: 1,
	id: 1,
	title: 'Test title',
	status: {
		completed: false
		}
{
```

```jsx
JSON.stringify()
```

```json
{"userId": 1"id": 1"title": "Test title","status":{"completed": false}}
```

## Мутация в JavaScript

Значения примитивных типов

```jsx
const a = 10

let b = a

b = 30

console.log(a) // 10

console.log(b) // 30
```

Значение ‘a’ не изменилось. 

## Значения ссылочного типа

```jsx
const person = {
name: 'Bob',
age: 21
}

person.age = 22
person.isAdult = true

console.log(person.age) // 22
console.log(person.isAdult) // true
```

Так выглядит мутация в JS.

Сама переменная const остается неизменной и хранит лишь ссылку на объект, когда само содержимое объекта меняется с помощью мутирования.

## Мутирование копий

```jsx
const person = {
name: 'Bob',
age: 25
}

const person2 = person

person2.age = 26
person2.isAdult = true

console.log(person.age) // 26
console.log(person.isAdult) // true
```

Мы создали копию объекта и мутировали его копию, значения объекта поменялись у переменной ‘person’ и ‘person2’, так как они ссылаются на один и тот же объект значения которого изменились с помощью мутации копии переменной ‘person2’.

Изменив копию, мы меняем и исходный объект.

## Как избежать мутаций

```jsx
const person = {
name: 'Bob',
age: 25
}

const person2 = Object.assign({}, person)

person2.age = 26

console.log(person2.age) // 26
console.log(person.age) // 25
```

Мы создали новый объект (скопировав его и начав ссылаться на новый объект, с теми же свойствами, что у исходного, но совсем другого объекта) с помощью Object.assign (функция)

Если у объекта есть вложенные объекты, то ссылки на них сохраняются. Мы можем избежать только мутаций корневых свойств таких как ‘name’, ‘age’.

## Второй вариант

```jsx
const person = {
name: 'Bob',
age: 25
}

const person2 = {...person } // Оператор разделения объекта на свойства

person2.name = 'Alice'

console.log(person2.name) // Alice
console.log(person.name) // Bob
```

Так же ссылки на вложенные объекты сохраняются. 

## Третий вариант

```jsx
const person = {
name: 'Bob',
age: 25
}

const person2 = JSON.parse(JSON.stringify(person))

person2.name = 'Alice'

console.log(person2.name) // Alice
console.log(person.name) // Bob
```

И только в таком случае ссылки на вложенные объекты не сохраняются. При таком методе создается полностью новый объект с помощью двойной конвертации из объекта в json и обратно.

## Функции.

Функция — блок кода, который можно выполнять многократно.

```jsx
let a = 5
let b = 3
let c

c = a + b 
console.log(c) // 8

a = 8
b = 12

c = a + b
console.log(c) // 20
```

Этот код можно оптимизировать убрав одинаковые блоки кода, заменив их на функцию.

Пример

```jsx
let a = 5
let b = 3

function sum (a, b) {
const c = a + b
console.log(c)
}

sum(a,b) // 8

a = 8
b = 12

sum(a, b) // 20
```

## Функция может быть..

…именованной

…присвоена переменной

…анонимной

…аргументом при вызове другой функции

                                   …значение свойства (метода) объекта

## Функция — это объект

```jsx
function myFn(a, b) {
let c
a = a + 1
c = a + b
return c
}
```

Используем console.dir(myFn), чтобы отобразились свойства объекта.

myFn — имя функции 

( ) — параметры функции

{ } — тело функции

return c — результат функции, ‘return’ возвращает значение ‘c’.

Функция возвращает undefined, если нет инструкции return.

```jsx
function myFn(a, b) {
let c
a = a + 1
c = a + b
return c
}

myFn(10, 3) // 14
```

Во время вызова функции то, что в круглых скобках, это аргументы. Параметрами они являются при объявлении функции. Аргументы меняются каждый раз при вызове одной и той же функции.

## Вызов функции

1. Параметрам ‘a’ и ‘b’ присваивается значения 10 и 3
2. Объявляется переменная ‘c’
3. Значение ‘a’ увеличивается на 1
4. Сумма значений ‘a’ и ‘b’ присваивается ‘c’
5. Возвращается значение ‘c’

Параметры, аргументы, return опциональны. Если return отсутствует, то функция возвращает undefined.

## Самая короткая функция

```jsx
function myFn() {}
myFn() // undefined
```

## Передача значения по ссылке

```jsx
const personOne = {
name: 'Bob',
age: 21
}

function increasePersonAge(person) {
person.age += 1
return person
}

increasePersonAge(personOne) // Передача объекта по ссылке
console.log(personOne.age) // 22
```

## Внутри функции не рекомендуется мутировать внешние объекты.

Создание копии объекта

```jsx
const personOne = {
name: 'Bob',
age: 21
}

function increasePersonAge(person) {
const updatedPerson = Object.assign({}, person)
updatedPerson.age += 1
return updatedPerson
}

const updatedPersonOne = increasePersonAge(personOne)
console.log(personOne.age) // 21
console.log(updatedPersonOne.age) // 22
```

Функции не должны работать с внешними переменными, а работать со своими внутренними.

## Колбэк функции

```jsx
function anotherFunction() {
//Действия..
}

function fnWithCallback(callbackFunction) {
callbackFunction()
}

fnWithCallback(anotherFunction)
```

Смысл колбэк функции что она вызывается внутри другой функции. Это называется колбэк функция.

Пример:

```jsx
function printMyName () {
console.log('Bogdan')
}

setTimeout(printMyName, 1000)
```

## Правила работы с функциями

1. Называть функции исходя из выполняемых задач
2. Одна функция должна выполнять одну задачу
3. Не рекомендуется изменять внешние относительно функции переменные

## Области видимости

Определяет границы действия переменной

Глобальная область видимости (window, global, globalThis…a, b, c)

Локальная область видимости 1 — переменные a, c

Локальная область видимости 2 — переменные— b

## Глобальные переменные и локальные переменные

Пример:

```jsx
// глобальные переменные
let a
let b

function myFn() {
let b // локальная переменная
a = true
b = 10
console.log(b) // 10
}

myFn()

console.log(a) // true
console.log(b) // undefined
```

То что внутри функции — локальная область видимости. Всё остальное — глобальная.

Названия переменных совпадают, это допускаются, но они разные.

## Цепочка областей видимости

```jsx
const a = 5
function myFn() {
function innerFn() {
console.log(a) // 5
}
innerFn()
}

myFn ()
```

## Жизненный цикл переменныых

```jsx
let a 
let b // 1. Объявление "b" в глобальной области видимости, ее значение undefined.
 
function myFn () {
let b // 3. Объявление "b" в зоне видимости функции
a = true
b = 10 // 4. Объявлена ли "b" в рамках функции? ДА, тогда присвоение этой переменной "b" значения 10 
console.log(b) // 10 , 5. "b" имеет значение 10 в области видимости функции
}

myFn () // 2. вызов myFn

console.log(a) // true
console.log(b) // undefined , 6. "b" всё так же имеет значение undefined в глобальной области видимости.
```

```jsx
let a // 1. Объявление "a" в глобальной области видимости, ее значение undefined.
let b 
 
function myFn () {
let b 
a = true // 3. Объявлена ли "a" в зоне видимости функции? НЕТ, объявлениа ли "a" во внешней области видимости? ДА, тогда присваиваем ей значение true в глобальной области видимости
b = 10 
console.log(a) // true 
}

myFn () // 2. вызов myFn

console.log(a) // true , 4. "a" имеет значение true
console.log(b) // undefined
```

Не следует менять свойства глобальных переменных с помощью функций в локальной области видимости.

## Типы областей видимости

Глобальная область видимости

Область видимости функции

Область видимости блока

Переменные, объявленные с помощью let или const внутри блока имеют область видимости, ограниченную этим блоком.

## Области видимости. Необъявленные переменные.

```jsx
function myFn() {
a = true
console.log(a) // true
}

myFn()

console.log(a) // true
```

Не рекомендуетчя так делать. Присваивать значения необъявленным переменным.

## Правила работы с переменными.

1. Все переменные объвлять перед их использованием.
2. Стараться использовать const везде, где это возможно.
3. Внутри функции не изменять переменные с внешних (глобальных) областей видимости.

## Строгий режим

```jsx
'use strict'
```

Запрещает использование необъявленных переменных.

Эта строка должна быть первой в глобальной области видимости или в области видимости функции.

## Операторы

Оператор — это встроенная функция в JS.

Операторы

Операнды

Унарные и бинарные

Инфиксная, префиксная и постфиксная записи

## Операторы

Арифмитические:

+

-

*

/

Сравнения: 

===

```jsx
!==
```

≤=

≥=

Логические:

!

&&

||

Присваивания:

=

## Текстовые операторы

typeof

instanceof

delete

new

## Примеры

```jsx
let a, b // запятая

a = 10 // присваивание
b = a // присваивание

let c = a + b // присваивание

console.log(c) // 20
```

a = 10 

a, 10 — операнды

Оператор — встроенная функция

“Внутреняя функция”

```jsx
function =(переменная, выражение) {
1. Получение результата выражения
2. Поиск переменной по имени
3. Присваивание результата выражения переменной
4. Возврат результата выражения
}
```

## Операнды

a = 10 (операнды или аргументы, так и так называются)

## Унарные операторы, у унарных операторов всегда один операнд (аргумент)

a++

+a  

delete obj.a

typeof a

new Object( )

## Бинарные операторы, у бинарных операторов два операнда (аргумента)

a = 5

a + b 

a += 5

a === b

a && b

## Инфиксная запись

a = true

a + b

a += 5

a || b

a > b

## Префиксная запись

++a

delete obj.a

typeof a

## Постфиксная запись

a++

myFunction( )

## Приоритетность операторов

a + b * c / d - e

a + ((b * c) / (d - e))

## Логические операторы

! (не) — всегда возвращает значения типа boolean

&& (и) , || (или) — возвращают значение одно из операндов.

## Ложные значения

```jsx
false
0
' '
undefined
null
```

boolean(value) → false

## Оператор ! чаще всего используется в условных инструкциях.

Используя двойной оператор ‘не’ ! — !!

Позволяет проверить ложность значения, потому двойное отрицание значений 0, ‘ ’, undefined даст всегда false.

## Операторы && и || являются операторами короткого замыкания.

Оператор &&

Выражения 1 && Выражение 2

Если “Выражение 1” ложно, то выражение 2 игнорируется, возвращается результат “выражения 1”

Оператор ||

Выражение 1 || Выражение 2

Если “Выражение 1” истинно:

“Выражение 2” игнорируется, возвращается результат “Выражения 1”

## Цепочка операторов && и ||

a && b && c && d

a || b || c || d

## Оператор разделения объекта на свойства — …

```jsx
const button = {
width: 200,
text: 'Buy'
}

const redButton = {
...button
color: 'red'
}

console.table(redButton)
```

Если у объекта “button” есть свойство “color”, его значение будет перезаписано.

Объединение объектов с помощью …

Пример

```jsx
const buttonInfo = {
text: 'Buy'
}

const buttonStyle = {
color: 'yellow',
width: 200,
height: 300
}

const button = {
...buttonInfo,
...buttonStyle
}

console.table(button)
```

Порядок записи в этом случае важен.

## Конкатенация строк, либо соединение строк

Пример

‘Hello ’ + ‘World’

Переменные в конкатенации строк

const hello = ‘Hello’

const world = ‘World’

const greeting = hello + ‘ ‘ + world

Шаблонные строки

const hello = ‘Hello’

const world = ‘World’

const greeting = `${hello} ${world}`

## Функциональные выражения

Объявленная функция vs Функциональное выражение

```jsx
function myFn(a, b) {
let c
a = a + 1
c = a + b
return c
}
```

```jsx
function(a, b) {
let c
a = a + 1
c = a + b
return c
}
```

У функционального выражения нет имени.

Функциональные выражения всегда анонимны.

## Присваивание функционального выражения переменной

```jsx
const myFunction = function(a, b) {
let c
a = a + 1
c = a + b
return c
}

myFunction(5, 3) // 9
```

Функциональное выражение в вызове другой функции

```jsx
setTimeout(function() {
console.log('Отложенное сообщение')
}, 1000)

// 'Отложенное сообщение' будет выведено в консоль через (1 сек)
```

## Стрелочные функции

```jsx
(a, b) => { // нет имени
let c
a = a + 1
c = a + b
return c
}
```

Стрелочные функции всегда анонимные. У функциональных выражения есть имя, а у стрелочных нет.

```jsx
const myFunction = (a, b) => {
let c
a = a + 1
c = a + b
return c
}

myFunction(5, 3) // 9
```

## Стрелочная функция в вызове другой функции

```jsx
setTimeout(() => {
console.log('Отложенное сообщение')
}, 1000)

// 'Отложенное сообщение' будет выведено в консоль через (1 сек)
```

## Сокращения в стрелочных функциях

Если тольк один параметр, то круглые собки можно опустить

a ⇒ {

// Тело функции

}

Второй вариант. Фигурные скобки можно опустить, если тело функции состоит из одного выражения.

(a, b) ⇒ a + b (в этом случае стрелочная функция неявно возвращает результат выражения)

## Значения параметров функции по умолчанию

```jsx
function multByFactor(value, multiplier = 1) {
return value * multiplier
}

multByFactor(10, 2) // 20
multByFactor (5) // 5
```

Второй пример

```jsx
const newPost = (post, addedAt = Date()) => ({
...post,
addedAt,
})

const firstPost = {
id: 1,
author: 'Bogdan',
}

newPost(firstPost)
```

Если мы хотим вернуть неявно объект, то его нужно обернуть в круглые скобки (тело функции), чтобы вернуть именно объект.

Значения по умолчанию вычисляются в момент вызова функции.

## Обработка ошибок

Что происходит в случае ошибок

```jsx
const fnWithError = () => {
throw new Error('Some error')
}

fnWithError()

console.log('Continue...')
```

## Try/Catch

```jsx
try {
// Выполнение блока кода
} catch (error) {
// Этот блок выполняется в случае возникновения ошибок в блоке try
}
```

Пример

```jsx
const fnWithError = () => {
throw new Error('Some error')
}

try {
fnWithError() {
} catch (error) {
console.error(error)
console.log(error.message)
}

console.log('Continue...')
```

## Инструкции

Выражение

Инструкция

Выражение - инструкция

~~Инструкция - выражение~~

Но инструкция не может стать выражением.

Выражение всегда возвращает значение. Инструкция выполняет определенные действия.

Пример

```jsx
let a;

const b = 5;

if (a>b) {
console.log('a is larger');
}

for (let i = 0; i++; i < 5) {
console.log(i);
}
```

## Инструкция обычно заканчивается точкой с запятой. Исключение: точка с запятой не требуется после блока инструкции.

## Выражение может быть инструкцией.

Примеры.

```jsx
'abc';

a = a + 3;

c = a + b;

d = 'Good ' + 'Evening';

myFunction(c, d);

console.log('Hey');
```

## Инструкция не может быть трансформирована в выражение.

Выражения могут быть использованы как аргументы в вызовах функции

Инструкция или выражение?

Примеры

```jsx
function myFn(a) {
console.log(a);
}

const b = true;
let c = 10;

myFn(2+3) // 5
myFn(b) // true
myFn(c = c + 1) // 11
myFn(c = c + 1;) // подобная запись неправильная
myFn(let d)
```

## Массивы

Массив — это объект c цифровыми именами свойств.

Формат записи массивов.

```jsx
const myArray = [1, 2, 3]
console.log(myArray)
// [1, 2, 3]

const myArray2 = new Array(1, 2, 3)
console.log(myArray2)
// [1, 2, 3] 
```

Структура массивов

```jsx
(3) [1, 2, 3]
0: 1
1: 2
2: 3
length: 3
__proto__: Array(0)
```

Массив vs Объект

```jsx
const myArray = [1, 2, 3]

console.log(myArray) // [1, 2, 3]
```

```jsx
const myObject = {
0: 1,
1: 2,
2: 3,
length: 3
}

console.log(myObject) // {0: 1, 1: 2, 2: 3, length: 3}
```

Отличается у них прототип.

## Чтение значений массива

```jsx
const myArray = [1, true, 'a']
console.log(myArray) // [1, true, 'a']

console.log(myArray[0]) // 1
console.log(myArray[1]) // true

console.log(myArray.length) // 3
```

## Длина массива

```jsx
const myArray = [1, 2, 3, 4]
console.log(myArray) // [1, 2, 3, 4]
console.log(myArray.length) // 4

myArray[2] = 'abc'

console.log(myArray) // [1, 2, 'abc', 4]

myArray[4] = true

console.log(myArray) // [1, 2, 'abc', 4, true]
console.log(myArray.length) // 5
```

## Методы массивов

push

pop

shift

unshift

forEach

map

Функции высшего порядка в массивах

## Push

```jsx
const myArray = [1, 2, 3]
console.log(myArray) // [1, 2, 3]

myArray.push(4)

console.log(myArray) // [1, 2, 3, 4]

myArray.push(true)

console.log(myArray) // [1, 2, 3, 4, true]
```

## Pop

```jsx
const myArray = [1, 2, 3]
console.log(myArray) // [1, 2, 3]

myArray.pop()

console.log(myArray) // [1, 2]

const removedElement = myArray.pop()

console.log(myArray) // [1]
console.log(removedElement) // 2
```

## Unshift

```jsx
const myArray = [1, 2, 3]
console.log(myArray) // [1, 2, 3]

myArray.unshift(true)

console.log(myArray) // [true, 1, 2, 3]

myArray.unshift('abc')

console.log(myArray)
// ['abc', true, 1, 2, 3]
```

## Shift

```jsx
const myArray = [1, 2, 3]
console.log(myArray) // [1, 2, 3]

myArray.shift()

console.log(myArray) // [2, 3]

const removedElement = myArray.shift()

console.log(myArray) // [3]
console.log(removedElement) // 2

```

## forEach

```jsx
const myArray = [1, 2, 3]
console.log(myArray) // [1, 2, 3]

myArray.forEach(el => console.log(el * 2))

console.log(myArray) // [1, 2, 3] , оригинальный массив не изменился
```

## Map

```jsx
const myArray = [1, 2, 3]
console.log(myArray) // [1, 2, 3]

const newArray = myArray.map(el => el * 3)

console.log(newArray) // [3, 6, 9]
console.log(myArray) // [1, 2, 3] , оригинальный массив не изменился
```

Map возвращает новый массив.

## Деструктуризация

Деструктуризация объектов

```jsx
const userProfile = {
name: 'Bogdan',
commentsQty: 23,
hasSignedAgreement: false,
}

const { name, commentsQty } = userProfile
const { hasSignedAgreement } = userProfile

console.log(name) // Bogdan
console.log(commentsQty) // 23
```

Объявление новых переменных и присваивание значений на основе значений свойств объекта.

## Деструктуризация массивов

```jsx
const fruits = ['Apple', 'Banana']

const [fruitOne, fruitTwo] = fruits

console.log(fruitOne) // Apple
console.log(fruitTwo) // Banana
```

Объявление новых переменных и присваивание значений на основе элементов массива

## Деструктуризация в функциях

```jsx
const userProfile = {
name: 'Bogdan',
commentsQty: 23, 
hasSignedAgreement: false,
}

const userInfo = ({ name, commentsQty }) => {
if (!commentsQty) {
return `User ${name} has no comments`
}
return `User ${name} has ${commentsQty} comments`
}

userInfo(userProfile) // User Bogdan has 23 comments

```

## Условные инструкции

if

switch

тернарный оператор

if … else

Инструкция if

```jsx
if (Условие) {
// Блок кода, выполняемый однократно, если Условие правдиво
}
```

Пример if

```jsx
let val = 10
if (val > 5) {
val += 20
}

console.log(val) // 30
```

Пример if с оператором отрицания

```jsx
const person = [
age: 20
}

if (!person.name) {
console.log('Имя не указано')
// Другие действия в случае, если свойства у "name" у объекта "person" нету
}
```

## Инструкция if else

```jsx
If (Условие) {
// Блок кода, выполняемый однократно, если Условие правдиво
} else {
// Блок кода, выполняемый однократно, если Условие ложно
}
```

Пример

```jsx
let val = 10

if (val < 5) {
val += 20
} else {
val -= 20
}

console.log(val) // -10
```

## Инструкция if else

```jsx
if (Условие) {
// Блок кода, выполняемый однократно, если Условие правдиво
} else if (Условие 2) {
// Блок кода, выполняемый однократно, если Условие ложно
} else { 
// Блок кода, выполняемый однократно, если предыдущие условия ложны
}
```

## Предпочтительный формат if

```jsx
if (Условие) {
// Блок кода, выполняемый однократно, если Условие 1 правдиво
} 
if (Условие 2) {
// Блок кода, выполняемый однократно, если Условие 2 правдиво
} 
if (Условие 3) { 
// Блок кода, выполняемый однократно, если Условие 3 правдиво
}
```

## Использование if в функциях

```jsx
const sumPositiveNumbers = (a, b) => {
if (typeof a !== 'number' || typeof b !== 'number') {
return 'One of the arguments is not a number'
}

if (a <= 0 || b <= 0) {
return 'Numbers are not positive'
}

return a + b
}
```

## Инструкция switch

```jsx
switch (Выражение) { 
case A:
// Действия если выражение === А
break
case B:
// Действия если Выражение === В
break
default:
// Действия по умолчанию
}
```

Пример

```jsx
const month = 2

switch (month) {
case 12:
console.log('Декабрь')
break
case 1:
console.log('Январь')
break
case 2:
console.log('Февраль')
break
default:
console.log('Это не зимний месяц')
}
```

## Тернарный оператор

У тернарного оператора три операнда. Тернарный оператор возвращает значение.

Конструкция с тернарным оператором, это выражение, а выражение возвращает значение.

Условие ? Выражение 1 : Выражение 2 

Любое выражение, Если условие правдиво, тогда возвращается результат Выражения 1, Если условие ложно, тогда возвращается результат Выражения 2

Условие

? Выражение 1

: Выражение 2

```jsx
const value = 11

value 
? console.log('Условие истинно')
: console.log('Условие ложно')

```

Другой пример

```jsx
const value1 = 11
const value2 = 25

value1 && value2
? myFunction1(value, value2)
: myFunction2()
```

Ещё пример

```jsx
let value = 11
console.log(value >= 0 ? value : -value) // 11

value = -5
const res = value >= 0 ? value : -value
console.log(res) // 5
```

## Циклы

```jsx
let i = 0
console.log(i)
i++
console.log(i)
i++
console.log(i)
i++
console.log(i)
i++
console.log(i)
i++
console.log(i)
i++
 
```

Перебор всех элементов массива без цикла

```jsx
const myArray = [true, 'abc', 10]

console.log(myArray[0])
console.log(myArray[1])
console.log(myArray[2])
```

Перебор всех свойств объекта без цикла

```jsx
const myObject = {
x: 10,
y: true,
z: 'abc'
}

console.log(myObject.x)
console.log(myObject.y)
console.log(myObject.z)
```

## Типы циклов

for

for ..in…

while

for ...of…

do ...while…

## Цикл for

```jsx
for (Начальная инструкция; Условие; Интерационное действие) {
// Блок кода, выполняемый на каждой итерации
}
```

Пример

```jsx
for (let i = 0; i < 5; i++) {
console.log(i) // 4
}
```

Циклы можно использовать для массивов, но не рекомендуется!

Используйте функции высшего порядка массивов - “forEach”, “map”, “reduce”

## Цикл for для массивов

```jsx
const myArray = ['first', 'second', 'third']

for (let i = 0; i < myArray.length; i++) {
console.log(myArray[i])
}

// 'first'
// 'second'
// 'third'
```

Метод массивов forEach

```jsx
const myArray = ['first', 'second', 'third']

myArray.forEach((element, index) => {
console.log(element, index)
})

// 'first' 0
// 'second' 1
// 'third' 2
```

## Цикл while

```jsx
while (Условие) {
// Блок кода, выполняемый на каждой итерации
}
```

Цикл while выполняется, пока условие правдиво. 

Пример

```jsx
let i = 0

while (i < 5) {
console.log(i)
i++
}
```

Бесконечный цикл

```jsx
let i = 0

while (i < 5) {
console.log(i)
}
```

Цикл do while

```jsx
do {
// Блок кода, выполняемый на каждой итерации
} while (Условие)
```

Пример

```jsx
let i = 0

do { 
console.log(i)
i++
} while (i < 5)
```

Цикл for in

```jsx
for (key in Object) {
// Действия с каждым свойством объекта
// Значения свойства - Object[key]
}
```

Пример

```jsx
const myObject = {
x: 10,
y: true,
z: 'abc'
}

for (const key in myObject) {
console.log(key, myObject[key])
}
```

## forEach для объектов

```jsx
const myObject = {
x: 10,
y: true,
z: 'abc'
}

Object.keys(myObject).forEach(key => {
console.log(key, myObject[key])
})
```

```jsx
const myObject = {
x: 10,
y: true,
z: 'abc'
}

Object.values(myObject).forEach(value => {
console.log(value)
})
```

## For in для массивов

```jsx
const myArray = [true, 10, 'abc', null]

for (const key in myArray) {
console.log(myArray[key])
}
```

Цикл for of (Появился в ecmascript6)

```jsx
for (Element of Iterable) {
// Действия с определенным элементом 
} 
```

Пример

```jsx
const myString = 'Hey'

for (const letter of myString) {
console.log(letter)
}
```

```jsx
const myArray = [true, 10, 'abc', null]

for (const element of myArray) {
console.log(element)
}
```

Метод массивов foreach (предпочтительнее всего)

```jsx
const myArray = [true, 10, 'abc', null]

myArray.forEach(element => {
console.log(element)
})

// true
// 10
// 'abc'
// null
```

## For of не для объектов

## Модули

Модули позволяют структурировать код

Модули позволяют избегать дублирования блоков кода

## Export/import синтаксис появился в ES6

```jsx
moduleOne.js

export ...
```

```jsx
moduleTwo.js

import ...
```

Примеры

## Экспорт по умолчанию.

```jsx
moduleOne.js

const myName = () => {
	console.log('Bogdan')
	}
	
	export default myName
```

```jsx
moduleTwo.js

import printMyName from './moduleOne.js'

printMyName() // Bogdan
```

Название переменных могут не совпадать.

## Несколько экспортов

```jsx
moduleOne.js

const one = 1
const two = 'two'

export {
one,
two
}
```

```jsx
moduleTwo.js

import {
one,
two
} from './moduleOne.js'

console.log(one) // 1
console.log(two) // 'two'
```

Имена переменных должны совпадать.

Переименование импортов в таком формате.

```jsx
moduleTwo.js

import {
one as oneRenamed,
two
} from './moduleOne.js'

console.log(oneRenamed) // 1
console.log(two) // 'two'
```

## Node.js поддерживает ES6 модули, начиная с версии 13

Правила работы с модулями

1. Модули должны быть одноцелевыми
2. Распологайте все export инструкции внизу файла.
3. Распологайте все import инструкции сверху файла.
4. По возможности используйте export default, по возможности.

## Классы и прототипы

Синтаксис классов появился в ES6

```jsx
class ...
```

Классы позволяют создавать прототипы для объектов

На основании прототипов создаются экземпляры.

Экземпляры могут иметь собственные свойства и методы.

Экземпляры наследуют свойства и методы прототипов.

Пример

```jsx
class Comment {
constructor(text) {
this.text = text
this.votesQty = 0
}

upvote() {
this.votesQty += 1
 }
}
```

Переменная this указывает на экземпляр класса.

Создание экземпляра 

```jsx
const firstComment = new Comment ('First comment')
```

Собственные свойства экземпляра 

```jsx
const firstComment = new Comment ('First comment')

console.log(firstComment)
```

Цепочка прототипов

firstComment → Comment → Object

## Проверка принадлежности

```jsx
class Comment {
constructor(text) {
this.text = text
this.votesQty = 0
}

upvote() {
this.votesQty += 1
}
}

const firstComment = new Comment('First Comment')

firstComment instanceof Comment // true
firstComment instanceof Object // false
```

```jsx
class Comment {
constructor(text) {
this.text = text
this.votesQty = 0
}

upvote() {
this.votesQty += 1
}
}

const firstComment = new Comment('First Comment')

firstComment.upvote()
console.log(firstComment.votesQty) // 1
firstComment.upvote()
console.log(firstComment.votesQty) // 2
```

Методы можно вызывать многократно

## Проверка принадлежности свойств экземпляру объекта

```jsx
const firstComment = new Comment('First comment')

firstComment.hasOwnProperty('text') // true
firstComment.hasOwnProperty('votesQty') // true
firstComment.hasOwnProperty('upvote') // false
firstComment.hasOwnProperty('hasOwnProperty') // false
```

## Создание несколько экземпляров класса

```jsx
class Comment {
constructor(text) {
this.text = text
this.votesQty = 0
}

upvote() {
this.votesQty += 1
}
}

const firstComment = new Comment('First comment')
const secondComment = new Comment('Second comment')
const thirdComment = new Comment('Third comment')
```

## Статические методы

```jsx
class Comment {
constructor(text) {
this.text = text
this.votesQty = 0
}

upvote() {
this.votesQty += 1
}
}

static mergeComments(first, second) {
return `${first} ${second}`
}
}

Comment.mergeComments('First comment.', 'Second comment.')
```

Метод доступен как свойство класса и не наследуется экземлярами класса

## Расширение других классов

```jsx
class NumbersArray extends Array {
sum() {
	return this.reduce((el, acc) => acc += el, 0)
	}
}

const myArray = new NumbersArray(2, 5, 7)

console.log(myArray)
myArray.sum()
```

Родительский конструктор вызовется автоматически.

## Цепочка прототипов

myArray → NumbersArray → Array → Object

## Что же такое прототип?

Благодаря скрытому свойству __proto__ создается цепочка прототипов.

Строки и числа ведут себя как объекты.

## Промисы

Промисы позволяют обрабатывать отложенные во времени события.

Промис — это обещание предоставить результат позже.

Промис может вернуть ошибку, если результат предоставить невозможно.

Состояния промиса:

Ожидание

Исполнен

Отклонен

## Cоздание промиса

```jsx
const myPromise = new Promise((resolve, reject) => {
/**
* Выполнение асинхронных действий
*
* Внутри этой функции нужно в результате вызвать одну из функций resolve или reject
*/
});
```

Вновь созданный промис будет в состоянии pending.

```jsx
myPromisе
.then(value => {
/**
* Действия в случае успешного исполнения промиса
* Значение value - это значение, переданное в вызове функции resolve внутри Промиса
*/
})
.catch(error => {
/**
* Действия в случае отклонения промиса
* Значение error - это значение, переданное в вызове функции reject внутри Промиса
*/
})
```

Получение данных с помощью FetchApi

```jsx
fetch('https://jsonplaceholder.typicode.com/todos')
.then(response => response.json())
.then(json => console.log(json))
.catch(error => console.error(error))
```

Пример

```jsx
const getData = (url) =>
	new Promise((resolve, reject) =>
		fetch(url)
			.then(response => response.json())
			.then(json => resolve(json))
			.catch(error => reject(error))
		)
	
getData('https://jsonplaceholder.typicode.com/todos')
	.then(data => console.log(data))
	.catch(error => console.log(error.message))
```

## Async/Await

Async/Await — специальный синтаксис для упрощения работы с промисами.

Асинхронная функция

```jsx
async function asyncFn() {
	// Всегда возвращает промис
}

const asyncFn = async() => {
	// Всегда возвращает промис
}
```

Пример

```jsx
const asyncFn = async() => {
	return 'Success!'
	}
	
asyncFn()
```

```jsx
const asyncFn = async() => {
	return 'Success!'
	}
	
asyncFn()
 .then(value => console.log(value))
```

```jsx
const asyncFn = async() => {
	throw new Error('There was an error!')
	}
 
 assyncFn()
```

```jsx
const asyncFn = async() => {
	throw new Error('There was an error!')
	}
 
 asyncFn()
 .then(value => console.log(value))
 .catch(error => console.log(error.message))
```

```jsx
const asyncFn = async() => {
	await <Promise>
	}
 
 asyncFn()
```

Внутри асинхронных функций можно ожидать результатов промисов

```jsx
const timerPromise = () =>
	new Promise((resolve, reject) =>
		setTimeout(() => resolve(), 2000))
		
const asyncFn = async () => {
	console.log('Timer starts')
	await timerPromise()
	console.log('Timer ended')
	}
	
	asyncFn()
```

```jsx
const timerPromise = () =>
	new Promise((resolve, reject) =>
		setTimeout(() => resolve(), 2000))
		
const asyncFn = async () => {
	console.log('Timer starts')
	const startTime = performance.now()
	await timerPromise()
	const endTime = performance.now()
	console.log('Timer ended', endTime - startTime)
	}
	
	asyncFn()
```

Async/Await

```jsx
const getData = (url) => {
	const res = await fetch(url)
	const json = await res.json()
	return json
	}
	
getData('https://jsonplaceholder.typicode.com/todos')
	.then(data => console.log(data))
	.catch(error => console.log(error.message))
```

```jsx
const getData = async (url) => {
	const res = await fetch(url)
	const json = await res.json()
	return json
	}
	
const url = 'https://jsonplaceholder.typicode.com/todos'
const data = await getData(url)
```

```jsx
const getData = async (url) => {
	const res = await fetch(url)
	const json = await res.json()
	return json
	}
	
const url = 'https://jsonplaceholder.typicode.com/todos'
try {
	const data = await getData(url)
	console.log(data)
} catch (error) {
	console.log(error.message)
}
```

## Главное в Async/Await

1. Async/await — это синтактическая надстройка над промисами
2. await синтаксис возможен только внутри async функций
3. async функция всегда возвращает Promise
4. async функция ожидает результата инструкции await и не выполняет последующие инструкции