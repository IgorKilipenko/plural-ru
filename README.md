# plural-ru


Pluralize russian words like never before 😏

### Installation

```
npm install --save plural-ru
```


Examples:

```js
var plural = require('plural-ru');

// склонение
plural(1, 'файл', 'файла', 'файлов'); // файл
plural(2, 'файл', 'файла', 'файлов'); // файла
plural(5, 'файл', 'файла', 'файлов'); // файлов

// склонение + плейсхолдер
plural(1, '%d файл', '%d файла', '%d файлов'); // 1 файл
plural(2, '%d файл', '%d файла', '%d файлов'); // 2 файла
plural(5, '%d файл', '%d файла', '%d файлов'); // 5 файлов

// единственное и множественное число
plural(1, 'Оформить товар', 'Оформить товары'); // Оформить товар
plural(21, 'Оформить товар', 'Оформить товары'); // Оформить товары


// процессинг числа

function numberWithSpaces(x) {
    return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ' ');
}

plural(1000000, '%d доллар', '%d доллара', '%d долларов', numberWithSpaces); // 1 000 000 долларов
plural(1000000, '%d долларов', numberWithSpaces); // 1 000 000 долларов
```
