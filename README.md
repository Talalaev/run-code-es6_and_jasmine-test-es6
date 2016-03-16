# Шаблон модуля ES6 + тесты jasmine ES6

Вы уже пишете код в стандарте ES6? Сейчас самое время начать! 
Нет, слишком трудозатратно тестировать, нельзя просто так
запустить код в браузере и проверить его работу. Нужно собирать код, компилировать код, запускать тесты в консоли и/или
в браузере. 
Хочется иметь для этого одну команду, а еще лучше, чтобы все было автоматически!

#### Добро пожаловать!
 В заготовке run-code-es6_and_jasmine-test-es6 все это есть! Запускай тесты и код написанный в стандарте ES6 одной командой!

#### Подготовка к работе:
1. ```npm i```
2. подключить нужные зависимости html, css, javascript(например jQuery) в файл _SpqcRunner.html

#### Запуск тестов:
1. В консоли -> ```npm test``` или ```node testModule.js```
    Команда node testModule имеет конфигурацию вывода в консоль. Т.е. все описания написанные в spec файле будут
    выведены в консоль, отформатированны и окрашены в соответствующие цвета.
2. Запуск в браузере -> вызвать shell скрипт compile-spec.bat, открыть _SpecRunner.html
    Для автоматического отслеживания изменений в коде и тестах включить ```watch webpack``` и ```watch babel```
	
#### Для работы требуется:
1. Глобально установленный nodeJS и npm
2. Глобально установленный webpack
3. Глобально установленный jasmine

#### Итоговая структура модуля:
* jasmine - файлы для визуализации тестов в браузере
* node_modules
```
    |
    |__ Зависимости для запуска тестов в формате es6
    |       "babel-core": "^6.3.17",
    |       "babel-preset-es2015": "^6.3.13",
    |       "babel-preset-stage-0": "^6.3.13",
    |__ Зависимость для красивого вывода результатов теста в консоль
    |       "jasmine-spec-reporter": "^2.4.0"
    |__ Зависимость для локальной компиляции файла сборки (код + тесты)
            "babel-cli": "^6.6.5"
```
* _SpacRunner.html - файл для запуска тестов в браузере
* bundle.js - Сборка. Модуль + тесты.
* compile-spec.bat - shell скрип с двумя командами на сборку и компиляцию.
* index.js - Код модуля
* jasmine.json - Конфигурации jasmine
* package.json - Конфигурация модуля
* spec.js - Тесты модуля
* spec-compiled.js - Компилированная сборка (es5). Код модуля + тесты в стандарте es5.
* testModule.js - Конфигурация jasmine. Расширенная конфигурация с подключение кастомного репортера
    jasmine-spec-reporter
* webpack.config.js - Конфигурация webpack