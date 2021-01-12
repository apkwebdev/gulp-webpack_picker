# Сборщик проектов gulp-webpack

Работает на базе gulp4 и webpack-stream. Предназначен для автоматизации сборки сайтов. 

## Особенности
* Для сборки html используется препроцессор pug.
* Для сборки css используется препроцессор sass в синтаксисе scss.
* Для сборки js используется webpack-stream.
* Есть специальные функции и миксины создающие для размеров элементов функции calc()
и медиазапросы, зависящие от ширины окна браузера и главного контейнера страницы. 

## Особенности компоновки сборщика
### Сборщик состоит из двух модулей:
1. [gulp-webpack_picker](https://github.com/apkwebdev/gulp-webpack_picker/)
2. [gulp-webpack_project](https://github.com/apkwebdev/gulp-webpack_project/)
### Для запуска сборщика требуется установка обеих его частей!

## Правильная установка модулей "gulp-webpack_picker" и "gulp-webpack_project"
* Запускаем командную строку в директории, в которой будем размещать директорию сборщика, например, C:\WebDev\projects\
* Название для сборщика пусть будет gulp-webpack

### Установка модуля "gulp-webpack_picker"
* Выполняем команду ```git clone https://github.com/apkwebdev/gulp-webpack_picker.git C:\WebDev\projects\gulp-webpack\```
* Будет создана директория C:\WebDev\projects\gulp-webpack\ и в ней файлы сборщика и директория #picker\ со своими поддиректориями и файлами
* Теперь выполняем установку модуля "gulp-webpack_project"

### Установка модуля "gulp-webpack_project"
* Выполняем команду ```git clone https://github.com/apkwebdev/gulp-webpack_project.git C:\WebDev\projects\gulp-webpack\\#project\```
* В директории C:\WebDev\projects\gulp-webpack\ появится директория #project\ со своими поддиректориями и файлами

### Таким образом получим
* Корневую директорию сборщика C:\WebDev\projects\gulp-webpack\ 
* В ней файлы сборщика
* А также поддиректории #picker и #project со своими поддиректориями и файлами

### Запуск сборщика
* Запускаем командную строку в корневой директории сборщика C:\WebDev\projects\gulp-webpack\
* Выполняем в ней команду npm install
* После установки всех необходимых компонентов запускаем нужную команду из списка команд сборщика, описанных ниже

## Команды сборщика
1. режим "development": gulp      /*при запуске сначала очищается всё, кроме images и fonts*/
2. режим "production": gulp --p   /*при запуске сначала делается полная очистка*/
3. очистка всего, кроме images и fonts: gulp clean
4. полная очистка: gulp clean --p
