# JavaScript Style Guide, 10 правил о том, как красиво и правильно писать на JavaScript.
---

1. <a href='#first-section'>Объявление переменных</a>
2. <a href='#second-section'>Используй let и const вместо var</a>
3. <a href='#third-section'>Используйте понятные имена переменных и функций</a>
4. <a href='#fourth-section'>Точка с запятой ";"</a>
5. <a href='#fifth-section'>Отступы</a>
6. <a href='#sixth-section'>Пробелы</a>
7. <a href='#seventh-section'>Фигурные скобки</a>
8. <a href='#eighth-section'>Кавычки</a>
9. <a href='#ninth-section'>Длина строки</a>
10. <a href='#tenth-section'>Комментарии</a>

<a name='first-section'>__1. Объявление переменных.__</a>

Объявление каждой локальной переменной объявляет только одну переменную: такие объявления, как let a = 1, b = 2; не используются.
```
// bad
let a = 1, b = 2, c = 3;

// good
let a = 1;
let b = 2;
let c = 3;
```

<a name='second-section'>__2. Используй let и const вместо var.__</a>

Объявляйте все переменные с помощью const или let. По умолчанию используется const, за исключением случаев, кгда нужно переназначить переменную. Ключевое слово var не должно использоваться.
```
// bad
var example = 42;

// good
let example = 42;
```

<a name='third-section'>__3. Используйте понятные имена переменных и функций.__</a>

Код гораздо легче читать, когда при его написании используют понятные, описательные имена функций и переменных.
+ Избегайте однобуквенных имен функций. Имена должны давать представление о том, что делает эта функция.
```
// bad
function q() {
  // ...код...
}

// good
function query() {
  // ...код...
}
```
+ Используйте camelCase для именования объектов, функций и переменных.
```
// bad
var OBJEcttsssss = {};
var this_is_my_object = {};
function c() {};
var u = new user({
  name: 'Bob Parr'
});

// good
var thisIsMyObject = {};
function thisIsMyFunction() {};
var user = new User({
  name: 'Bob Parr'
});
```
+ Имя функции должно быть глаголом на английском языке или начинаться с него.
```
// bad
function pravkaspiska() {
  // тело функции
};

// good
function editName() {
  // тело функции
};
```
<a name='fourth-section'>__4. Точка с запятой.__</a>

В конце выражения обязательна точка с запятой.
```
// bad
alert('Привет')
alert('Мир')

// good
alert('Привет');
alert('Мир');
```
<a name='fifth-section'>__5. Отступы.__</a>

Горизонтальные отступы
+ Горизонтальный отступ выполняется с помощью 2 или 4 пробелов, или символа табуляции (клавиша Tab). Какой из них выбрать – это уже на ваше усмотрение. Пробелы больше распространены.
Одно из преимуществ пробелов над табуляцией заключается в том, что пробелы допускают более гибкие конфигурации отступов, чем символ табуляции.
```
// bad
if (age < 98) {
for (var i = 0, iMax = items.length; i < iMax; ++i) {
// тело цикла
}
}

// good
if (age < 98) {
  for (var i = 0, iMax = items.length; i < iMax; ++i) {
    // тело цикла
  }
}
```
Вертикальные отступы
+Между логическими блоками(циклами, функциями и т.д.) следует оставлять пустую строку. Это делает код более читабельным. Избегайте блоков кода более 9 строк подряд.
```
// bad
var i;
var iMax = items.length;

for (i = 0; i < iMax, ++i) {
  // тело цикла
}
function showName() {
  // тело функции
}

// good
var i;
var iMax = items.length;
for (i = 0; i < iMax, ++i) {
  // тело цикла
}

function showName() {
  // тело функции
}
```

<a name='sixth-section'>__6. Пробелы.__</a>

Пробелы следует использовать разумно, то есть так, чтобы они способствовали улучшению читабельности кода.
+ Используйте пробелы между параметрами и не используйте между именем функции и скобкой; 
```
// bad
function edit (name,age) {
  // тело функции
}

// good
function edit(name, age) {
  // тело функции
}
```
+ Устанавливайте один пробел перед открывающей скобкой.; 
```
// bad
function test(){
  console.log('test');
}

// хорошо
function test() {
  console.log('test');
}
+ Используйте пробелы вокруг операторов. 
// bad
if (age<100) {
  // тело цикла
}

// good
if (age < 100) {
  // тело цикла
}

<a name='seventh-section'>__7. Фигурные скобки.__</a>

+ Используйте фигурные скобки для всех многострочных блоков.
```
// плохо
if (test)
  return false;

// хорошо
if (test) {
  return false;
}
```
+ Открывающая фигурная скобка располагается на той же строке. Перед скобкой пробел. Закрывающая скобка располагается на новой строке.
```

function edit(name, age)
{
  if (age < 100) {/*тело цикла*/}
}

// хорошо
function edit(name, age) {
  if (age < 100) {
    // тело цикла
  }
}
```
<a name='eighth-section'>__8. Кавычки.__</a>

Всегда в коде скрипта используйте одинарные кавычки, если не требуется иного. Двойные кавычки допустимы, если в этой же строке необходимо использовать апостроф (') или одинарные кавычки для других целей.
```
// плохо
var string = "строка";

// хорошо
var string = 'строка';
var phrase = "you're next";
```
<a name='ninth-section'>__9. Длина строки.__</a>

Никто не любит читать длинные горизонтальные строки кода. Строки длиннее 80 символов нужно разделять, выполняя перенос через конкатенацию строк.
```
// плохо
var errorMessage = 'Эта сверхдлинная ошибка возникла из-за белой обезъяны. Не говори про обезъяну! Не слушай об обезьяне! Не думай об обезъяне!';
```
```
// хорошо
var errorMessage = 'Эта сверхдлинная ошибка возникла из-за белой обезъяны. ' +
  'Не говори про обезъяну! Не слушай об обезьяне! ' +
  'Не думай об обезъяне!';
```
<a name='tenth-section'>__10. Комментарии.__</a>

Не нужно комментировать очевидные вещи, добавлять в код комментарии, которые не помогают разобраться в его сути.
+ Используйте /** ... */ для многострочных комментариев. Включите описание, опишите типы и значения для всех параметров и возвращаемых значений в формате jsdoc.
```
// плохо
// make() возвращает новый элемент
// основываясь на получаемом имени тэга
//
// @param <String> tag
// @return <Element> element
function make(tag) {

  // ...создаем element...

  return element;
}

// хорошо
/**
 * make() возвращает новый элемент
 * основываясь на получаемом имени тэга
 *
 * @param <String> tag
 * @return <Element> element
 */
function make(tag) {

  // ...создаем element...

  return element;
}
```
+ Используйте // для комментариев в одну строку. Размещайте комментарии на новой строке над темой комментария. Добавляйте пустую строку над комментарием.
```
// плохо
var active = true;  // устанавливаем активным элементом

// хорошо
// устанавливаем активным элементом
var active = true;

// плохо
function getType() {
  console.log('проверяем тип...');
  // задаем тип по умолчанию 'no type'
  var type = this._type || 'no type';

  return type;
}

// хорошо
function getType() {
  console.log('проверяем тип...');

  // задаем тип по умолчанию 'no type'
  var type = this._type || 'no type';

  return type;
}
```